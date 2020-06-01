---
ms.openlocfilehash: 636fd0432d421f74fa74f3275abbc31ec5dc0b5c
ms.sourcegitcommit: 31f4facf815c2e25dc44e2fde0e1d2bd690bfc54
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/20/2020
ms.locfileid: "83688529"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="6f161-101">Az 4.1.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="6f161-101">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="6f161-102">이 문서에서는 Az 3.0.0에서 4.1.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-102">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="6f161-103">Az 4.1.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="6f161-103">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="6f161-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f161-104">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="6f161-105">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f161-105">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="6f161-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="6f161-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="6f161-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="6f161-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="6f161-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="6f161-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="6f161-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f161-109">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="6f161-110">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f161-110">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="6f161-111">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f161-111">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="6f161-112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f161-112">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="6f161-113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f161-113">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="6f161-114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f161-114">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="6f161-115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f161-115">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="6f161-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="6f161-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="6f161-117">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="6f161-117">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="6f161-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="6f161-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="6f161-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="6f161-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="6f161-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="6f161-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="6f161-121">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f161-121">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="6f161-122">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` 형식의 `Type` 속성이 `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType`에서 `System.String`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-122">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="6f161-123">`New-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-123">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-124">`New-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-124">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="6f161-125">`Set-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-125">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-126">`Set-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-126">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="6f161-127">`Get-AzApiManagementProperty` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-127">The cmdlet `Get-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="6f161-128">`New-AzApiManagementProperty` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-128">The cmdlet `New-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="6f161-129">`Remove-AzApiManagementProperty` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-129">The cmdlet `Remove-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="6f161-130">`Set-AzApiManagementProperty` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-130">The cmdlet `Set-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

