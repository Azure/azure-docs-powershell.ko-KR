---
title: Microsoft Azure PowerShell 4.0.0의 주요 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell 버전 4 릴리스에 이루어진 호환성이 손상되는 변경의 목록이 포함되어 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 47d7ab67a6b1d092bb07405e7dc925d844cac5ab
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386717"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Microsoft Azure PowerShell 4.0.0의 주요 변경 내용

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다. 각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다. 심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.

## <a name="table-of-contents"></a>목차

- [Compute cmdlet의 호환성이 손상되는 변경](#breaking-changes-to-compute-cmdlets)
- [EventHub cmdlet의 주요 변경 내용](#breaking-changes-to-eventhub-cmdlets)
- [Insights cmdlet의 주요 변경 내용](#breaking-changes-to-insights-cmdlets)
- [Network cmdlet의 주요 변경 내용](#breaking-changes-to-network-cmdlets)
- [ServiceBus cmdlet의 주요 변경 내용](#breaking-changes-to-servicebus-cmdlets)
- [Sql cmdlet의 주요 변경 내용](#breaking-changes-to-sql-cmdlets)
- [Storage cmdlet의 주요 변경 내용](#breaking-changes-to-storage-cmdlets)
- [Profile cmdlet의 주요 변경 내용](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>Compute cmdlet의 호환성이 손상되는 변경

이 릴리스에는 다음과 같은 출력 형식이 적용됩니다.

### <a name="psvirtualmachine"></a>PSVirtualMachine
- `PSVirtualMachine` 개체의 최상위 수준 속성 `DataDiskNames` 및 `NetworkInterfaceIDs`가 출력 형식에서 제거되었습니다. 이러한 속성은 `PSVirtualMachine` 개체의 `StorageProfile` 및 `NetworkProfile` 속성에서 항상 사용 가능하며 앞으로 액세스하는 데 필요한 방법이 될 것입니다.
- 이 변경 사항은 다음 cmdlet에 적용됩니다.
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- 속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- 속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.

## <a name="breaking-changes-to-insights-cmdlets"></a>Insights cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- 이 cmdlet은 더 이상 사용되지 않습니다.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- 이 cmdlet의 출력이 단일 개체가 있는 목록에서 단일 개체로 변경되었습니다. 이 개체는 요청 ID와 상태 코드를 포함합니다.
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- 이 cmdlet은 더 이상 사용되지 않습니다.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- 이 cmdlet의 출력(개체 목록)의 각 요소는 평면화되어 `{ Id, Location, Name, Tags, Properties }` 구조의 개체를 반환하는 대신 `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` 구조의 개체를 반환합니다. 이 개체는 Azure 리소스의 모든 특성과 최상위 수준에 있는 AlertRuleResource의 모든 특성을 포함합니다.
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- `AutoscaleSettingResourceName` 필드는 항상 `Name` 필드와 동일한 값을 포함하므로 더 이상 사용되지 않습니다.

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- 이 cmdlet의 출력이 `Boolean`에서 `RequestId` 및 `StatusCode`를 포함하는 개체로 변경됩니다.

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- 이 cmdlet의 출력이 요청 ID, 상태 코드를 포함하는 개체에서, 업데이트되거나 새로 만든 리소스로 변경됩니다.
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- 이 명령은 `Update-AzureRmDiagnosticSettings`로 이름이 변경됩니다.

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Network cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- `EnableBgp` 매개 변수가 `string` 대신 `boolean`을 사용하도록 변경되었습니다.

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- 속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- 속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.

## <a name="breaking-changes-to-sql-cmdlets"></a>Sql cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- `Tag` 매개 변수가 제거되었습니다.
- `GracePeriodWithDataLossHour` 매개 변수의 이름이 `GracePeriodWithDataLossHours`로 변경되었습니다.

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- `Tag` 매개 변수가 제거되었습니다.
- `GracePeriodWithDataLossHour` 매개 변수의 이름이 `GracePeriodWithDataLossHours`로 변경되었습니다.

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- `Tag` 매개 변수가 제거되었습니다.

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- `Tag` 매개 변수가 제거되었습니다.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- `PartnerResourceGroupName` 매개 변수가 제거되었습니다.
- `PartnerServerName` 매개 변수가 제거되었습니다.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- 값 `Usage_Anomaly`가 매개 변수 `ExcludedDetectionType`에 대해 더 이상 유효하지 않습니다.

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- 값 `Usage_Anomaly`가 매개 변수 `ExcludedDetectionType`에 대해 더 이상 유효하지 않습니다.

## <a name="breaking-changes-to-storage-cmdlets"></a>Storage cmdlet의 주요 변경 내용

이 릴리스에는 다음과 같은 출력 형식 속성이 적용됩니다.

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- 이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 이 변경 사항은 다음 cmdlet에 적용됩니다.
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- 이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 이 변경 사항은 다음 cmdlet에 적용됩니다.
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- 이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- 이 변경 사항은 다음 cmdlet에 적용됩니다.
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- 이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- 이 변경 사항은 다음 cmdlet에 적용됩니다.
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>Profile cmdlet의 주요 변경 내용

이 릴리스에서는 다음 cmdlet 및 cmdlet 출력 형식이 변경되었습니다.

### <a name="add-azurermaccount-breaking-changes"></a>Add-AzureRmAccount 주요 변경 내용

- ```EnvironmentName``` 매개 변수가 제거되고 ```Environment```로 대체되었으며 이제 ```Environment```는 ```AzureEnvironment``` 개체가 아닌 문자열을 사용합니다.

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile의 이름이 Import-AzureRmContext로 바뀌었습니다.

```Select-AzureRmProfile```의 이름이 ```Import-AzureRmContext```로 바뀌었습니다.

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile의 이름이 Save-AzureRmContext로 바뀌었습니다.

```Save-AzureRmProfile```의 이름이 ```Save-AzureRmContext```로 바뀌었습니다.

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>출력 PSAzureContext 형식의 주요 변경 내용

- ```TokenCache``` 속성이 ```byte[]``` 대신 ```IAzureTokenCache```를 구현하는 형식으로 변경되었습니다.

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>출력 PSAzureAccount 형식의 주요 변경 내용

- ```AccountType``` 속성이 ```Type```로 변경되었습니다.

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>출력 PSAzureSubscription 형식의 주요 변경 내용
- ```SubscriptionId``` 속성이 ```Id```로 변경되었습니다.

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- ```SubscriptionName``` 속성이 ```Name```로 변경되었습니다.

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>출력 PSAzureTenant 형식의 주요 변경 내용

- ```TenantId``` 속성이 ```Id```로 변경되었습니다.

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- ```Domain``` 속성이 ```Directory```로 변경되었습니다.

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
