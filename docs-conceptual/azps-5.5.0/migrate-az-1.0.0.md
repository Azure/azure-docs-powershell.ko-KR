---
title: AzureRM에서 Azure PowerShell Az 1.0.0으로의 모든 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell Az 버전 1 릴리스의 호환성이 손상되는 변경에 대한 목록이 포함되어 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 3ab12307f786c12422338835926802793a33713e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012012"
---
# <a name="breaking-changes-for-az-100"></a>Az 1.0.0의 호환성이 손상되는 변경

이 문서에서는 AzureRM 6.x와 새 Az 모듈 버전 1.x 이상 간의 변경 내용에 대한 자세한 정보를 제공합니다. 목차는 스크립트에 영향을 줄 수 있는 모듈별 변경을 포함하여 전체 마이그레이션 경로를 안내합니다.

마이그레이션을 AzureRM에서 Az로 시작하는 방법에 대한 일반적인 추천 사항은 [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)을 참조하세요.

> [!IMPORTANT]
> Az 1.0.0과 Az 2.0.0 간에도 호환성이 손상되는 변경이 있습니다. 이 가이드에 따라 AzureRM에서 Az로 업데이트한 후에 [Az 2.0.0 호환성이 손상되는 변경](migrate-az-2.0.0.md)을 참조하여 추가로 변경할 필요가 있는지 확인하세요.

## <a name="table-of-contents"></a>목차

