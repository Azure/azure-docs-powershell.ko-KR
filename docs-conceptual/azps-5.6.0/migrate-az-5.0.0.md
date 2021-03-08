---
title: Az 5.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 5.0.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872555"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="dfc48-103">Az 5.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="dfc48-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="dfc48-104">이 문서에서는 Az 4.0.0에서 5.0.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="dfc48-105">Az 5.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="dfc48-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="dfc48-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dfc48-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="dfc48-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="dfc48-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="dfc48-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="dfc48-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="dfc48-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dfc48-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="dfc48-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dfc48-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="dfc48-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dfc48-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="dfc48-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="dfc48-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="dfc48-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="dfc48-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="dfc48-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="dfc48-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="dfc48-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="dfc48-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfc48-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="dfc48-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dfc48-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="dfc48-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="dfc48-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="dfc48-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="dfc48-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="dfc48-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="dfc48-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="dfc48-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="dfc48-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="dfc48-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="dfc48-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="dfc48-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="dfc48-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="dfc48-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="dfc48-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="dfc48-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="dfc48-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="dfc48-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="dfc48-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="dfc48-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="dfc48-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="dfc48-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="dfc48-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="dfc48-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="dfc48-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="dfc48-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="dfc48-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="dfc48-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="dfc48-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="dfc48-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="dfc48-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="dfc48-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="dfc48-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="dfc48-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="dfc48-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="dfc48-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="dfc48-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="dfc48-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="dfc48-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="dfc48-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="dfc48-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="dfc48-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="dfc48-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="dfc48-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dfc48-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="dfc48-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="dfc48-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="dfc48-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="dfc48-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="dfc48-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfc48-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="dfc48-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfc48-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="dfc48-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dfc48-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="dfc48-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="dfc48-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="dfc48-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="dfc48-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="dfc48-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="dfc48-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="dfc48-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="dfc48-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dfc48-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="dfc48-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="dfc48-169">New-AzAksCluster</span></span>

- <span data-ttu-id="dfc48-170">`NodeOsType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다. 이는 항상 `Linux`입니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="dfc48-171">`ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="dfc48-172">`NodeVmSetType`의 기본값은 `AvailabilitySet`에서 `VirtualMachineScaleSets`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="dfc48-173">`NetworkPlugin`의 기본값은 `none`에서 `azure`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-174">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-175">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="dfc48-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="dfc48-176">Set-AzAksCluster</span></span>

