---
title: Microsoft Azure PowerShell 6.0.0의 주요 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell 버전 6 릴리스의 주요 변경 내용에 대한 목록이 포함되어 있습니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 1fbd24996da2fbc7d4e95c2a63f828aea6cb3145
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534934"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Microsoft Azure PowerShell 6.0.0의 주요 변경 내용

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다. 각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다. 심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.

## <a name="table-of-contents"></a>목차

- [일반적인 주요 변경 내용](#general-breaking-changes)
    - [요구되는 최소 PowerShell 버전이 5.0으로 향상됨](#minimum-powershell-version-required-bumped-to-50)
    - [기본적으로 사용되는 컨텍스트 자동 저장](#context-autosave-enabled-by-default)
    - [태그 별칭 제거](#removal-of-tags-alias)
- [AzureRM.Compute cmdlet의 주요 변경 내용](#breaking-changes-to-azurermcompute-cmdlets)
- [AzureRM.DataLakeStore cmdlet의 주요 변경 내용](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [AzureRM.Dns cmdlet의 주요 변경 내용](#breaking-changes-to-azurermdns-cmdlets)
- [AzureRM.Insights cmdlet의 주요 변경 내용](#breaking-changes-to-azurerminsights-cmdlets)
- [AzureRM.KeyVault cmdlet의 주요 변경 내용](#breaking-changes-to-azurermkeyvault-cmdlets)
- [AzureRM.Network cmdlet의 주요 변경 내용](#breaking-changes-to-azurermnetwork-cmdlets)
- [AzureRM.RedisCache cmdlet의 주요 변경 내용](#breaking-changes-to-azurermrediscache-cmdlets)
- [AzureRM.Resources cmdlet의 주요 변경 내용](#breaking-changes-to-azurermresources-cmdlets)
- [AzureRM.Storage cmdlet의 주요 변경 내용](#breaking-changes-to-azurermstorage-cmdlets)
- [제거된 모듈](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>일반적인 주요 변경 내용

### <a name="minimum-powershell-version-required-bumped-to-50"></a>요구되는 최소 PowerShell 버전이 5.0으로 향상됨

이전에는 Azure PowerShell에서 모든 cmdlet을 실행하는 데 PowerShell 버전3.0 _이상_이 필요했습니다. 앞으로 이 요구 사항은 PowerShell 버전 5.0으로 향상됩니다. PowerShell 5.0으로 업그레이드하는 방법에 대한 자세한 내용은 [이 표](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)를 참조하세요.

### <a name="context-autosave-enabled-by-default"></a>기본적으로 사용되는 컨텍스트 자동 저장

컨텍스트 자동 저장은 새 PowerShell 세션과 다른 PowerShell 세션 간에 사용할 수 있는 Azure 로그인 정보의 스토리지입니다. 컨텍스트 자동 저장에 대한 자세한 내용은 [이 문서](https://docs.microsoft.com/powershell/azure/context-persistence)를 참조하세요.

이전에는 컨텍스트 자동 저장이 기본적으로 비활성화되었으므로 먼저 `Enable-AzureRmContextAutosave` cmdlet을 실행하여 컨텍스트 지속성을 설정해야 세션 간에 사용자의 Azure 인증 정보를 저장할 수 있었습니다. 앞으로 컨텍스트 자동 저장은 기본적으로 사용하도록 설정됩니다. 즉, _저장된 컨텍스트 자동 저장 설정이 없는_ 사용자는 다음에 로그인할 때 컨텍스트가 저장됩니다. 사용자는 `Disable-AzureRmContextAutosave` cmdlet을 사용하여 이 기능을 사용하지 않도록 선택할 수 있습니다.

_참고_: 이전에 컨텍스트 자동 저장이 설정되지 않은 사용자 또는 컨텍스트 자동 저장이 설정된 사용자 및 기존 컨텍스트는 이 변경으로 인해 영향을 받지 않습니다.

### <a name="removal-of-tags-alias"></a>태그 별칭 제거

`Tag` 매개 변수에 대한 `Tags` 별칭은 많은 cmdlet에서 제거되었습니다. 이 변경으로 인해 영향을 받는 모듈 및 해당 cmdlet에 대한 목록은 다음과 같습니다.

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>AzureRM.Compute cmdlet의 주요 변경 내용

**기타**
- `PSDisk` 및 `PSSnapshot` 형식에 중첩된 SKU 이름 속성이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- `PSVirtualMachine`, `PSVirtualMachineScaleSet` 및 `PSImage` 형식에 중첩된 스토리지 계정 유형 속성이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Add-AzureRmVMDataDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Add-AzureRmVmssDataDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**New-AzureRmAvailabilitySet**
- `Managed` 매개 변수가 `Sku`을 위해 제거되었습니다

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- `SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**New-AzureRmDiskUpdateConfig**
- `SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**New-AzureRmSnapshotConfig**
- `SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**New-AzureRmSnapshotUpdateConfig**
- `SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Set-AzureRmImageOsDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Set-AzureRmVMAEMExtension**
- `DisableWAD` 매개 변수가 제거되었습니다.
    -  Windows Azure Diagnostics는 기본적으로 사용되지 않습니다.

**Set-AzureRmVMDataDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Set-AzureRmVMOSDisk**
- `StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Set-AzureRmVmssStorageProfile**
- `ManagedDisk` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

**Update-AzureRmVmss**
- `ManagedDiskStorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>AzureRM.DataLakeStore cmdlet의 주요 변경 내용

**Export-AzureRmDataLakeStoreItem**
- `PerFileThreadCount` 및 `ConcurrentFileCount` 매개 변수가 제거되었습니다. 앞으로 `Concurrency` 매개 변수를 사용하세요.

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- `PerFileThreadCount` 및 `ConcurrentFileCount` 매개 변수가 제거되었습니다. 앞으로 `Concurrency` 매개 변수를 사용하세요.

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- `Clean` 매개 변수가 제거되었습니다.

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>AzureRM.Dns cmdlet의 주요 변경 내용

**New-AzureRmDnsRecordSet**
- `Force` 매개 변수가 제거되었습니다.

**Remove-AzureRmDnsRecordSet**
- `Force` 매개 변수가 제거되었습니다.

**Remove-AzureRmDnsZone**
- `Force` 매개 변수가 제거되었습니다.

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>AzureRM.Insights cmdlet의 주요 변경 내용

**Add-AzureRmAutoscaleSetting**
- `AutoscaleProfiles` 및 `Notifications` 매개 변수 별칭이 제거되었습니다.

**Add-AzureRmLogProfile**
- `Categories` 및 `Locations` 매개 변수 별칭이 제거되었습니다.

**Add-AzureRmMetricAlertRule**
- `Actions` 매개 변수 별칭이 제거되었습니다.

**Add-AzureRmWebtestAlertRule**
- `Actions` 매개 변수 별칭이 제거되었습니다.

**Get-AzureRmLog**
- `MaxRecords` 및 `MaxEvents` 매개 변수 별칭이 제거되었습니다.

**Get-AzureRmMetricDefinition**
- `MetricNames` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmAlertRuleEmail**
- `CustomEmails` 및 `SendToServiceOwners` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmAlertRuleWebhook**
- `Properties` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmAutoscaleNotification**
- `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` 및 `Webhooks` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmAutoscaleProfile**
- `Rules`, `ScheduleDays`, `ScheduleHours` 및 `ScheduleMinutes` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmAutoscaleWebhook**
- `Properties` 매개 변수 별칭이 제거되었습니다.

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>AzureRM.KeyVault cmdlet의 주요 변경 내용

**Add-AzureKeyVaultCertificate**
- `CertificatePolicy` 매개 변수가 필수 항목이 되었습니다.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- 액세스 토큰을 구성하는 개별 매개 변수는 더 이상 허용되지 않습니다. 대신 명시적 토큰 매개 변수(예: `Service` 또는 `Permissions`)를 다른 곳에 정의된 액세스 토큰 샘플에 해당하는 제네릭 `TemplateUri` 매개 변수(아마도 Storage PowerShell cmdlet을 사용하거나 Storage 설명서에 따라 수동으로 구성됨)로 바꿉니다. `ValidityPeriod` 매개 변수는 계속 유지됩니다.

Azure Storage에 대한 공유 액세스 토큰 구성에 대한 자세한 내용은 다음의 각 설명서 페이지를 참조하세요.
- [서비스 SAS 생성(영문)](https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [계정 SAS 생성(영문)](https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- `IssuerProvider` 매개 변수가 필수 항목이 되었습니다.

**Undo-AzureKeyVaultCertificateRemoval**
- 이 cmdlet의 출력이 `CertificateBundle`에서 `PSKeyVaultCertificate`로 변경되었습니다.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName`은 `InputObject` 매개 변수 집합에서 제거되었으며, 대신 `InputObject` 매개 변수의 `ResourceId` 속성에서 가져옵니다.

**Set-AzureRmKeyVaultAccessPolicy**
- `all` 권한이 `PermissionsToKeys`, `PermissionsToSecrets` 및 `PermissionsToCertificates`에서 제거되었습니다.

**일반**
- `ValueFromPipelineByPropertyName` 속성이 `InputObject`에 의한 파이핑을 사용하도록 설정된 모든 cmdlet에서 제거되었습니다.  영향을 받는 cmdlet은 다음과 같습니다.
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `ConfirmImpact` 수준이 모든 cmdlet에서 제거되었습니다.  영향을 받는 cmdlet은 다음과 같습니다.
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `IKeyVaultDataServiceClient`가 업데이트되어 모든 Certificate 작업에서 SDK 형식 대신 PSType을 반환합니다. 다음 내용이 포함됩니다.
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>AzureRM.Network cmdlet의 주요 변경 내용


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` 매개 변수가 제거되었습니다.

**Add-AzureRmVirtualNetworkPeering**
- `AlloowGatewayTransit` 매개 변수 별칭이 제거되었습니다.

**New-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` 매개 변수가 제거되었습니다.

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` 매개 변수가 제거되었습니다.

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>AzureRM.RedisCache cmdlet의 주요 변경 내용

**New-AzureRmRedisCache**
- `Subnet` 및 `VirtualNetwork` 매개 변수가 `SubnetId`를 위해 제거되었습니다.
- `RedisVersion` 매개 변수가 제거되었습니다.
- `MaxMemoryPolicy` 매개 변수가 `RedisConfiguration`을 위해 제거되었습니다

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- `MaxMemoryPolicy` 매개 변수가 `RedisConfiguration`을 위해 제거되었습니다

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>AzureRM.Resources cmdlet의 주요 변경 내용

**Find-AzureRmResource**
- 이 cmdlet은 제거되었으며, 해당 기능이 `Get-AzureRmResource`으로 이동되었습니다.

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- 이 cmdlet은 제거되었으며, 해당 기능이 `Get-AzureRmResourceGroup`으로 이동되었습니다.

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- `AtScopeAndBelow` 매개 변수가 제거되었습니다.

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>AzureRM.Storage cmdlet의 주요 변경 내용

**New-AzureRmStorageAccount**
- `EnableEncryptionService` 매개 변수가 제거되었습니다.

**Set-AzureRmStorageAccount**
- `EnableEncryptionService` 및 `DisableEncryptionService` 매개 변수가 제거되었습니다.

## <a name="removed-modules"></a>제거된 모듈

### `AzureRM.ServerManagement`

서버 관리 도구 서비스가 [작년에 사용 중지](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)되어 SMT에 해당하는 `AzureRM.ServerManagement` 모듈이 `AzureRM`에서 제거되었으며, 앞으로 제공되지 않습니다.

### `AzureRM.SiteRecovery`

`AzureRM.SiteRecovery` 모듈은 `AzureRM.SiteRecovery` 모듈의 기능 상위 집합이고 동등한 새 cmdlet 집합이 포함된 `AzureRM.RecoveryServices.SiteRecovery`로 대체됩니다. 이전 cmdlet과 새 cmdlet을 매핑한 전체 목록은 다음과 같습니다.

| 사용되지 않는 cmdlet                                        | 상응하는 cmdlet                                                | 별칭                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
