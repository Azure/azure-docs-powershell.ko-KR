---
title: Az 5.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 5.0.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856430"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="70fe5-103">Az 5.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="70fe5-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="70fe5-104">이 문서에서는 Az 4.0.0에서 5.0.0 버전으로 변경되면서 바뀐 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="70fe5-105">Az 5.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="70fe5-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="70fe5-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="70fe5-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="70fe5-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="70fe5-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="70fe5-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="70fe5-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="70fe5-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70fe5-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="70fe5-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70fe5-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="70fe5-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="70fe5-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="70fe5-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="70fe5-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="70fe5-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="70fe5-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="70fe5-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="70fe5-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="70fe5-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="70fe5-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="70fe5-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="70fe5-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="70fe5-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="70fe5-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="70fe5-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="70fe5-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="70fe5-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="70fe5-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="70fe5-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="70fe5-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="70fe5-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="70fe5-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="70fe5-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="70fe5-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="70fe5-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="70fe5-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="70fe5-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="70fe5-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="70fe5-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="70fe5-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="70fe5-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="70fe5-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="70fe5-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="70fe5-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="70fe5-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="70fe5-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="70fe5-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="70fe5-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="70fe5-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="70fe5-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="70fe5-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="70fe5-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="70fe5-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="70fe5-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="70fe5-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="70fe5-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="70fe5-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="70fe5-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="70fe5-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="70fe5-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="70fe5-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="70fe5-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="70fe5-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="70fe5-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="70fe5-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="70fe5-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70fe5-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="70fe5-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="70fe5-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="70fe5-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="70fe5-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="70fe5-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70fe5-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="70fe5-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70fe5-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="70fe5-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70fe5-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="70fe5-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="70fe5-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="70fe5-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="70fe5-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="70fe5-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="70fe5-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="70fe5-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="70fe5-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="70fe5-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="70fe5-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="70fe5-169">New-AzAksCluster</span></span>

- <span data-ttu-id="70fe5-170">`NodeOsType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다. 이는 항상 `Linux`입니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="70fe5-171">`ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="70fe5-172">`NodeVmSetType`의 기본값은 `AvailabilitySet`에서 `VirtualMachineScaleSets`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="70fe5-173">`NetworkPlugin`의 기본값은 `none`에서 `azure`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-174">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-175">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="70fe5-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="70fe5-176">Set-AzAksCluster</span></span>

<span data-ttu-id="70fe5-177">`ServicePrincipalIdAndSecret` 매개 변수의 `ClientIdAndSecret` 별칭을 더 이상 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-178">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-179">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="70fe5-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70fe5-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="70fe5-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70fe5-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="70fe5-182">`StorageAccountName` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-183">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="70fe5-184">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-184">After</span></span>

<span data-ttu-id="70fe5-185">`Classic`은 사용되지 않으며 `StorageAccountName`은 Classic Container Registry에서만 작동하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="70fe5-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="70fe5-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="70fe5-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="70fe5-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="70fe5-188">`Get-AzFunctionApp` 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 `IncludeSlot` 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="70fe5-189">이제 cmdlet은 `-IncludeSlot`이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="70fe5-190">이전 cmdlet 버전에서는 이 기능이 작동하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="70fe5-191">하지만 이제 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="70fe5-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="70fe5-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="70fe5-193">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 `New-AzFunctionApp`의 `-DisableApplicationInsights`가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="70fe5-194">PowerShell 6.2는 더 이상 지원되지 않으므로 PowerShell 6.2 함수 앱 생성을 지원하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="70fe5-195">고객을 위한 최신 지침은 PowerShell 7.0 함수 앱을 대신 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="70fe5-196">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="70fe5-197">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="70fe5-198">그러나 사용자는 여전히 `-Runtime Node` 및 `-RuntimeVersion 10`을 지정하여 Node 10 함수 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="70fe5-199">`RuntimeVersion` 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="70fe5-200">그러나 사용자는 여전히 `-Runtime Python` 및 `-RuntimeVersion 3.7`을 지정하여 Python 3.7 함수 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-201">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="70fe5-202">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="70fe5-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="70fe5-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-204">New-AzKeyVault</span></span>

<span data-ttu-id="70fe5-205">`DisableSoftDelete` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-206">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="70fe5-207">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-207">After</span></span>