<span data-ttu-id="dfc48-177">`ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-178">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-179">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="dfc48-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dfc48-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="dfc48-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dfc48-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="dfc48-182">`StorageAccountName` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-183">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="dfc48-184">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-184">After</span></span>

<span data-ttu-id="dfc48-185">`Classic`은 사용되지 않으며 `StorageAccountName`은 Classic Container Registry에서만 작동하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="dfc48-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dfc48-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="dfc48-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="dfc48-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="dfc48-188">`Get-AzFunctionApp` 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 `IncludeSlot` 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="dfc48-189">이제 cmdlet은 `-IncludeSlot`이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="dfc48-190">이전 cmdlet 버전에서는 이 기능이 작동하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="dfc48-191">하지만 이제 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="dfc48-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="dfc48-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="dfc48-193">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 `New-AzFunctionApp`의 `-DisableApplicationInsights`가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="dfc48-194">PowerShell 6.2는 더 이상 지원되지 않으므로 PowerShell 6.2 함수 앱 생성을 지원하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="dfc48-195">고객을 위한 최신 지침은 PowerShell 7.0 함수 앱을 대신 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="dfc48-196">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="dfc48-197">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="dfc48-198">그러나 사용자는 여전히 `-Runtime Node` 및 `-RuntimeVersion 10`을 지정하여 Node 10 함수 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="dfc48-199">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="dfc48-200">그러나 사용자는 여전히 `-Runtime Python` 및 `-RuntimeVersion 3.7`을 지정하여 Python 3.7 함수 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-201">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="dfc48-202">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="dfc48-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="dfc48-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-204">New-AzKeyVault</span></span>

<span data-ttu-id="dfc48-205">`DisableSoftDelete` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-206">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="dfc48-207">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-207">After</span></span>

<span data-ttu-id="dfc48-208">일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="dfc48-209">자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="dfc48-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="dfc48-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dfc48-210">Update-AzKeyVault</span></span>

<span data-ttu-id="dfc48-211">`EnableSoftDelete`, `SoftDeleteRetentionInDays` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-212">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="dfc48-213">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-213">After</span></span>

<span data-ttu-id="dfc48-214">일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="dfc48-215">자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="dfc48-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="dfc48-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dfc48-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="dfc48-217">`Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` 형식의 속성 `SecretValueText`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="dfc48-218">호출에 `-AsPlainText`를 적용하여 일반 텍스트 비밀을 가져오거나 스크립트에 `SecureString` 형식의 `$secret.SecretValue`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-219">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="dfc48-220">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="dfc48-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dfc48-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="dfc48-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="dfc48-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="dfc48-223">`ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-224">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-225">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="dfc48-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="dfc48-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="dfc48-227">`RegistrationDefinitionName`, `RegistrationDefinitionResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-228">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-229">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="dfc48-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="dfc48-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="dfc48-231">`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-232">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-233">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="dfc48-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="dfc48-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="dfc48-235">`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-236">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-237">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="dfc48-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="dfc48-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="dfc48-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="dfc48-240">`ApiVersion` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-241">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-242">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="dfc48-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="dfc48-244">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="dfc48-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-245">Get-AzDeployment</span></span>

<span data-ttu-id="dfc48-246">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="dfc48-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="dfc48-248">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="dfc48-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="dfc48-250">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="dfc48-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="dfc48-252">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="dfc48-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="dfc48-254">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="dfc48-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="dfc48-256">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="dfc48-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-257">New-AzDeployment</span></span>

<span data-ttu-id="dfc48-258">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="dfc48-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="dfc48-260">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="dfc48-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="dfc48-262">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="dfc48-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-263">Remove-AzDeployment</span></span>

<span data-ttu-id="dfc48-264">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="dfc48-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="dfc48-266">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="dfc48-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="dfc48-268">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="dfc48-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="dfc48-270">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="dfc48-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="dfc48-272">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="dfc48-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="dfc48-274">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="dfc48-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-275">Stop-AzDeployment</span></span>

<span data-ttu-id="dfc48-276">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="dfc48-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="dfc48-278">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="dfc48-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="dfc48-280">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="dfc48-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-281">Test-AzDeployment</span></span>

<span data-ttu-id="dfc48-282">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="dfc48-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="dfc48-284">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="dfc48-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="dfc48-286">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="dfc48-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfc48-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="dfc48-288">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="dfc48-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="dfc48-290">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="dfc48-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="dfc48-292">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="dfc48-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="dfc48-294">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="dfc48-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dfc48-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="dfc48-296">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="dfc48-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="dfc48-298">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="dfc48-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dfc48-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="dfc48-300">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="dfc48-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="dfc48-302">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="dfc48-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="dfc48-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="dfc48-304">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="dfc48-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dfc48-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="dfc48-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="dfc48-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="dfc48-307">`IsAzureADOnlyAuthentication` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-308">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="dfc48-309">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="dfc48-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="dfc48-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="dfc48-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfc48-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="dfc48-312">`FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-313">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="dfc48-314">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="dfc48-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfc48-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="dfc48-316">`Suspend`, `Resume` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="dfc48-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dfc48-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="dfc48-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="dfc48-319">`PrivateLinkResourceType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-320">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="dfc48-321">이러한</span><span class="sxs-lookup"><span data-stu-id="dfc48-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="dfc48-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="dfc48-323">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="dfc48-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="dfc48-325">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="dfc48-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="dfc48-327">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="dfc48-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dfc48-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="dfc48-329">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="dfc48-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="dfc48-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="dfc48-331">`FilterType`, `FilterItem` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc48-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="dfc48-332">이전</span><span class="sxs-lookup"><span data-stu-id="dfc48-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="dfc48-333">After</span><span class="sxs-lookup"><span data-stu-id="dfc48-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
