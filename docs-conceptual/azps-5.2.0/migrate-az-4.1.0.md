---
title: Az 4.1.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 4.1.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: fe4a2a7c2f1b171b530eef41ac072b2029be1026
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856777"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="15f0f-103">Az 4.1.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="15f0f-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="15f0f-104">이 문서에서는 Az 3.0.0에서 4.1.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="15f0f-105">Az 4.1.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="15f0f-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="15f0f-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="15f0f-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="15f0f-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="15f0f-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="15f0f-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="15f0f-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="15f0f-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="15f0f-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="15f0f-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="15f0f-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="15f0f-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15f0f-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="15f0f-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15f0f-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="15f0f-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="15f0f-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="15f0f-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15f0f-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="15f0f-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="15f0f-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="15f0f-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15f0f-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="15f0f-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15f0f-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="15f0f-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="15f0f-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="15f0f-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="15f0f-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="15f0f-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="15f0f-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="15f0f-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="15f0f-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="15f0f-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="15f0f-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="15f0f-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="15f0f-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="15f0f-124">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` 형식의 `Type` 속성이 `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType`에서 `System.String`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="15f0f-125">`New-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-126">`New-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="15f0f-127">`Set-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-128">`Set-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="15f0f-129">`Get-AzApiManagementProperty` cmdlet이 `Get-AzApiManagementNamedValue`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="15f0f-130">`New-AzApiManagementProperty` cmdlet이 `New-AzApiManagementNamedValue`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="15f0f-131">`Remove-AzApiManagementProperty` cmdlet이 `Remove-AzApiManagementNamedValue`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="15f0f-132">`Set-AzApiManagementProperty` cmdlet이 `Set-AzApiManagementNamedValue`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="15f0f-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="15f0f-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="15f0f-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="15f0f-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="15f0f-135">`Microsoft.Azure.Commands.Batch.Models.PSApplication` 형식의 속성 `ApplicationPackages`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="15f0f-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="15f0f-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="15f0f-137">`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` 형식의 `PublicIPs` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="15f0f-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="15f0f-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="15f0f-139">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` 형식의 `StorageUrlExpiry` 속성이 `System.DateTime`에서 `System.DateTime?`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="15f0f-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15f0f-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="15f0f-141">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="15f0f-142">`Get-AzVMImage` cmdlet이 `FilterExpression` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-143">`Get-AzVMImage` cmdlet의 `ListVMImage` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="15f0f-144">`New-AzVMConfig` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-145">`New-AzVMConfig` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="15f0f-146">`Update-AzVM` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-147">`Update-AzVM` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="15f0f-148">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="15f0f-149">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-150">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="15f0f-151">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-151">After</span></span>

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

- <span data-ttu-id="15f0f-152">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="15f0f-153">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-154">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="15f0f-155">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-155">After</span></span>

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

- <span data-ttu-id="15f0f-156">`VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="15f0f-157">`Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-158">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="15f0f-159">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-159">After</span></span>

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

<span data-ttu-id="15f0f-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="15f0f-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="15f0f-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="15f0f-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="15f0f-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="15f0f-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="15f0f-166">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="15f0f-167">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="15f0f-168">`AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-169">`AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-170">`__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="15f0f-171">`ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="15f0f-172">`AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="15f0f-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="15f0f-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="15f0f-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="15f0f-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="15f0f-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="15f0f-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="15f0f-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="15f0f-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="15f0f-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="15f0f-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="15f0f-183">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="15f0f-184">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="15f0f-185">`AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-186">`__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="15f0f-187">`ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="15f0f-188">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="15f0f-189">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="15f0f-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15f0f-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="15f0f-191">`New-AzKeyVaultCertificateOrganizationDetails` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="15f0f-192">`New-AzKeyVaultCertificateOrganizationDetail`을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="15f0f-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-193">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="15f0f-194">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="15f0f-195">`New-AzKeyVaultCertificateAdministratorDetails` 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="15f0f-196">`New-AzKeyVaultCertificateAdministratorDetail`을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="15f0f-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-197">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="15f0f-198">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="15f0f-199">일시 삭제가 기본적으로 사용되므로 `-EnableSoftDelete`는 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="15f0f-200">이 동작을 원하지 않는 경우 `-DisableSoftDelete`를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="15f0f-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-201">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="15f0f-202">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="15f0f-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="15f0f-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="15f0f-204">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="15f0f-205">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="15f0f-206">`New-AzMetricAlertRuleV2Criteria` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="15f0f-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15f0f-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="15f0f-208">`RoundTripTimeMs` 속성의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="15f0f-209">`SuccessThresholdRoundTripTimeMs` 매개 변수의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="15f0f-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="15f0f-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="15f0f-211">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="15f0f-212">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="15f0f-213">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="15f0f-214">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="15f0f-215">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="15f0f-216">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="15f0f-217">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="15f0f-218">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="15f0f-219">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="15f0f-220">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="15f0f-221">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="15f0f-222">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="15f0f-223">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="15f0f-224">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="15f0f-225">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="15f0f-226">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="15f0f-227">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="15f0f-228">`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` 형식의 속성 `Metadata`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="15f0f-229">`Get-AzOperationalInsightsSavedSearchResult` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="15f0f-230">`Get-AzOperationalInsightsSearchResult` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="15f0f-231">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="15f0f-232">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="15f0f-233">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="15f0f-234">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="15f0f-235">`Get-AzOperationalInsightsLinkTarget` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="15f0f-236">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="15f0f-237">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="15f0f-238">`New-AzOperationalInsightsWorkspace` cmdlet이 `CustomerId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="15f0f-239">`New-AzOperationalInsightsWorkspace` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="15f0f-240">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="15f0f-241">`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="15f0f-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15f0f-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="15f0f-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="15f0f-244">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="15f0f-245">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="15f0f-246">`TenantLevel` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="15f0f-247">`Aliases` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="15f0f-248">`New-AzPolicyAssignment` cmdlet은 `PolicyDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="15f0f-249">`New-AzPolicyAssignment` cmdlet은 `PolicySetDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="15f0f-250">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="15f0f-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15f0f-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="15f0f-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="15f0f-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="15f0f-253">NetWorkRule DefaultAction 값이 Allow = 1, Deny = 0에서 Allow = 0, Deny = 1로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="15f0f-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="15f0f-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="15f0f-255">출력 개체 Get-azurestoragetable. AzureStorageTable.CloudTable.ServiceClient의 2개 속성 ConnectionPolicy 및 ConsistencyLevel이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="15f0f-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="15f0f-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="15f0f-257">출력 형식을 CloudFile에서 AzureStorageFile로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFile"이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-258">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="15f0f-259">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="15f0f-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="15f0f-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="15f0f-261">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileDirectory"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-262">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="15f0f-263">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="15f0f-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="15f0f-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="15f0f-265">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-266">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="15f0f-267">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="15f0f-268">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare.Properties"가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-269">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="15f0f-270">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-270">After</span></span>

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

<span data-ttu-id="15f0f-271">부모 디렉터리 개체와 -Path를 사용하여 하위 파일 디렉터리를 제거할 때 형식(문자열)이 일치하는 파이프라인의 -Path를 더 이상 입력할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15f0f-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="15f0f-272">이전</span><span class="sxs-lookup"><span data-stu-id="15f0f-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="15f0f-273">After</span><span class="sxs-lookup"><span data-stu-id="15f0f-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
