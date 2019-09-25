---
title: AzureRM에서 Azure PowerShell Az 1.0.0으로의 모든 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell Az 버전 1 릴리스의 호환성이 손상되는 변경에 대한 목록이 포함되어 있습니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: 1d99f04525a33f03f859bfb4abe263b12ca6add9
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226238"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="2483e-103">Az 1.0.0의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="2483e-104">이 문서에서는 AzureRM 6.x와 새 Az 모듈 버전 1.x 이상 간의 변경 내용에 대한 자세한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="2483e-105">목차는 스크립트에 영향을 줄 수 있는 모듈별 변경을 포함하여 전체 마이그레이션 경로를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="2483e-106">마이그레이션을 AzureRM에서 Az로 시작하는 방법에 대한 일반적인 추천 사항은 [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2483e-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2483e-107">Az 1.0.0과 Az 2.0.0 간에도 호환성이 손상되는 변경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="2483e-108">이 가이드에 따라 AzureRM에서 Az로 업데이트한 후에 [Az 2.0.0 호환성이 손상되는 변경](migrate-az-2.0.0.md)을 참조하여 추가로 변경할 필요가 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="2483e-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="2483e-109">목차</span><span class="sxs-lookup"><span data-stu-id="2483e-109">Table of Contents</span></span>