## <a name="azbatch"></a><span data-ttu-id="6f161-131">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f161-131">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="6f161-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="6f161-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="6f161-133">`Microsoft.Azure.Commands.Batch.Models.PSApplication` 형식의 속성 `ApplicationPackages`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-133">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="6f161-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="6f161-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="6f161-135">`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` 형식의 `PublicIPs` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-135">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="6f161-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="6f161-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="6f161-137">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` 형식의 `StorageUrlExpiry` 속성이 `System.DateTime`에서 `System.DateTime?`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-137">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="6f161-138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f161-138">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="6f161-139">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-139">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="6f161-140">`Get-AzVMImage` cmdlet이 `FilterExpression` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-140">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-141">`Get-AzVMImage` cmdlet의 `ListVMImage` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-141">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="6f161-142">`New-AzVMConfig` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-142">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-143">`New-AzVMConfig` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-143">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="6f161-144">`Update-AzVM` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-144">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-145">`Update-AzVM` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-145">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="6f161-146">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-146">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6f161-147">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-147">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-148">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-148">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="6f161-149">After</span><span class="sxs-lookup"><span data-stu-id="6f161-149">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="6f161-150">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-150">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6f161-151">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-151">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-152">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-152">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="6f161-153">After</span><span class="sxs-lookup"><span data-stu-id="6f161-153">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="6f161-154">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-154">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6f161-155">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-155">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-156">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-156">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="6f161-157">After</span><span class="sxs-lookup"><span data-stu-id="6f161-157">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="6f161-158">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-158">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="6f161-159">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-159">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="6f161-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="6f161-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="6f161-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="6f161-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="6f161-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="6f161-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="6f161-166">`AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-166">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-167">`AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-167">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-168">`__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-168">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="6f161-169">`ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-169">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="6f161-170">`AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-170">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="6f161-171">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-171">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="6f161-172">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-172">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="6f161-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="6f161-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="6f161-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="6f161-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="6f161-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="6f161-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="6f161-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="6f161-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="6f161-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="6f161-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="6f161-183">`AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-183">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-184">`__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-184">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="6f161-185">`ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-185">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="6f161-186">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-186">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="6f161-187">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-187">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="6f161-188">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f161-188">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="6f161-189">`New-AzKeyVaultCertificateOrganizationDetails` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-189">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="6f161-190">`New-AzKeyVaultCertificateOrganizationDetail`을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6f161-190">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-191">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-191">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="6f161-192">After</span><span class="sxs-lookup"><span data-stu-id="6f161-192">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="6f161-193">`New-AzKeyVaultCertificateAdministratorDetails` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-193">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="6f161-194">`New-AzKeyVaultCertificateAdministratorDetail`을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6f161-194">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-195">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-195">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="6f161-196">After</span><span class="sxs-lookup"><span data-stu-id="6f161-196">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="6f161-197">일시 삭제가 기본적으로 사용되므로 `-EnableSoftDelete`는 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-197">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="6f161-198">이 동작을 원하지 않는 경우 `-DisableSoftDelete`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6f161-198">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-199">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-199">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="6f161-200">After</span><span class="sxs-lookup"><span data-stu-id="6f161-200">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="6f161-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f161-201">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="6f161-202">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-202">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="6f161-203">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-203">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="6f161-204">`New-AzMetricAlertRuleV2Criteria` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-204">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="6f161-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f161-205">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="6f161-206">`RoundTripTimeMs` 속성의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-206">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="6f161-207">`SuccessThresholdRoundTripTimeMs` 매개 변수의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-207">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="6f161-208">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f161-208">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="6f161-209">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-209">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="6f161-210">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-210">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="6f161-211">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="6f161-212">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="6f161-213">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="6f161-214">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="6f161-215">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="6f161-216">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="6f161-217">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="6f161-218">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="6f161-219">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="6f161-220">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="6f161-221">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="6f161-222">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="6f161-223">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="6f161-224">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="6f161-225">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="6f161-226">`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` 형식의 속성 `Metadata`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-226">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="6f161-227">`Get-AzOperationalInsightsSavedSearchResult` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-227">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="6f161-228">`Get-AzOperationalInsightsSearchResult` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-228">The cmdlet `Get-AzOperationalInsightsSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6f161-229">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-229">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6f161-230">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-230">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6f161-231">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6f161-232">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="6f161-233">`Get-AzOperationalInsightsLinkTarget` cmdlet이 제거되었으며 원래 cmdlet 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-233">The cmdlet `Get-AzOperationalInsightsLinkTarget` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="6f161-234">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="6f161-235">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-235">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="6f161-236">`New-AzOperationalInsightsWorkspace` cmdlet이 `CustomerId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-236">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6f161-237">`New-AzOperationalInsightsWorkspace` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-237">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="6f161-238">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-238">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="6f161-239">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-239">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="6f161-240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f161-240">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="6f161-241">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-241">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="6f161-242">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-242">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="6f161-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="6f161-244">`TenantLevel` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-244">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="6f161-245">`Aliases` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-245">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="6f161-246">`New-AzPolicyAssignment` cmdlet은 `PolicyDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-246">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="6f161-247">`New-AzPolicyAssignment` cmdlet은 `PolicySetDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-247">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="6f161-248">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-248">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="6f161-249">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f161-249">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="6f161-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="6f161-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="6f161-251">NetWorkRule DefaultAction 값이 Allow = 1, Deny = 0에서 Allow = 0, Deny = 1로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-251">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="6f161-252">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="6f161-252">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="6f161-253">출력 개체 Get-azurestoragetable. AzureStorageTable.CloudTable.ServiceClient의 2개 속성 ConnectionPolicy 및 ConsistencyLevel이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-253">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="6f161-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="6f161-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="6f161-255">출력 형식을 CloudFile에서 AzureStorageFile로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFile"이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-255">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-256">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-256">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="6f161-257">After</span><span class="sxs-lookup"><span data-stu-id="6f161-257">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="6f161-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="6f161-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="6f161-259">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileDirectory"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-259">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-260">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-260">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="6f161-261">After</span><span class="sxs-lookup"><span data-stu-id="6f161-261">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="6f161-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="6f161-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="6f161-263">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-263">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-264">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-264">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="6f161-265">After</span><span class="sxs-lookup"><span data-stu-id="6f161-265">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="6f161-266">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare.Properties"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-266">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-267">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-267">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="6f161-268">After</span><span class="sxs-lookup"><span data-stu-id="6f161-268">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="6f161-269">부모 디렉터리 개체와 -Path를 사용하여 하위 파일 디렉터리를 제거할 때 형식(문자열)이 일치하는 파이프라인의 -Path를 더 이상 입력할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f161-269">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="6f161-270">이전</span><span class="sxs-lookup"><span data-stu-id="6f161-270">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="6f161-271">After</span><span class="sxs-lookup"><span data-stu-id="6f161-271">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