- [일반적인 주요 변경 내용](#general-breaking-changes)
  - [cmdlet 명사 접두사 변경](#cmdlet-noun-prefix-changes)
  - [모듈 이름 변경](#module-name-changes)
  - [제거된 모듈](#removed-modules)
  - [Windows PowerShell 5.1 및 .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [PSCredential을 사용하여 사용자 로그인 임시 제거](#temporary-removal-of-user-login-using-pscredential)
  - [웹 브라우저 프롬프트 대신 기본 디바이스 코드 로그인](#default-device-code-login-instead-of-web-browser-prompt)
- [모듈의 호환성이 손상되는 변경](#module-breaking-changes)
  - [Az.ApiManagement(이전에는 AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing(이전에는 AzureRM.Billing, AzureRM.Consumption, 및 AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices(이전에는 AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute(이전에는 AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory(이전에는 AzureRM.DataFactories 및 AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics(이전에는 AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore(이전에는 AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault(이전에는 AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media(이전에는 AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor(이전에는 AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network(이전에는 AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights(이전에는 AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices(이전에는 AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, 및 AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources(이전에는 AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric(이전에는 AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql(이전에는 AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage(이전에는 Azure.Storage 및 AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites(이전에는 AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>일반적인 주요 변경 내용

이 섹션에서는 Az 모듈 재설계의 일부인 일반적인 호환성이 손상되는 변경에 대해 자세히 설명합니다.

### <a name="cmdlet-noun-prefix-changes"></a>Cmdlet 명사 접두사 변경

AzureRM 모듈에서 cmdlet은 `AzureRM` 또는 `Azure`를 명사 접두사로 사용했습니다.  Az는 cmdlet 이름을 간소화하고 정규화하여 모든 cmdlet에서 'Az'를 해당 cmdlet 명사 접두사로 사용합니다. 예를 들면 다음과 같습니다.

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

다음으로 변경되었습니다.

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

이러한 새 cmdlet 이름으로 더 간단하게 전환할 수 있도록 Az에서 [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) 및 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias)라는 두 개의 새 cmdlet을 도입했습니다.  `Enable-AzureRmAlias`는 최신 Az cmdlet 이름에 매핑되는 AzureRM의 이전 cmdlet 이름에 대한 별칭을 에 만듭니다. `Enable-AzureRmAlias`에서 `-Scope` 인수를 사용하면 별칭을 사용하도록 설정되는 위치를 선택할 수 있습니다.

예를 들어, AzureRM의 다음 스크립트가 있습니다.

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

`Enable-AzureRmAlias`를 사용하여 최소한의 변경으로 실행할 수 있습니다.

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

`Enable-AzureRmAlias -Scope CurrentUser`를 실행하면 열려 있는 모든 PowerShell 세션에 별칭을 사용하도록 설정되므로 이 cmdlet을 실행한 후 이와 같은 스크립트를 전혀 변경할 필요가 없습니다.

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

별칭 cmdlet을 사용하는 방법에 대한 자세한 내용은 [Enable-AzureRmAlias 참조](/powershell/module/az.accounts/enable-azurermalias)를 참조하세요.

별칭을 사용하지 않도록 설정할 준비가 되면 `Disable-AzureRmAlias`에서 만들어진 별칭을 제거합니다. 자세한 내용은 [Disable-AzureRmAlias 참조](/powershell/module/az.accounts/disable-azurermalias)를 참조하세요.

> [!IMPORTANT]
> 별칭을 사용하지 않도록 설정하는 경우 별칭을 사용하도록 설정된 _모든_ 범위에 대해 사용하지 않도록 설정해야 합니다.

### <a name="module-name-changes"></a>모듈 이름 변경

다음 모듈을 제외하고 모듈 이름이 `AzureRM.*`에서 `Az.*`로 변경되었습니다.

| AzureRM 모듈 | Az 모듈 |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

모듈 이름이 변경되면 `#Requires` 또는 `Import-Module`을 사용하여 특정 모듈을 로드하는 스크립트는 대신 새 모듈을 사용하도록 변경되어야 합니다. cmdlet 접미사가 변경되지 않은 모듈의 경우 이는 모듈 이름이 변경되었지만 작업 공간을 나타내는 접미사가 _변경되지 않았음_ 을 의미합니다.

#### <a name="migrating-requires-and-import-module-statements"></a>#Requires 및 Import-Module 문 마이그레이션

`#Requires` 또는 `Import-Module`을 사용하여 AzureRM 모듈에 대한 종속성을 선언하는 스크립트는 새 모듈 이름을 사용하도록 업데이트해야 합니다. 예를 들면 다음과 같습니다.

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

다음으로 변경되어야 합니다.

```azurepowershell-interactive
#Requires -Module Az.Compute
```

`Import-Module`의 경우

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

다음으로 변경되어야 합니다.

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Cmdlet 정규화 호출 마이그레이션

다음과 같이 모듈에서 정규화된 cmdlet 호출을 사용하는 스크립트는

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

새 모듈 및 cmdlet 이름을 사용하도록 변경되어야 합니다.

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>모듈 매니페스트 종속성 마이그레이션

모듈 매니페스트 파일(.psd1)을 통해 AzureRM 모듈에 대한 종속성을 나타내는 모듈은 `RequiredModules` 섹션에서 모듈 이름을 업데이트해야 합니다

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

다음으로 변경되어야 합니다.

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>제거된 모듈

다음 모듈이 제거되었습니다.

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

이러한 서비스를 위한 도구는 더 이상 적극적으로 지원되지 않습니다.  편리한 대체 서비스로 이동하는 것이 좋습니다.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 및 .NET 4.7.2

Windows용 PowerShell 5.1에서 Az를 사용하려면 .NET Framework 4.7.2를 설치해야 합니다. PowerShell Core 6.x 이상을 사용하는 경우 .NET Framework가 필요하지 않습니다.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>PSCredential을 사용하여 사용자 로그인 임시 제거

.NET 표준의 인증 흐름이 변경되어 PSCredential을 통한 사용자 로그인이 일시적으로 제거됩니다. 이 기능은 Windows용 PowerShell 5.1에 대한 2019년 1월 15일 릴리스에서 다시 도입됩니다. 이는 [이 GitHub 문제](https://github.com/Azure/azure-powershell/issues/7430)에서 자세히 설명하고 있습니다.

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>웹 브라우저 프롬프트 대신 기본 디바이스 코드 로그인

.NET 표준의 인증 흐름이 변경되어 대화식 로그인 중에 기본 로그인 흐름으로 디바이스 로그인을 사용합니다. 웹 브라우저 기반 로그인은 Windows용 PowerShell 5.1에 대한 2019년 1월 15일 릴리스에서 기본적으로 다시 도입됩니다. 이때 사용자는 스위치 매개 변수를 사용하여 디바이스 로그인을 선택할 수 있습니다.

## <a name="module-breaking-changes"></a>모듈의 호환성이 손상되는 변경

이 섹션에서는 개별 모듈 및 cmdlet에 대한 특정 호환성이 손상되는 변경에 대해 자세히 설명합니다.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement(이전에는 AzureRM.ApiManagement)

- 다음 cmdlet이 제거되었습니다.
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - 대신 **Set-AzApiManagement** 를 사용하여 이러한 속성을 설정합니다.
- 다음 속성이 제거되었습니다.
  - `PsApiManagementContext`에서 `PsApiManagementHostnameConfiguration` 형식의 `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration`, `ScmHostnameConfiguration` 속성을 제거했습니다. 대신 `PsApiManagementCustomHostNameConfiguration` 형식의 `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration`, `ScmCustomHostnameConfiguration`을 사용합니다.
  - PsApiManagementContext에서 `StaticIPs`속성을 제거했습니다. 해당 속성은 `PublicIPAddresses`, `PrivateIPAddresses`로 분할되었습니다.
  - 필수 속성 `Location`을 New-AzureApiManagementVirtualNetwork cmdlet에서 제거했습니다.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing(이전에는 AzureRM.Billing, AzureRM.Consumption, 및 AzureRM.UsageAggregates)

- `InvoiceName` 매개 변수가 `Get-AzConsumptionUsageDetail` cmdlet에서 제거되었습니다.  스크립트는 청구서에 대한 다른 ID 매개 변수를 사용해야 합니다.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices(이전에는 AzureRM.CognitiveServices)

- `Get-AzCognitiveServicesAccountSkus` cmdlet에서 `GetSkusWithAccountParamSetName` 매개 변수 집합을 제거했습니다.  ResourceGroupName 및 계정 이름을 사용하는 대신 계정 형식 및 위치별로 SKU를 가져와야 합니다.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute(이전에는 AzureRM.Compute)

- `PSVirtualMachine` 및 `PSVirtualMachineScaleSet` 객체의 `Identity` 속성에서 `IdentityIds`가 제거되었습니다. 스크립트는 더 이상 이 필드의 값을 사용하여 처리 결정을 내려서는 안됩니다.
- `PSVirtualMachineScaleSetVM` 개체의 `InstanceView` 속성의 형식이 `VirtualMachineInstanceView`에서 `VirtualMachineScaleSetVMInstanceView`로 변경되었습니다.
- `UpgradePolicy` 속성에서 `AutoOSUpgradePolicy` 및 `AutomaticOSUpgrade` 속성이 제거되었습니다.
- `PSSnapshotUpdate` 개체의 `Sku` 속성의 형식이 `DiskSku`에서 `SnapshotSku`로 변경되었습니다.
- `VmScaleSetVMParameterSet`이 `Add-AzVMDataDisk` cmdlet에서 제거되어, 더 이상 ScaleSet VM에 개별적으로 데이터 디스크를 추가할 수 없습니다.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory(이전에는 AzureRM.DataFactories 및 AzureRM.DataFactoryV2)

- `GatewayName` 매개 변수가 `New-AzDataFactoryEncryptValue` cmdlet에서 필수 항목이 되었습니다.
- `New-AzDataFactoryGatewayKey` cmdlet이 제거됨
- `Get-AzDataFactoryV2ActivityRun` cmdlet에서 `LinkedServiceName` 매개 변수가 제거되었습니다. 스크립트는 더 이상 이 필드의 값을 사용하여 처리 결정을 내려서는 안됩니다.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics(이전에는 AzureRM.DataLakeAnalytics)

- 사용되지 않는 cmdlet 제거: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore(이전에는 AzureRM.DataLakeStore)

- 다음 cmdlet의 `Encoding` 매개 변수는 `FileSystemCmdletProviderEncoding` 형식에서 `System.Text.Encoding` 형식으로 변경되었습니다. 이 변경은 인코딩 값 `String` 및 `Oem`을 제거합니다. 다른 모든 이전 인코딩 값은 유지됩니다.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- 사용되지 않는 `Tags` 속성 별칭을 `New-AzDataLakeStoreAccount` 및 `Set-AzDataLakeStoreAccount` cmdlet에서 제거함

  다음을 사용하는 스크립트
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  다음과 같이 변경되어야 합니다.
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- `PSDataLakeStoreAccountBasic` 개체에서 사용되지 않는 속성 `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps`을 제거했습니다.  `Get-AzDataLakeStoreAccount`에서 반환된 `PSDatalakeStoreAccount`를 사용하는 모든 스크립트는 이러한 속성을 참조하지 않아야 합니다.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault(이전에는 AzureRM.KeyVault)

- `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` 및 `PSKeyVaultSecretAttributes` 개체에서 `PurgeDisabled` 속성이 제거되었습니다. 스크립트는 처리 결정을 내리기 위해 ```PurgeDisabled``` 속성을 더 이상 참조하지 않아야 합니다.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media(이전에는 AzureRM.Media)

- 다음을 사용하여 `New-AzMediaService` cmdlet에서 사용되지 않는 `Tags` 속성 별칭을 제거합니다.
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  다음과 같이 변경되어야 합니다.
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor(이전에는 AzureRM.Insights)

- `Set-AzDiagnosticSetting` cmdlet 스크립트에서 다음을 사용하여 단일 매개 변수 이름을 위해 복수 이름 `Categories` 및 `Timegrains` 매개 변수를 제거했습니다.
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  다음과 같이 변경되어야 합니다.
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network(이전에는 AzureRM.Network)

- 사용되지 않는 매개 변수 `ResourceId`를 `Get-AzServiceEndpointPolicyDefinition` cmdlet에서 제거
- `PSVirtualNetwork` 개체에서 사용되지 않는 속성 `EnableVmProtection`을 제거했습니다.
- 사용되지 않는 cmdlet 제거: `Set-AzVirtualNetworkGatewayVpnClientConfig`

스크립트는 더 이상 이 필드의 값에 따라 처리하도록 결정하지 않아야 합니다.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights(이전에는 AzureRM.OperationalInsights)

- `Get-AzOperationalInsightsDataSource`에 설정된 기본 매개 변수가 제거되고 `ByWorkspaceNameByKind`가 기본 매개 변수 집합이 되었습니다.

  다음을 사용하여 데이터 원본을 나열하는 스크립트
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  종류를 지정하도록 변경되어야 합니다.
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices(이전에는 AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, 및 AzureRM.RecoveryServices.SiteRecovery)

- `New/Set-AzRecoveryServicesAsrPolicy` cmdlet에서 `Encryption` 매개 변수를 제거했습니다.
- `TargetStorageAccountName` 매개 변수는 이제 `Restore-AzRecoveryServicesBackupItem` cmdlet의 관리 디스크 복원에 필수 항목입니다.
- `Restore-AzRecoveryServicesBackupItem` cmdlet에서 `StorageAccountName`, `StorageAccountResourceGroupName` 매개 변수 제거
- `Get-AzRecoveryServicesBackupContainer` cmdlet에서 `Name` 매개 변수 제거

### <a name="azresources-previously-azurermresources"></a>Az.Resources(이전에는 AzureRM.Resources)

- `New/Set-AzPolicyAssignment` cmdlet에서 `Sku` 매개 변수를 제거했습니다.
- `New-AzADServicePrincipal` 및 `New-AzADSpCredential` cmdlet에서 `Password` 매개 변수를 제거했습니다. 암호는 자동으로 생성되며 암호를 제공하는 스크립트는 다음과 같습니다.

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  출력에서 암호를 검색하도록 변경해야 합니다.

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric(이전에는 AzureRM.ServiceFabric)

- 다음 cmdlet 반환 형식이 변경되었습니다.
  - `ApplicationHealthPolicy` 형식의 속성 `ServiceTypeHealthPolicies`가 제거되었습니다.
  - `ClusterUpgradeDeltaHealthPolicy` 형식의 속성 `ApplicationHealthPolicies`가 제거되었습니다.
  - `ClusterUpgradePolicy` 형식의 속성 `OverrideUserUpgradePolicy`가 제거되었습니다.
  - 이러한 변경 내용은 다음 cmdlet에 영향을 줍니다.
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql(이전에는 AzureRM.Sql)

- `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet에서 `State`, `ResourceId` 매개 변수 제거
- 사용되지 않는 cmdlet 제거: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- 사용되지 않는 매개 변수 `Current`을 `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet에서 제거
- 사용되지 않는 매개 변수 `DatabaseName`을 `Get-AzSqlServerServiceObjective` cmdlet에서 제거
- 사용되지 않는 매개 변수 `PrivilegedLogin`을 `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet에서 제거

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage(이전에는 Azure.Storage 및 AzureRM.Storage)

- 스토리지 계정 이름만 사용하여 Oauth 스토리지 컨텍스트를 만들 수 있도록 기본 매개 변수 집합이 `OAuthParameterSet`으로 변경되었습니다.
  - 예: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- `Location` 매개 변수가 `Get-AzStorageUsage` cmdlet에서 필수 항목이 되었습니다.
- 이제 Storage API 메서드는 동기 API 호출 대신 작업 기반 비동기 패턴(TAP)을 사용합니다. 다음 예제에서는 새 비동기 명령을 보여 줍니다.

#### <a name="blob-snapshot"></a>Blob 스냅샷

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>스냅샷 공유

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>일시 삭제된 Blob 삭제 취소

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>BLOB 계층 설정

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites(이전에는 AzureRM.Websites)

- 사용되지 않는 속성을 `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, `PSSite` 개체에서 제거했습니다.
