---
title: Az 5.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 5.0.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3a82e738bcb652ddc38886f7064e7373b5fb8cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754131"
---
# <a name="migration-guide-for-az-500"></a>Az 5.0.0 마이그레이션 가이드

이 문서에서는 Az 4.0.0에서 5.0.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.

- [Az 5.0.0 마이그레이션 가이드](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- `NodeOsType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다. 이는 항상 `Linux`입니다.
- `ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.
- `NodeVmSetType`의 기본값은 `AvailabilitySet`에서 `VirtualMachineScaleSets`로 변경되었습니다.
- `NetworkPlugin`의 기본값은 `none`에서 `azure`로 변경되었습니다.

#### <a name="before"></a>이전

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>이러한

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

`ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.

#### <a name="before"></a>이전

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>이러한

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

`StorageAccountName` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>이러한

`Classic`은 사용되지 않으며 `StorageAccountName`은 Classic Container Registry에서만 작동하므로 제거되었습니다.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

`Get-AzFunctionApp` 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 `IncludeSlot` 스위치 매개 변수가 제거되었습니다. 이제 cmdlet은 `-IncludeSlot`이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.
이전 cmdlet 버전에서는 이 기능이 작동하지 않았습니다. 하지만 이제 문제가 해결되었습니다.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- 이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 `New-AzFunctionApp`의 `-DisableApplicationInsights`가 수정되었습니다.
- PowerShell 6.2는 더 이상 지원되지 않으므로 PowerShell 6.2 함수 앱 생성을 지원하는 기능이 제거되었습니다. 고객을 위한 최신 지침은 PowerShell 7.0 함수 앱을 대신 만드는 것입니다.
- `RuntimeVersion` 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.
- `RuntimeVersion` 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다. 그러나 사용자는 여전히 `-Runtime Node` 및 `-RuntimeVersion 10`을 지정하여 Node 10 함수 앱을 만들 수 있습니다. `RuntimeVersion` 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다. 그러나 사용자는 여전히 `-Runtime Python` 및 `-RuntimeVersion 3.7`을 지정하여 Python 3.7 함수 앱을 만들 수 있습니다.

#### <a name="before"></a>이전

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>이러한

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

`DisableSoftDelete` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>이러한

일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다. 자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

`EnableSoftDelete`, `SoftDeleteRetentionInDays` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>이러한

일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다. 자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

`Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` 형식의 속성 `SecretValueText`가 제거되었습니다. `SecretValueText` 속성이 `SecretValue`로 대체되었습니다.

#### <a name="before"></a>이전

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>이러한

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

`ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>이러한

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

`RegistrationDefinitionName`, `RegistrationDefinitionResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>이러한

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>이러한

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>이러한

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

`ApiVersion` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>이러한

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azdeployment"></a>Get-AzDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="new-azdeployment"></a>New-AzDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="test-azdeployment"></a>Test-AzDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

`Get-AzManagementGroupDeployment`의 경우와 동일합니다.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

`IsAzureADOnlyAuthentication` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>이러한

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

`FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>이러한

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

`Suspend`, `Resume` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

`PrivateLinkResourceType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>이러한

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

`FilterType`, `FilterItem` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.

#### <a name="before"></a>이전

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>After

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
