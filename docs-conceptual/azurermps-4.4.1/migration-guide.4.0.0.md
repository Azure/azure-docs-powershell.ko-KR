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
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="95fcf-103">Microsoft Azure PowerShell 4.0.0의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="95fcf-104">이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="95fcf-105">각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="95fcf-106">심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95fcf-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="95fcf-107">목차</span><span class="sxs-lookup"><span data-stu-id="95fcf-107">Table of Contents</span></span>

- [<span data-ttu-id="95fcf-108">Compute cmdlet의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="95fcf-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="95fcf-109">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="95fcf-110">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="95fcf-111">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="95fcf-112">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="95fcf-113">Sql cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="95fcf-114">Storage cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="95fcf-115">Profile cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="95fcf-116">Compute cmdlet의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="95fcf-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="95fcf-117">이 릴리스에는 다음과 같은 출력 형식이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="95fcf-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95fcf-118">PSVirtualMachine</span></span>
- <span data-ttu-id="95fcf-119">`PSVirtualMachine` 개체의 최상위 수준 속성 `DataDiskNames` 및 `NetworkInterfaceIDs`가 출력 형식에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="95fcf-120">이러한 속성은 `PSVirtualMachine` 개체의 `StorageProfile` 및 `NetworkProfile` 속성에서 항상 사용 가능하며 앞으로 액세스하는 데 필요한 방법이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="95fcf-121">이 변경 사항은 다음 cmdlet에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-121">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="95fcf-122">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="95fcf-123">이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="95fcf-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="95fcf-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="95fcf-125">속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="95fcf-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="95fcf-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="95fcf-127">속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="95fcf-128">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="95fcf-129">이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="95fcf-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="95fcf-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="95fcf-131">이 cmdlet은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="95fcf-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="95fcf-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="95fcf-133">이 cmdlet의 출력이 단일 개체가 있는 목록에서 단일 개체로 변경되었습니다. 이 개체는 요청 ID와 상태 코드를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="95fcf-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="95fcf-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="95fcf-135">이 cmdlet은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="95fcf-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="95fcf-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="95fcf-137">이 cmdlet의 출력(개체 목록)의 각 요소는 평면화되어 `{ Id, Location, Name, Tags, Properties }` 구조의 개체를 반환하는 대신 `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` 구조의 개체를 반환합니다. 이 개체는 Azure 리소스의 모든 특성과 최상위 수준에 있는 AlertRuleResource의 모든 특성을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="95fcf-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="95fcf-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="95fcf-139">`AutoscaleSettingResourceName` 필드는 항상 `Name` 필드와 동일한 값을 포함하므로 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="95fcf-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="95fcf-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="95fcf-141">이 cmdlet의 출력이 `Boolean`에서 `RequestId` 및 `StatusCode`를 포함하는 개체로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="95fcf-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="95fcf-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="95fcf-143">이 cmdlet의 출력이 요청 ID, 상태 코드를 포함하는 개체에서, 업데이트되거나 새로 만든 리소스로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
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
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="95fcf-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="95fcf-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="95fcf-145">이 명령은 `Update-AzureRmDiagnosticSettings`로 이름이 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="95fcf-146">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="95fcf-147">이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="95fcf-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95fcf-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="95fcf-149">`EnableBgp` 매개 변수가 `string` 대신 `boolean`을 사용하도록 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="95fcf-150">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="95fcf-151">이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="95fcf-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="95fcf-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="95fcf-153">속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="95fcf-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="95fcf-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="95fcf-155">속성 `ResourceGroupName`이 출력 형식 `NamespaceAttributes`에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="95fcf-156">Sql cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="95fcf-157">이 릴리스에는 다음과 같은 cmdlet이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="95fcf-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95fcf-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="95fcf-159">`Tag` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="95fcf-160">`GracePeriodWithDataLossHour` 매개 변수의 이름이 `GracePeriodWithDataLossHours`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="95fcf-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95fcf-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="95fcf-162">`Tag` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="95fcf-163">`GracePeriodWithDataLossHour` 매개 변수의 이름이 `GracePeriodWithDataLossHours`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="95fcf-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95fcf-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="95fcf-165">`Tag` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="95fcf-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95fcf-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="95fcf-167">`Tag` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="95fcf-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="95fcf-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="95fcf-169">`PartnerResourceGroupName` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="95fcf-170">`PartnerServerName` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="95fcf-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fcf-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="95fcf-172">값 `Usage_Anomaly`가 매개 변수 `ExcludedDetectionType`에 대해 더 이상 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="95fcf-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fcf-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="95fcf-174">값 `Usage_Anomaly`가 매개 변수 `ExcludedDetectionType`에 대해 더 이상 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="95fcf-175">Storage cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="95fcf-176">이 릴리스에는 다음과 같은 출력 형식 속성이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="95fcf-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="95fcf-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="95fcf-178">이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="95fcf-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="95fcf-179">이 변경 사항은 다음 cmdlet에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="95fcf-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="95fcf-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="95fcf-181">이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="95fcf-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="95fcf-182">이 변경 사항은 다음 cmdlet에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="95fcf-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="95fcf-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="95fcf-184">이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="95fcf-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="95fcf-185">이 변경 사항은 다음 cmdlet에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="95fcf-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="95fcf-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="95fcf-187">이 형식에서 다음과 같은 속성이 제거되었습니다(_참고_: `DefaultRequestOptions` 속성에서 확인할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="95fcf-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="95fcf-188">이 변경 사항은 다음 cmdlet에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-188">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="95fcf-189">Profile cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="95fcf-190">이 릴리스에서는 다음 cmdlet 및 cmdlet 출력 형식이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="95fcf-191">Add-AzureRmAccount 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="95fcf-192">```EnvironmentName``` 매개 변수가 제거되고 ```Environment```로 대체되었으며 이제 ```Environment```는 ```AzureEnvironment``` 개체가 아닌 문자열을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="95fcf-193">Select-AzureRmProfile의 이름이 Import-AzureRmContext로 바뀌었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="95fcf-194">```Select-AzureRmProfile```의 이름이 ```Import-AzureRmContext```로 바뀌었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="95fcf-195">Save-AzureRmProfile의 이름이 Save-AzureRmContext로 바뀌었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="95fcf-196">```Save-AzureRmProfile```의 이름이 ```Save-AzureRmContext```로 바뀌었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="95fcf-197">출력 PSAzureContext 형식의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="95fcf-198">```TokenCache``` 속성이 ```byte[]``` 대신 ```IAzureTokenCache```를 구현하는 형식으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="95fcf-199">출력 PSAzureAccount 형식의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="95fcf-200">```AccountType``` 속성이 ```Type```로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-200">The ```AccountType``` property was changed to ```Type```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="95fcf-201">출력 PSAzureSubscription 형식의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="95fcf-202">```SubscriptionId``` 속성이 ```Id```로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="95fcf-203">```SubscriptionName``` 속성이 ```Name```로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="95fcf-204">출력 PSAzureTenant 형식의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="95fcf-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="95fcf-205">```TenantId``` 속성이 ```Id```로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-205">The ```TenantId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="95fcf-206">```Domain``` 속성이 ```Directory```로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="95fcf-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