<span data-ttu-id="70fe5-208">일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="70fe5-209">자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="70fe5-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="70fe5-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70fe5-210">Update-AzKeyVault</span></span>

<span data-ttu-id="70fe5-211">`EnableSoftDelete`, `SoftDeleteRetentionInDays` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-212">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="70fe5-213">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-213">After</span></span>

<span data-ttu-id="70fe5-214">일시 삭제 설정을 업데이트하는 기능은 Az.KeyVault 3.0.0에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="70fe5-215">자세한 정보: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="70fe5-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="70fe5-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="70fe5-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="70fe5-217">`Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` 형식의 속성 `SecretValueText`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="70fe5-218">`SecretValueText` 속성이 `SecretValue`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-219">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="70fe5-220">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="70fe5-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="70fe5-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="70fe5-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="70fe5-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="70fe5-223">`ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-224">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-225">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="70fe5-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="70fe5-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="70fe5-227">`RegistrationDefinitionName`, `RegistrationDefinitionResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-228">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-229">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="70fe5-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="70fe5-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="70fe5-231">`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-232">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-233">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="70fe5-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="70fe5-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="70fe5-235">`Id`, `ResourceId` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-236">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-237">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="70fe5-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="70fe5-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="70fe5-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="70fe5-240">`ApiVersion` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-241">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-242">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="70fe5-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="70fe5-244">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="70fe5-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-245">Get-AzDeployment</span></span>

<span data-ttu-id="70fe5-246">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="70fe5-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="70fe5-248">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="70fe5-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="70fe5-250">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="70fe5-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="70fe5-252">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="70fe5-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="70fe5-254">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="70fe5-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="70fe5-256">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="70fe5-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-257">New-AzDeployment</span></span>

<span data-ttu-id="70fe5-258">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="70fe5-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="70fe5-260">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="70fe5-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="70fe5-262">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="70fe5-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-263">Remove-AzDeployment</span></span>

<span data-ttu-id="70fe5-264">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="70fe5-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="70fe5-266">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="70fe5-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="70fe5-268">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="70fe5-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="70fe5-270">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="70fe5-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="70fe5-272">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="70fe5-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="70fe5-274">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="70fe5-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-275">Stop-AzDeployment</span></span>

<span data-ttu-id="70fe5-276">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="70fe5-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="70fe5-278">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="70fe5-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="70fe5-280">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="70fe5-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-281">Test-AzDeployment</span></span>

<span data-ttu-id="70fe5-282">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="70fe5-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="70fe5-284">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="70fe5-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="70fe5-286">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="70fe5-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="70fe5-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="70fe5-288">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="70fe5-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="70fe5-290">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="70fe5-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="70fe5-292">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="70fe5-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="70fe5-294">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="70fe5-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="70fe5-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="70fe5-296">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="70fe5-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="70fe5-298">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="70fe5-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="70fe5-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="70fe5-300">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="70fe5-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="70fe5-302">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="70fe5-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="70fe5-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="70fe5-304">`Get-AzManagementGroupDeployment`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="70fe5-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70fe5-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="70fe5-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="70fe5-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="70fe5-307">`IsAzureADOnlyAuthentication` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-308">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="70fe5-309">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="70fe5-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="70fe5-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="70fe5-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70fe5-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="70fe5-312">`FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-313">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="70fe5-314">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="70fe5-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70fe5-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="70fe5-316">`Suspend`, `Resume` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="70fe5-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70fe5-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="70fe5-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="70fe5-319">`PrivateLinkResourceType` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-320">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="70fe5-321">이러한</span><span class="sxs-lookup"><span data-stu-id="70fe5-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="70fe5-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="70fe5-323">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="70fe5-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="70fe5-325">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="70fe5-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="70fe5-327">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="70fe5-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="70fe5-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="70fe5-329">`Approve-AzPrivateEndpointConnection`의 경우와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="70fe5-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="70fe5-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="70fe5-331">`FilterType`, `FilterItem` 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름의 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70fe5-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="70fe5-332">이전</span><span class="sxs-lookup"><span data-stu-id="70fe5-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="70fe5-333">After</span><span class="sxs-lookup"><span data-stu-id="70fe5-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
