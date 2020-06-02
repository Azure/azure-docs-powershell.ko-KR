---
title: Az 2.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 2.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 91362f3cc6b35e96a543c1304fb55acbf373d291
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299114"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="86e21-103">Az 2.0.0 마이그레이션 가이드</span><span class="sxs-lookup"><span data-stu-id="86e21-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="86e21-104">이 문서에서는 Az 1.0.0 및 2.0.0 버전 간의 변경 내용에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="86e21-105">목차</span><span class="sxs-lookup"><span data-stu-id="86e21-105">Table of Contents</span></span>
- [<span data-ttu-id="86e21-106">모듈의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="86e21-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="86e21-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86e21-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="86e21-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86e21-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="86e21-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86e21-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="86e21-110">모듈의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="86e21-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="86e21-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86e21-111">Az.Compute</span></span>

- <span data-ttu-id="86e21-112">```Sku = Aligned```를 사용하기 위해 `New-AzAvailabilitySet` 및 `Update-AzAvailabilitySet` cmdlet에서 `Managed` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-113">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-114">After</span><span class="sxs-lookup"><span data-stu-id="86e21-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="86e21-115">일관성을 위해 `Update-AzImage`의 'ByName' 및 'ByResourceId' 매개 변수 집합에서 `Image` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="86e21-116">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-116">Before</span></span>

  <span data-ttu-id="86e21-117">아래 코드는 작동하지만, 전달된 ImageName은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-118">After</span><span class="sxs-lookup"><span data-stu-id="86e21-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="86e21-119">일관성을 위해 `Restart-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="86e21-120">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-120">Before</span></span>

  <span data-ttu-id="86e21-121">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-122">After</span><span class="sxs-lookup"><span data-stu-id="86e21-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="86e21-123">일관성을 위해 `Start-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="86e21-124">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-124">Before</span></span>

  <span data-ttu-id="86e21-125">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-126">After</span><span class="sxs-lookup"><span data-stu-id="86e21-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="86e21-127">일관성을 위해 `Stop-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="86e21-128">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-128">Before</span></span>

  <span data-ttu-id="86e21-129">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-130">After</span><span class="sxs-lookup"><span data-stu-id="86e21-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="86e21-131">일관성을 위해 `Remove-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="86e21-132">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-132">Before</span></span>

  <span data-ttu-id="86e21-133">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-134">After</span><span class="sxs-lookup"><span data-stu-id="86e21-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="86e21-135">일관성을 위해 `Set-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="86e21-136">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-136">Before</span></span>

  <span data-ttu-id="86e21-137">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-138">After</span><span class="sxs-lookup"><span data-stu-id="86e21-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="86e21-139">일관성을 위해 `Save-AzVMImage`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="86e21-140">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-140">Before</span></span>
  <span data-ttu-id="86e21-141">아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="86e21-142">After</span><span class="sxs-lookup"><span data-stu-id="86e21-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="86e21-143">`PSVirtualMachineScaleSetVM`의 `ProtectFromScaleIn` 속성을 캡슐화하기 위해 ProtectionPolicy 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-144">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-145">After</span><span class="sxs-lookup"><span data-stu-id="86e21-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="86e21-146">`PSDisk`의 `EncryptionSettings` 속성을 묶기 위해 ```EncryptionSettingsCollection``` 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-147">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-148">After</span><span class="sxs-lookup"><span data-stu-id="86e21-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="86e21-149">`PSSnapshot`의 `EncryptionSettings` 속성을 묶기 위해 ```EncryptionSettingsCollection``` 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-150">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-151">After</span><span class="sxs-lookup"><span data-stu-id="86e21-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="86e21-152">`PSVirtualMachineScaleSet`에서 `VirtualMachineProfile` 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-153">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-154">After</span><span class="sxs-lookup"><span data-stu-id="86e21-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="86e21-155">`Set-AzVMBootDiagnostic` cmdlet에서 `Set-AzVMBootDiagnostics`에 대한 별칭을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-156">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-156">Before</span></span>

  <span data-ttu-id="86e21-157">사용되지 않는 별칭을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-158">After</span><span class="sxs-lookup"><span data-stu-id="86e21-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="86e21-159">`Export-AzLogAnalyticThrottledRequest` cmdlet에서 `Export-AzLogAnalyticThrottledRequests`에 대한 별칭을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-160">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-160">Before</span></span>

  <span data-ttu-id="86e21-161">사용되지 않는 별칭을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-162">After</span><span class="sxs-lookup"><span data-stu-id="86e21-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="86e21-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86e21-163">Az.HDInsight</span></span>

- <span data-ttu-id="86e21-164">`Grant-AzHDInsightHttpServicesAccess` 및 `Revoke-AzHDInsightHttpServicesAccess` cmdlet을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="86e21-165">HTTP 액세스는 모든 HDInsight 클러스터에서 항상 사용하도록 설정되므로 더 이상 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="86e21-166">새 `Set-AzHDInsightGatewayCredential` cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="86e21-167">이 cmdlet을 사용하여 게이트웨이 HTTP 사용자 이름 및 암호를 변경합니다(`Grant-AzHDInsightHttpServicesAccess` 대체).</span><span class="sxs-lookup"><span data-stu-id="86e21-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="86e21-168">스토리지 키에 대한 세분화된 역할 기반 액세스를 지원하도록 `Get-AzHDInsightJobOutput` cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="86e21-169">HDInsight 클러스터 운영자, 기여자 또는 소유자 역할이 있는 사용자는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="86e21-170">읽기 권한자 역할만 있는 사용자는 `DefaultStorageAccountKey` 매개 변수를 명시적으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="86e21-171">이러한 역할 기반 액세스 변경에 대한 자세한 내용은 [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="86e21-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="86e21-172">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-173">After</span><span class="sxs-lookup"><span data-stu-id="86e21-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="86e21-174">Get-AzHDInsightJobOutput cmdlet에 대한 읽기 권한자 역할만 있는 사용자</span><span class="sxs-lookup"><span data-stu-id="86e21-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="86e21-175">이전</span><span class="sxs-lookup"><span data-stu-id="86e21-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="86e21-176">After</span><span class="sxs-lookup"><span data-stu-id="86e21-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="86e21-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86e21-177">Az.Storage</span></span>

- <span data-ttu-id="86e21-178">Blob, Queue 및 File cmdlet에서 반환된 형식의 네임스페이스를 `Microsoft.WindowsAzure.Storage`에서 `Microsoft.Azure.Storage`로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="86e21-179">이는 기술적으로 호환성이 손상되는 변경 정책에 따른 호환성이 손상되는 변경이 아니지만, 이러한 cmdlet에서 반환되는 개체와 상호 작용하기 위해 Storage .Net SDK의 메서드를 사용하는 코드를 일부 변경해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="86e21-180">예제 1:  Queue에 메시지 추가(CloudQueueMessage 개체 네임스페이스 변경)</span><span class="sxs-lookup"><span data-stu-id="86e21-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="86e21-181">이전:</span><span class="sxs-lookup"><span data-stu-id="86e21-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="86e21-182">이후:</span><span class="sxs-lookup"><span data-stu-id="86e21-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="86e21-183">예제 2:  AccessCondition을 사용하여 Blob/File 특성 가져오기(AccessCondition 개체 네임스페이스 변경)</span><span class="sxs-lookup"><span data-stu-id="86e21-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="86e21-184">이전:</span><span class="sxs-lookup"><span data-stu-id="86e21-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="86e21-185">이후:</span><span class="sxs-lookup"><span data-stu-id="86e21-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="86e21-186">기술적으로 호환성이 손상되는 변경이 아니지만, `New/Get/Set-AzStorageAccount` 변경에서 반환되는 스토리지 계정의 Sku.Name 속성의 출력 차이가 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="86e21-187">(변경되면 출력 및 입력 SkuName이 정렬됩니다.)</span><span class="sxs-lookup"><span data-stu-id="86e21-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="86e21-188">"StandardLRS" -> "Standard_LRS"</span><span class="sxs-lookup"><span data-stu-id="86e21-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="86e21-189">"StandardGRS" -> "Standard_GRS"</span><span class="sxs-lookup"><span data-stu-id="86e21-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="86e21-190">"StandardRAGRS" -> "Standard_RAGRS"</span><span class="sxs-lookup"><span data-stu-id="86e21-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="86e21-191">"StandardZRS" -> "Standard_ZRS"</span><span class="sxs-lookup"><span data-stu-id="86e21-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="86e21-192">"PremiumLRS" -> "Premium_LRS"</span><span class="sxs-lookup"><span data-stu-id="86e21-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="86e21-193">Kind를 지정하지 않고 스토리지 계정을 만들 때의 기본 서비스 동작을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="86e21-194">이전 버전에서는 `Kind`가 지정되지 않은 스토리지 계정을 만들 때 `Storage`라는 스토리지 계정 종류가 사용되었지만, 새 `StorageV2` 버전에서 기본값은 `Kind`입니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="86e21-195">Kind 'Storage'를 사용하여 V1 스토리지 계정을 만들어야 하는 경우 '-Kind Storage' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="86e21-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="86e21-196">예제: 스토리지 계정 만들기(기본 종류 변경)</span><span class="sxs-lookup"><span data-stu-id="86e21-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="86e21-197">이전:</span><span class="sxs-lookup"><span data-stu-id="86e21-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="86e21-198">이후:</span><span class="sxs-lookup"><span data-stu-id="86e21-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