- [<span data-ttu-id="2483e-110">일반적인 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="2483e-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="2483e-111">cmdlet 명사 접두사 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="2483e-112">모듈 이름 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="2483e-113">제거된 모듈</span><span class="sxs-lookup"><span data-stu-id="2483e-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="2483e-114">Windows PowerShell 5.1 및 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2483e-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="2483e-115">PSCredential을 사용하여 사용자 로그인 임시 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="2483e-116">웹 브라우저 프롬프트 대신 기본 디바이스 코드 로그인</span><span class="sxs-lookup"><span data-stu-id="2483e-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="2483e-117">모듈의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="2483e-118">Az.ApiManagement(이전에는 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="2483e-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="2483e-119">Az.Billing(이전에는 AzureRM.Billing, AzureRM.Consumption, 및 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="2483e-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="2483e-120">Az.CognitiveServices(이전에는 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="2483e-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="2483e-121">Az.Compute(이전에는 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="2483e-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="2483e-122">Az.DataFactory(이전에는 AzureRM.DataFactories 및 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="2483e-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="2483e-123">Az.DataLakeAnalytics(이전에는 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="2483e-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="2483e-124">Az.DataLakeStore(이전에는 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="2483e-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="2483e-125">Az.KeyVault(이전에는 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="2483e-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="2483e-126">Az.Media(이전에는 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="2483e-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="2483e-127">Az.Monitor(이전에는 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="2483e-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="2483e-128">Az.Network(이전에는 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="2483e-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="2483e-129">Az.OperationalInsights(이전에는 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="2483e-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="2483e-130">Az.RecoveryServices(이전에는 AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, 및 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="2483e-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="2483e-131">Az.Resources(이전에는 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="2483e-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="2483e-132">Az.ServiceFabric(이전에는 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="2483e-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="2483e-133">Az.Sql(이전에는 AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="2483e-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="2483e-134">Az.Storage(이전에는 Azure.Storage 및 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="2483e-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="2483e-135">Az.Websites(이전에는 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="2483e-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="2483e-136">일반적인 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="2483e-136">General breaking changes</span></span>

<span data-ttu-id="2483e-137">이 섹션에서는 Az 모듈 재설계의 일부인 일반적인 호환성이 손상되는 변경에 대해 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="2483e-138">Cmdlet 명사 접두사 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="2483e-139">AzureRM 모듈에서 cmdlet은 `AzureRM` 또는 `Azure`를 명사 접두사로 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="2483e-140">Az는 cmdlet 이름을 간소화하고 정규화하여 모든 cmdlet에서 'Az'를 해당 cmdlet 명사 접두사로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="2483e-141">다음은 그 예입니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="2483e-142">다음으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="2483e-143">이러한 새 cmdlet 이름으로 더 간단하게 전환할 수 있도록 Az에서 [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) 및 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias)라는 두 개의 새 cmdlet을 도입했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="2483e-144">`Enable-AzureRmAlias`는 최신 Az cmdlet 이름에 매핑되는 AzureRM의 이전 cmdlet 이름에 대한 별칭을 에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="2483e-145">`Enable-AzureRmAlias`에서 `-Scope` 인수를 사용하면 별칭을 사용하도록 설정되는 위치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="2483e-146">예를 들어, AzureRM의 다음 스크립트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2483e-147">`Enable-AzureRmAlias`를 사용하여 최소한의 변경으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2483e-148">`Enable-AzureRmAlias -Scope CurrentUser`를 실행하면 열려 있는 모든 PowerShell 세션에 별칭을 사용하도록 설정되므로 이 cmdlet을 실행한 후 이와 같은 스크립트를 전혀 변경할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2483e-149">별칭 cmdlet을 사용하는 방법에 대한 자세한 내용은 [Enable-AzureRmAlias 참조](/powershell/module/az.accounts/enable-azurermalias)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2483e-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="2483e-150">별칭을 사용하지 않도록 설정할 준비가 되면 `Disable-AzureRmAlias`에서 만들어진 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="2483e-151">자세한 내용은 [Disable-AzureRmAlias 참조](/powershell/module/az.accounts/disable-azurermalias)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2483e-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2483e-152">별칭을 사용하지 않도록 설정하는 경우 별칭을 사용하도록 설정된 _모든_ 범위에 대해 사용하지 않도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="2483e-153">모듈 이름 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-153">Module Name Changes</span></span>

<span data-ttu-id="2483e-154">다음 모듈을 제외하고 모듈 이름이 `AzureRM.*`에서 `Az.*`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="2483e-155">AzureRM 모듈</span><span class="sxs-lookup"><span data-stu-id="2483e-155">AzureRM module</span></span> | <span data-ttu-id="2483e-156">Az 모듈</span><span class="sxs-lookup"><span data-stu-id="2483e-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="2483e-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2483e-157">Azure.Storage</span></span> | <span data-ttu-id="2483e-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2483e-158">Az.Storage</span></span> |
| <span data-ttu-id="2483e-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2483e-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="2483e-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2483e-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="2483e-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2483e-161">AzureRM.Profile</span></span> | <span data-ttu-id="2483e-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2483e-162">Az.Accounts</span></span> |
| <span data-ttu-id="2483e-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2483e-163">AzureRM.Insights</span></span> | <span data-ttu-id="2483e-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2483e-164">Az.Monitor</span></span> |
| <span data-ttu-id="2483e-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2483e-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="2483e-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2483e-166">Az.DataFactory</span></span> |
| <span data-ttu-id="2483e-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2483e-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="2483e-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2483e-168">Az.DataFactory</span></span> |
| <span data-ttu-id="2483e-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2483e-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="2483e-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2483e-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="2483e-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2483e-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="2483e-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2483e-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="2483e-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2483e-173">AzureRM.Tags</span></span> | <span data-ttu-id="2483e-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2483e-174">Az.Resources</span></span> |
| <span data-ttu-id="2483e-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2483e-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="2483e-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2483e-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="2483e-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="2483e-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="2483e-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2483e-178">Az.Billing</span></span> |
| <span data-ttu-id="2483e-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2483e-179">AzureRM.Consumption</span></span> | <span data-ttu-id="2483e-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2483e-180">Az.Billing</span></span> |

<span data-ttu-id="2483e-181">모듈 이름이 변경되면 `#Requires` 또는 `Import-Module`을 사용하여 특정 모듈을 로드하는 스크립트는 대신 새 모듈을 사용하도록 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="2483e-182">cmdlet 접미사가 변경되지 않은 모듈의 경우 이는 모듈 이름이 변경되었지만 작업 공간을 나타내는 접미사가 _변경되지 않았음_ 을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="2483e-183">#Requires 및 Import-Module 문 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="2483e-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="2483e-184">`#Requires` 또는 `Import-Module`을 사용하여 AzureRM 모듈에 대한 종속성을 선언하는 스크립트는 새 모듈 이름을 사용하도록 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="2483e-185">예:</span><span class="sxs-lookup"><span data-stu-id="2483e-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="2483e-186">다음으로 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="2483e-187">`Import-Module`의 경우</span><span class="sxs-lookup"><span data-stu-id="2483e-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="2483e-188">다음으로 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="2483e-189">Cmdlet 정규화 호출 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="2483e-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="2483e-190">다음과 같이 모듈에서 정규화된 cmdlet 호출을 사용하는 스크립트는</span><span class="sxs-lookup"><span data-stu-id="2483e-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="2483e-191">새 모듈 및 cmdlet 이름을 사용하도록 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="2483e-192">모듈 매니페스트 종속성 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="2483e-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="2483e-193">모듈 매니페스트 파일(.psd1)을 통해 AzureRM 모듈에 대한 종속성을 나타내는 모듈은 `RequiredModules` 섹션에서 모듈 이름을 업데이트해야 합니다</span><span class="sxs-lookup"><span data-stu-id="2483e-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="2483e-194">다음으로 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="2483e-195">제거된 모듈</span><span class="sxs-lookup"><span data-stu-id="2483e-195">Removed modules</span></span>

<span data-ttu-id="2483e-196">다음 모듈이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="2483e-197">이러한 서비스를 위한 도구는 더 이상 적극적으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="2483e-198">편리한 대체 서비스로 이동하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="2483e-199">Windows PowerShell 5.1 및 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2483e-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="2483e-200">Windows용 PowerShell 5.1에서 Az를 사용하려면 .NET Framework 4.7.2를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="2483e-201">PowerShell Core 6.x 이상을 사용하는 경우 .NET Framework가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="2483e-202">PSCredential을 사용하여 사용자 로그인 임시 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="2483e-203">.NET 표준의 인증 흐름이 변경되어 PSCredential을 통한 사용자 로그인이 일시적으로 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="2483e-204">이 기능은 Windows용 PowerShell 5.1에 대한 2019년 1월 15일 릴리스에서 다시 도입됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="2483e-205">이는 [이 GitHub 문제](https://github.com/Azure/azure-powershell/issues/7430)에서 자세히 설명하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="2483e-206">웹 브라우저 프롬프트 대신 기본 디바이스 코드 로그인</span><span class="sxs-lookup"><span data-stu-id="2483e-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="2483e-207">.NET 표준의 인증 흐름이 변경되어 대화식 로그인 중에 기본 로그인 흐름으로 디바이스 로그인을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="2483e-208">웹 브라우저 기반 로그인은 Windows용 PowerShell 5.1에 대한 2019년 1월 15일 릴리스에서 기본적으로 다시 도입됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="2483e-209">이때 사용자는 스위치 매개 변수를 사용하여 디바이스 로그인을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="2483e-210">모듈의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="2483e-210">Module breaking changes</span></span>

<span data-ttu-id="2483e-211">이 섹션에서는 개별 모듈 및 cmdlet에 대한 특정 호환성이 손상되는 변경에 대해 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="2483e-212">Az.ApiManagement(이전에는 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="2483e-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="2483e-213">다음 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="2483e-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2483e-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="2483e-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2483e-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="2483e-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2483e-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="2483e-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2483e-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="2483e-218">대신 **Set-AzApiManagement**를 사용하여 이러한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="2483e-219">다음 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-219">Removed the following properties:</span></span>
  - <span data-ttu-id="2483e-220">`PsApiManagementContext`에서 `PsApiManagementHostnameConfiguration` 형식의 `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration`, `ScmHostnameConfiguration` 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="2483e-221">대신 `PsApiManagementCustomHostNameConfiguration` 형식의 `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration`, `ScmCustomHostnameConfiguration`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="2483e-222">PsApiManagementContext에서 `StaticIPs`속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="2483e-223">해당 속성은 `PublicIPAddresses`, `PrivateIPAddresses`로 분할되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="2483e-224">필수 속성 `Location`을 New-AzureApiManagementVirtualNetwork cmdlet에서 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="2483e-225">Az.Billing(이전에는 AzureRM.Billing, AzureRM.Consumption, 및 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="2483e-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="2483e-226">`InvoiceName` 매개 변수가 `Get-AzConsumptionUsageDetail` cmdlet에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="2483e-227">스크립트는 청구서에 대한 다른 ID 매개 변수를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="2483e-228">Az.CognitiveServices(이전에는 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="2483e-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="2483e-229">`Get-AzCognitiveServicesAccountSkus` cmdlet에서 `GetSkusWithAccountParamSetName` 매개 변수 집합을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="2483e-230">ResourceGroupName 및 계정 이름을 사용하는 대신 계정 형식 및 위치별로 SKU를 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="2483e-231">Az.Compute(이전에는 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="2483e-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="2483e-232">`PSVirtualMachine` 및 `PSVirtualMachineScaleSet` 객체의 `Identity` 속성에서 `IdentityIds`가 제거되었습니다. 스크립트는 더 이상 이 필드의 값을 사용하여 처리 결정을 내려서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="2483e-233">`PSVirtualMachineScaleSetVM` 개체의 `InstanceView` 속성의 형식이 `VirtualMachineInstanceView`에서 `VirtualMachineScaleSetVMInstanceView`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="2483e-234">`UpgradePolicy` 속성에서 `AutoOSUpgradePolicy` 및 `AutomaticOSUpgrade` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="2483e-235">`PSSnapshotUpdate` 개체의 `Sku` 속성의 형식이 `DiskSku`에서 `SnapshotSku`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="2483e-236">`VmScaleSetVMParameterSet`이 `Add-AzVMDataDisk` cmdlet에서 제거되면 더 이상 ScaleSet VM에 개별적으로 데이터 디스크를 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="2483e-237">Az.DataFactory(이전에는 AzureRM.DataFactories 및 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="2483e-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="2483e-238">`GatewayName` 매개 변수가 `New-AzDataFactoryEncryptValue` cmdlet에서 필수 항목이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="2483e-239">`New-AzDataFactoryGatewayKey` cmdlet이 제거됨</span><span class="sxs-lookup"><span data-stu-id="2483e-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="2483e-240">`Get-AzDataFactoryV2ActivityRun` cmdlet에서 `LinkedServiceName` 매개 변수가 제거되었습니다. 스크립트는 더 이상 이 필드의 값을 사용하여 처리 결정을 내려서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="2483e-241">Az.DataLakeAnalytics(이전에는 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="2483e-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="2483e-242">사용되지 않는 cmdlet 제거: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="2483e-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="2483e-243">Az.DataLakeStore(이전에는 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="2483e-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="2483e-244">다음 cmdlet의 `Encoding` 매개 변수는 `FileSystemCmdletProviderEncoding` 형식에서 `System.Text.Encoding` 형식으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="2483e-245">이 변경은 인코딩 값 `String` 및 `Oem`을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="2483e-246">다른 모든 이전 인코딩 값은 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="2483e-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2483e-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="2483e-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2483e-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="2483e-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2483e-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="2483e-250">사용되지 않는 `Tags` 속성 별칭을 `New-AzDataLakeStoreAccount` 및 `Set-AzDataLakeStoreAccount` cmdlet에서 제거함</span><span class="sxs-lookup"><span data-stu-id="2483e-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="2483e-251">다음을 사용하는 스크립트</span><span class="sxs-lookup"><span data-stu-id="2483e-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="2483e-252">다음과 같이 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="2483e-253">`PSDataLakeStoreAccountBasic` 개체에서 사용되지 않는 속성 `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps`을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="2483e-254">`Get-AzDataLakeStoreAccount`에서 반환된 `PSDatalakeStoreAccount`를 사용하는 모든 스크립트는 이러한 속성을 참조하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="2483e-255">Az.KeyVault(이전에는 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="2483e-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="2483e-256">`PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` 및 `PSKeyVaultSecretAttributes` 개체에서 `PurgeDisabled` 속성이 제거되었습니다. 스크립트는 처리 결정을 내리기 위해 ```PurgeDisabled``` 속성을 더 이상 참조하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="2483e-257">Az.Media(이전에는 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="2483e-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="2483e-258">다음을 사용하여 `New-AzMediaService` cmdlet에서 사용되지 않는 `Tags` 속성 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="2483e-259">다음과 같이 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="2483e-260">Az.Monitor(이전에는 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="2483e-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="2483e-261">`Set-AzDiagnosticSetting` cmdlet 스크립트에서 다음을 사용하여 단일 매개 변수 이름을 위해 복수 이름 `Categories` 및 `Timegrains` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="2483e-262">다음과 같이 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="2483e-263">Az.Network(이전에는 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="2483e-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="2483e-264">사용되지 않는 매개 변수 `ResourceId`를 `Get-AzServiceEndpointPolicyDefinition` cmdlet에서 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="2483e-265">`PSVirtualNetwork` 개체에서 사용되지 않는 속성 `EnableVmProtection`을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="2483e-266">사용되지 않는 cmdlet 제거: `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="2483e-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="2483e-267">스크립트는 더 이상 이 필드의 값에 따라 처리하도록 결정하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="2483e-268">Az.OperationalInsights(이전에는 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="2483e-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="2483e-269">`Get-AzOperationalInsightsDataSource`에 설정된 기본 매개 변수가 제거되고 `ByWorkspaceNameByKind`가 기본 매개 변수 집합이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="2483e-270">다음을 사용하여 데이터 원본을 나열하는 스크립트</span><span class="sxs-lookup"><span data-stu-id="2483e-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="2483e-271">종류를 지정하도록 변경되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2483e-272">Az.RecoveryServices(이전에는 AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, 및 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="2483e-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="2483e-273">`New/Set-AzRecoveryServicesAsrPolicy` cmdlet에서 `Encryption` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="2483e-274">`TargetStorageAccountName` 매개 변수는 이제 `Restore-AzRecoveryServicesBackupItem` cmdlet의 관리 디스크 복원에 필수 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="2483e-275">`Restore-AzRecoveryServicesBackupItem` cmdlet에서 `StorageAccountName`, `StorageAccountResourceGroupName` 매개 변수 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="2483e-276">`Get-AzRecoveryServicesBackupContainer` cmdlet에서 `Name` 매개 변수 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="2483e-277">Az.Resources(이전에는 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="2483e-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="2483e-278">`New/Set-AzPolicyAssignment` cmdlet에서 `Sku` 매개 변수를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="2483e-279">`New-AzADServicePrincipal` 및 `New-AzADSpCredential` cmdlet에서 `Password` 매개 변수를 제거했습니다. 암호는 자동으로 생성되며 암호를 제공하는 스크립트는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="2483e-280">출력에서 암호를 검색하도록 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="2483e-281">Az.ServiceFabric(이전에는 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="2483e-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="2483e-282">다음 cmdlet 반환 형식이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="2483e-283">`ApplicationHealthPolicy` 형식의 속성 `ServiceTypeHealthPolicies`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="2483e-284">`ClusterUpgradeDeltaHealthPolicy` 형식의 속성 `ApplicationHealthPolicies`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="2483e-285">`ClusterUpgradePolicy` 형식의 속성 `OverrideUserUpgradePolicy`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="2483e-286">이러한 변경 내용은 다음 cmdlet에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="2483e-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2483e-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="2483e-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2483e-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="2483e-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2483e-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="2483e-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2483e-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="2483e-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2483e-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="2483e-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2483e-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="2483e-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2483e-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="2483e-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2483e-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="2483e-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2483e-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="2483e-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2483e-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="2483e-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2483e-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="2483e-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2483e-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="2483e-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2483e-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="2483e-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2483e-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="2483e-301">Az.Sql(이전에는 AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="2483e-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="2483e-302">`Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet에서 `State`, `ResourceId` 매개 변수 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="2483e-303">사용되지 않는 cmdlet 제거: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="2483e-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="2483e-304">사용되지 않는 매개 변수 `Current`를 `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet에서 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="2483e-305">사용되지 않는 매개 변수 `DatabaseName`을 `Get-AzSqlServerServiceObjective` cmdlet에서 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="2483e-306">사용되지 않는 매개 변수 `PrivilegedLogin`을 `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet에서 제거</span><span class="sxs-lookup"><span data-stu-id="2483e-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="2483e-307">Az.Storage(이전에는 Azure.Storage 및 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="2483e-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="2483e-308">스토리지 계정 이름만 사용하여 Oauth 스토리지 컨텍스트를 만들 수 있도록 기본 매개 변수 집합이 `OAuthParameterSet`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="2483e-309">예제: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="2483e-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="2483e-310">`Location` 매개 변수가 `Get-AzStorageUsage` cmdlet에서 필수 항목이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="2483e-311">이제 Storage API 메서드는 동기 API 호출 대신 작업 기반 비동기 패턴(TAP)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="2483e-312">다음 예제에서는 새 비동기 명령을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="2483e-313">Blob 스냅샷</span><span class="sxs-lookup"><span data-stu-id="2483e-313">Blob Snapshot</span></span>

<span data-ttu-id="2483e-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2483e-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="2483e-315">Az:</span><span class="sxs-lookup"><span data-stu-id="2483e-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="2483e-316">스냅샷 공유</span><span class="sxs-lookup"><span data-stu-id="2483e-316">Share Snapshot</span></span>

<span data-ttu-id="2483e-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2483e-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="2483e-318">Az:</span><span class="sxs-lookup"><span data-stu-id="2483e-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="2483e-319">일시 삭제된 Blob 삭제 취소</span><span class="sxs-lookup"><span data-stu-id="2483e-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="2483e-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2483e-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="2483e-321">Az:</span><span class="sxs-lookup"><span data-stu-id="2483e-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="2483e-322">BLOB 계층 설정</span><span class="sxs-lookup"><span data-stu-id="2483e-322">Set Blob Tier</span></span>

<span data-ttu-id="2483e-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2483e-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="2483e-324">Az:</span><span class="sxs-lookup"><span data-stu-id="2483e-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="2483e-325">Az.Websites(이전에는 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="2483e-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="2483e-326">사용되지 않는 속성을 `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, `PSSite` 개체에서 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="2483e-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
