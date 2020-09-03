---
title: Az 4.1.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 4.1.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5f42bbb65313d1caa839443d463b61cc743ca0a5
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242667"
---
# <a name="migration-guide-for-az-410"></a>Az 4.1.0 마이그레이션 가이드

이 문서에서는 Az 3.0.0에서 4.1.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.

- [Az 4.1.0 마이그레이션 가이드](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
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
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
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
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` 형식의 `Type` 속성이 `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType`에서 `System.String`으로 변경되었습니다.

### `New-AzApiManagement`

- `New-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `New-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.

### `Set-AzApiManagement`

- `Set-AzApiManagement` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `Set-AzApiManagement` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.

### `Get-AzApiManagementProperty`

`Get-AzApiManagementProperty` cmdlet이 `Get-AzureApiManagementNamedValue`로 대체되었습니다.

### `New-AzApiManagementProperty`

`New-AzApiManagementProperty` cmdlet이 `New-AzureApiManagementNamedValue`로 대체되었습니다.

### `Remove-AzApiManagementProperty`

`Remove-AzApiManagementProperty` cmdlet이 `Remove-AzureApiManagementNamedValue`로 대체되었습니다.

### `Set-AzApiManagementProperty`

`Set-AzApiManagementProperty` cmdlet이 `Set-AzureApiManagementNamedValue`로 대체되었습니다.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

`Microsoft.Azure.Commands.Batch.Models.PSApplication` 형식의 속성 `ApplicationPackages`가 제거되었습니다.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

`Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` 형식의 `PublicIPs` 속성이 제거되었습니다.

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` 형식의 `StorageUrlExpiry` 속성이 `System.DateTime`에서 `System.DateTime?`으로 변경되었습니다.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Get-AzVMImage`

- `Get-AzVMImage` cmdlet이 `FilterExpression` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `Get-AzVMImage` cmdlet의 `ListVMImage` 매개 변수 세트가 제거되었습니다.

### `New-AzVMConfig`

- `New-AzVMConfig` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `New-AzVMConfig` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.

### `Update-AzVM`

- `Update-AzVM` cmdlet이 `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `Update-AzVM` cmdlet의 `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.

### `New-AzProximityPlacementGroup`

- `VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.

#### <a name="before"></a>이전

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

#### <a name="after"></a>After

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

- `VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.

#### <a name="before"></a>이전

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

#### <a name="after"></a>After

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

- `VirtualMachines`, `VirtualMachineScaleSets` 및 `AvailabilitySets` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`로 변경되었습니다.
- `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 형식의 `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` 및 `AvailabilitySetsColocationStatus` 속성이 제거되었습니다.

#### <a name="before"></a>이전

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

#### <a name="after"></a>After

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

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssDataDisk`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssNetworkInterfaceConfiguration`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssSecret`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssSshPublicKey`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Add-AzVmssWinRMListener`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `New-AzVmssConfig`

- `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.
- `AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `AssignIdentity` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `__AllParameterSets` 매개 변수 세트가 제거되었습니다.
- `ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.
- `AssignIdentityParameterSet` 매개 변수 세트가 제거되었습니다.

### `Remove-AzVmssDataDisk`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Remove-AzVmssExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Remove-AzVmssNetworkInterfaceConfiguration`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Set-AzVmssBootDiagnostic`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Set-AzVmssOsProfile`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Set-AzVmssRollingUpgradePolicy`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Set-AzVmssStorageProfile`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `New-AzVmss`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Repair-AzVmssServiceFabricUpdateDomain`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Get-AzVmss`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Set-AzVmssOrchestrationServiceState`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Update-AzVmss`

- `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.
- `AutomaticRepairMaxInstanceRepairsPercent` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `__AllParameterSets` 매개 변수 세트가 제거되었습니다.
- `ExplicitIdentityParameterSet` 매개 변수 세트가 제거되었습니다.

### `Add-AzVmssDiagnosticsExtension`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

### `Disable-AzVmssDiskEncryption`

`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 형식의 `AutomaticRepairsPolicy` 속성이 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy`에서 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`로 변경되었습니다.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

`New-AzKeyVaultCertificateOrganizationDetails` 별칭이 제거되었습니다. `New-AzKeyVaultCertificateOrganizationDetail`을 사용하세요.

#### <a name="before"></a>이전

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>After

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

`New-AzKeyVaultCertificateAdministratorDetails` 별칭이 제거되었습니다. `New-AzKeyVaultCertificateAdministratorDetail`을 사용하세요.

#### <a name="before"></a>이전

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>After

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

일시 삭제가 기본적으로 사용되므로 `-EnableSoftDelete`는 제거되었습니다. 이 동작을 원하지 않는 경우 `-DisableSoftDelete`를 사용하세요.

#### <a name="before"></a>이전

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>After

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.

### `Get-AzLogProfile`

`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 형식의 `RetentionPolicy` 속성이 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy`에서 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`로 변경되었습니다.

### `New-AzMetricAlertRuleV2Criteria`

`New-AzMetricAlertRuleV2Criteria` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

`RoundTripTimeMs` 속성의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

`SuccessThresholdRoundTripTimeMs` 매개 변수의 제네릭 형식이 `System.Nullable1[System.Int32]`에서 `System.Nullable1[System.Double]`로 변경되었습니다.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsCustomLogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsWindowsEventDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Remove-AzOperationalInsightsDataSource`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Disable-AzOperationalInsightsIISLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Enable-AzOperationalInsightsIISLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Get-AzOperationalInsightsSavedSearch`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` 형식의 속성 `Metadata`가 제거되었습니다.

### `Get-AzOperationalInsightsSavedSearchResult`

`Get-AzOperationalInsightsSavedSearchResult` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.

### `Get-AzOperationalInsightsSearchResult`

`Get-AzOperationalInsightsSearchResult` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.

### `Get-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Remove-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Set-AzOperationalInsightsStorageInsight`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Get-AzOperationalInsightsLinkTarget`

`Get-AzOperationalInsightsLinkTarget` cmdlet은 SDK에서 더 이상 지원되지 않아 제거되었습니다.

### `Get-AzOperationalInsightsWorkspace`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `New-AzOperationalInsightsWorkspace`

- `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.
- `New-AzOperationalInsightsWorkspace` cmdlet이 `CustomerId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.
- `New-AzOperationalInsightsWorkspace` cmdlet의 `__AllParameterSets` 매개 변수 세트가 제거되었습니다.

### `Set-AzOperationalInsightsWorkspace`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

### `Invoke-AzOperationalInsightsQuery`

`Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 형식의 속성 `PortalUrl`가 제거되었습니다.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.

### `Get-AzDeploymentScriptLog`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.

### `Save-AzDeploymentScriptLog`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

`TenantLevel` 매개 변수가 제거되었습니다.

### `Get-AzPolicyAlias`

`Aliases` 속성의 제네릭 형식이 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]`에서 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`로 변경되었습니다.

### `New-AzPolicyAssignment`

- `New-AzPolicyAssignment` cmdlet은 `PolicyDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.
- `New-AzPolicyAssignment` cmdlet은 `PolicySetDefinition` 매개 변수의 `System.Management.Automation.PSObject` 형식을 더 이상 지원하지 않습니다.

### `Remove-AzDeploymentScript`

`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 형식의 `Status` 속성이 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus`에서 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`로 변경되었습니다.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

NetWorkRule DefaultAction 값이 Allow = 1, Deny = 0에서 Allow = 0, Deny = 1로 변경되었습니다.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

출력 개체 Get-azurestoragetable. AzureStorageTable.CloudTable.ServiceClient의 2개 속성 ConnectionPolicy 및 ConsistencyLevel이 제거되었습니다.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

출력 형식을 CloudFile에서 AzureStorageFile로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFile"이 됩니다.

#### <a name="before"></a>이전

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>After

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileDirectory"가 됩니다.

#### <a name="before"></a>이전

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare"가 됩니다.

#### <a name="before"></a>이전

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>After

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경하며, 원래 출력은 새 출력의 자식 속성 "CloudFileShare.Properties"가 됩니다.

#### <a name="before"></a>이전

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>After

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

부모 디렉터리 개체와 -Path를 사용하여 하위 파일 디렉터리를 제거할 때 형식(문자열)이 일치하는 파이프라인의 -Path를 더 이상 입력할 수 없습니다.

#### <a name="before"></a>이전

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
