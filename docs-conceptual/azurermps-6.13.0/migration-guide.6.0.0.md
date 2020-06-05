---
title: Microsoft Azure PowerShell 6.0.0의 주요 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell 버전 6 릴리스의 주요 변경 내용에 대한 목록이 포함되어 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: ab20dd07fb0c14d8066ad12185f8245be291e7ec
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122245"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="5d98f-103">Microsoft Azure PowerShell 6.0.0의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="5d98f-104">이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5d98f-105">각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="5d98f-106">심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5d98f-107">목차</span><span class="sxs-lookup"><span data-stu-id="5d98f-107">Table of Contents</span></span>

- [<span data-ttu-id="5d98f-108">일반적인 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="5d98f-109">요구되는 최소 PowerShell 버전이 5.0으로 향상됨</span><span class="sxs-lookup"><span data-stu-id="5d98f-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
  - [<span data-ttu-id="5d98f-110">기본적으로 사용되는 컨텍스트 자동 저장</span><span class="sxs-lookup"><span data-stu-id="5d98f-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
  - [<span data-ttu-id="5d98f-111">태그 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="5d98f-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="5d98f-112">AzureRM.Compute cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="5d98f-113">AzureRM.DataLakeStore cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="5d98f-114">AzureRM.Dns cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="5d98f-115">AzureRM.Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="5d98f-116">AzureRM.KeyVault cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="5d98f-117">AzureRM.Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="5d98f-118">AzureRM.RedisCache cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="5d98f-119">AzureRM.Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="5d98f-120">AzureRM.Storage cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="5d98f-121">제거된 모듈</span><span class="sxs-lookup"><span data-stu-id="5d98f-121">Removed modules</span></span>](#removed-modules)
  - [`AzureRM.ServerManagement`](#azurermservermanagement)
  - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="5d98f-122">일반적인 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="5d98f-123">요구되는 최소 PowerShell 버전이 5.0으로 향상됨</span><span class="sxs-lookup"><span data-stu-id="5d98f-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="5d98f-124">이전에는 Azure PowerShell에서 모든 cmdlet을 실행하는 데 PowerShell 버전3.0 _이상_이 필요했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="5d98f-125">앞으로 이 요구 사항은 PowerShell 버전 5.0으로 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="5d98f-126">PowerShell 5.0으로 업그레이드하는 방법에 대한 자세한 내용은 [이 표](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-126">For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="5d98f-127">기본적으로 사용되는 컨텍스트 자동 저장</span><span class="sxs-lookup"><span data-stu-id="5d98f-127">Context autosave enabled by default</span></span>

<span data-ttu-id="5d98f-128">컨텍스트 자동 저장은 새 PowerShell 세션과 다른 PowerShell 세션 간에 사용할 수 있는 Azure 로그인 정보의 스토리지입니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="5d98f-129">컨텍스트 자동 저장에 대한 자세한 내용은 [이 문서](/powershell/azure/context-persistence)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-129">For more information on context autosave, please see [this document](/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="5d98f-130">이전에는 컨텍스트 자동 저장이 기본적으로 비활성화되었으므로 먼저 `Enable-AzureRmContextAutosave` cmdlet을 실행하여 컨텍스트 지속성을 설정해야 세션 간에 사용자의 Azure 인증 정보를 저장할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="5d98f-131">앞으로 컨텍스트 자동 저장은 기본적으로 사용하도록 설정됩니다. 즉, _저장된 컨텍스트 자동 저장 설정이 없는_ 사용자는 다음에 로그인할 때 컨텍스트가 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="5d98f-132">사용자는 `Disable-AzureRmContextAutosave` cmdlet을 사용하여 이 기능을 사용하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

> [!NOTE]
> <span data-ttu-id="5d98f-133">이전에 컨텍스트 자동 저장이 설정되지 않은 사용자 또는 컨텍스트 자동 저장이 설정된 사용자 및 기존 컨텍스트는 이 변경으로 인해 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-133">Users who previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change.</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="5d98f-134">태그 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="5d98f-134">Removal of Tags alias</span></span>

<span data-ttu-id="5d98f-135">`Tag` 매개 변수에 대한 `Tags` 별칭은 많은 cmdlet에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="5d98f-136">이 변경으로 인해 영향을 받는 모듈 및 해당 cmdlet에 대한 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

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

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="5d98f-137">AzureRM.Compute cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="5d98f-138">**기타**</span><span class="sxs-lookup"><span data-stu-id="5d98f-138">**Miscellaneous**</span></span>

- <span data-ttu-id="5d98f-139">`PSDisk` 및 `PSSnapshot` 형식에 중첩된 SKU 이름 속성이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="5d98f-140">`PSVirtualMachine`, `PSVirtualMachineScaleSet` 및 `PSImage` 형식에 중첩된 스토리지 계정 유형 속성이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="5d98f-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-141">**Add-AzureRmImageDataDisk**</span></span>

- <span data-ttu-id="5d98f-142">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-143">**Add-AzureRmVMDataDisk**</span></span>

- <span data-ttu-id="5d98f-144">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-145">**Add-AzureRmVmssDataDisk**</span></span>

- <span data-ttu-id="5d98f-146">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="5d98f-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="5d98f-148">`Managed` 매개 변수가 `Sku`을 위해 제거되었습니다</span><span class="sxs-lookup"><span data-stu-id="5d98f-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="5d98f-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="5d98f-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="5d98f-150">`SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="5d98f-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="5d98f-152">`SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="5d98f-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="5d98f-154">`SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="5d98f-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="5d98f-156">`SkuName` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="5d98f-158">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="5d98f-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="5d98f-160">`DisableWAD` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="5d98f-161">Windows Azure Diagnostics는 기본적으로 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="5d98f-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="5d98f-163">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="5d98f-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="5d98f-165">`StorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="5d98f-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="5d98f-167">`ManagedDisk` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5d98f-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="5d98f-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="5d98f-169">`ManagedDiskStorageAccountType` 매개 변수에 허용되는 값이 각각 `StandardLRS` 및 `PremiumLRS`에서 `Standard_LRS` 및 `Premium_LRS`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="5d98f-170">AzureRM.DataLakeStore cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="5d98f-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5d98f-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5d98f-172">`PerFileThreadCount` 및 `ConcurrentFileCount` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="5d98f-173">앞으로 `Concurrency` 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="5d98f-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5d98f-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5d98f-175">`PerFileThreadCount` 및 `ConcurrentFileCount` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="5d98f-176">앞으로 `Concurrency` 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="5d98f-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5d98f-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5d98f-178">`Clean` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-178">Parameter `Clean` was removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="5d98f-179">AzureRM.Dns cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="5d98f-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="5d98f-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="5d98f-181">`Force` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="5d98f-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="5d98f-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="5d98f-183">`Force` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="5d98f-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="5d98f-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="5d98f-185">`Force` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="5d98f-186">AzureRM.Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="5d98f-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="5d98f-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="5d98f-188">`AutoscaleProfiles` 및 `Notifications` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="5d98f-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="5d98f-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="5d98f-190">`Categories` 및 `Locations` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="5d98f-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5d98f-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="5d98f-192">`Actions` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="5d98f-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5d98f-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="5d98f-194">`Actions` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="5d98f-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="5d98f-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="5d98f-196">`MaxRecords` 및 `MaxEvents` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="5d98f-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="5d98f-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="5d98f-198">`MetricNames` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="5d98f-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="5d98f-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="5d98f-200">`CustomEmails` 및 `SendToServiceOwners` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="5d98f-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="5d98f-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="5d98f-202">`Properties` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="5d98f-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="5d98f-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="5d98f-204">`CustomEmails`, `SendEmailToSubscriptionCoAdministrators` 및 `Webhooks` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="5d98f-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="5d98f-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="5d98f-206">`Rules`, `ScheduleDays`, `ScheduleHours` 및 `ScheduleMinutes` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="5d98f-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="5d98f-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="5d98f-208">`Properties` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="5d98f-209">AzureRM.KeyVault cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="5d98f-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="5d98f-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="5d98f-211">`CertificatePolicy` 매개 변수가 필수 항목이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="5d98f-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="5d98f-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="5d98f-213">액세스 토큰을 구성하는 개별 매개 변수는 더 이상 허용되지 않습니다. 대신 명시적 토큰 매개 변수(예: `Service` 또는 `Permissions`)를 다른 곳에 정의된 액세스 토큰 샘플에 해당하는 제네릭 `TemplateUri` 매개 변수(아마도 Storage PowerShell cmdlet을 사용하거나 Storage 설명서에 따라 수동으로 구성됨)로 바꿉니다. `ValidityPeriod` 매개 변수는 계속 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="5d98f-214">Azure Storage에 대한 공유 액세스 토큰 구성에 대한 자세한 내용은 다음의 각 설명서 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d98f-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>

- [<span data-ttu-id="5d98f-215">서비스 SAS 생성(영문)</span><span class="sxs-lookup"><span data-stu-id="5d98f-215">Constructing a Service SAS</span></span>](/rest/api/storageservices/Constructing-a-Service-SAS)
- [<span data-ttu-id="5d98f-216">계정 SAS 생성(영문)</span><span class="sxs-lookup"><span data-stu-id="5d98f-216">Constructing an Account SAS</span></span>](/rest/api/storageservices/constructing-an-account-sas)

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

<span data-ttu-id="5d98f-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="5d98f-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="5d98f-218">`IssuerProvider` 매개 변수가 필수 항목이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="5d98f-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="5d98f-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="5d98f-220">이 cmdlet의 출력이 `CertificateBundle`에서 `PSKeyVaultCertificate`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="5d98f-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="5d98f-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="5d98f-222">`ResourceGroupName`은 `InputObject` 매개 변수 집합에서 제거되었으며, 대신 `InputObject` 매개 변수의 `ResourceId` 속성에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="5d98f-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="5d98f-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="5d98f-224">`all` 권한이 `PermissionsToKeys`, `PermissionsToSecrets` 및 `PermissionsToCertificates`에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="5d98f-225">**일반**</span><span class="sxs-lookup"><span data-stu-id="5d98f-225">**General**</span></span>
- <span data-ttu-id="5d98f-226">`ValueFromPipelineByPropertyName` 속성이 `InputObject`에 의한 파이핑을 사용하도록 설정된 모든 cmdlet에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span> <span data-ttu-id="5d98f-227">영향을 받는 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-227">The cmdlets affected are:</span></span>
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

- <span data-ttu-id="5d98f-228">`ConfirmImpact` 수준이 모든 cmdlet에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="5d98f-229">영향을 받는 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-229">The cmdlets affected are:</span></span>
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

- <span data-ttu-id="5d98f-230">`IKeyVaultDataServiceClient`가 업데이트되어 모든 Certificate 작업에서 SDK 형식 대신 PSType을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="5d98f-231">다음 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-231">This includes:</span></span>
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

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="5d98f-232">AzureRM.Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="5d98f-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5d98f-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5d98f-234">`ProbeEnabled` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="5d98f-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="5d98f-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="5d98f-236">`AlloowGatewayTransit` 매개 변수 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="5d98f-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5d98f-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5d98f-238">`ProbeEnabled` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="5d98f-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5d98f-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5d98f-240">`ProbeEnabled` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="5d98f-241">AzureRM.RedisCache cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="5d98f-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="5d98f-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="5d98f-243">`Subnet` 및 `VirtualNetwork` 매개 변수가 `SubnetId`를 위해 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="5d98f-244">`RedisVersion` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="5d98f-245">`MaxMemoryPolicy` 매개 변수가 `RedisConfiguration`을 위해 제거되었습니다</span><span class="sxs-lookup"><span data-stu-id="5d98f-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="5d98f-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="5d98f-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="5d98f-247">`MaxMemoryPolicy` 매개 변수가 `RedisConfiguration`을 위해 제거되었습니다</span><span class="sxs-lookup"><span data-stu-id="5d98f-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="5d98f-248">AzureRM.Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="5d98f-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="5d98f-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="5d98f-250">이 cmdlet은 제거되었으며, 해당 기능이 `Get-AzureRmResource`으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="5d98f-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="5d98f-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="5d98f-252">이 cmdlet은 제거되었으며, 해당 기능이 `Get-AzureRmResourceGroup`으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

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

<span data-ttu-id="5d98f-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="5d98f-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="5d98f-254">`AtScopeAndBelow` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="5d98f-255">AzureRM.Storage cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d98f-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="5d98f-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="5d98f-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="5d98f-257">`EnableEncryptionService` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="5d98f-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="5d98f-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="5d98f-259">`EnableEncryptionService` 및 `DisableEncryptionService` 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="5d98f-260">제거된 모듈</span><span class="sxs-lookup"><span data-stu-id="5d98f-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="5d98f-261">서버 관리 도구 서비스가 [작년에 사용 중지](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)되어 SMT에 해당하는 `AzureRM.ServerManagement` 모듈이 `AzureRM`에서 제거되었으며, 앞으로 제공되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="5d98f-262">`AzureRM.SiteRecovery` 모듈은 `AzureRM.SiteRecovery` 모듈의 기능 상위 집합이고 동등한 새 cmdlet 집합이 포함된 `AzureRM.RecoveryServices.SiteRecovery`로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="5d98f-263">이전 cmdlet과 새 cmdlet을 매핑한 전체 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d98f-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="5d98f-264">사용되지 않는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d98f-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="5d98f-265">상응하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d98f-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="5d98f-266">별칭</span><span class="sxs-lookup"><span data-stu-id="5d98f-266">Aliases</span></span>                                  |
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
