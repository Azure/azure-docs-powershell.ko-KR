---
title: AzureRM에서 Az로 Azure PowerShell 스크립트 마이그레이션
description: AzureRM에서 새 Az PowerShell 모듈로 Azure PowerShell 스크립트를 마이그레이션하는 단계와 도구에 대해 알아봅니다.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012037"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="51dcf-103">Azure PowerShell을 AzureRM에서 Az로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="51dcf-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="51dcf-104">모든 버전의 AzureRM PowerShell 모듈은 오래된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-104">All versions of the AzureRM PowerShell module are outdated.</span></span> <span data-ttu-id="51dcf-105">이제는 [Az PowerShell 모듈](install-az-ps.md)이 Azure와 상호 작용하는 데 추천되는 PowerShell 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

## <a name="why-a-new-module"></a><span data-ttu-id="51dcf-106">새 모듈인 이유는?</span><span class="sxs-lookup"><span data-stu-id="51dcf-106">Why a new module?</span></span>

<span data-ttu-id="51dcf-107">가장 크고 중요한 변화는 .NET Standard 라이브러리 기반의 [PowerShell](/powershell/scripting/overview)이 도입된 이후 여러 플랫폼에 사용되는 제품이 되었다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-107">The biggest and most important change is that [PowerShell](/powershell/scripting/overview), being based on the .NET Standard library, has been a cross-platform product since its introduction.</span></span>

<span data-ttu-id="51dcf-108">PowerShell 언어와 마찬가지로, 저희는 모든 플랫폼에서 Azure를 지원하기 위해 최선을 다하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-108">Like the PowerShell language, we're committed to bringing Azure support to all platforms.</span></span> <span data-ttu-id="51dcf-109">즉, .NET Standard를 사용하고 PowerShell Core와 호환될 수 있도록 Azure PowerShell 모듈을 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-109">Our commitment meant that the Azure PowerShell modules needed to be updated to use .NET Standard and be compatible with PowerShell Core.</span></span> <span data-ttu-id="51dcf-110">기존 AzureRM 모듈을 수정하고 수정된 내용을 지원하기 위해 복잡하게 변경하는 대신 Az 모듈을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-110">Rather than modifying the existing AzureRM module and introducing complex changes to add this support, the Az module was created.</span></span>

<span data-ttu-id="51dcf-111">또한 새 모듈을 만듦으로써 엔지니어들이 cmdlet 및 모듈의 디자인과 이름을 일관적으로 유지할 수 있게 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-111">Creating a new module also allowed our engineers to make the design, naming of cmdlets, and modules consistent.</span></span> <span data-ttu-id="51dcf-112">이제 모든 모듈이 `Az.` 접두사로 시작하고, 모든 cmdlet에서 `Verb-AzNoun` 명명 규칙을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-112">All modules now start with the `Az.` prefix and cmdlets all use the `Verb-AzNoun` naming convention.</span></span> <span data-ttu-id="51dcf-113">이전에는 cmdlet 이름이 더 길었으며 일관적이지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-113">Previously, cmdlet names were longer and inconsistent.</span></span>

<span data-ttu-id="51dcf-114">모듈 수도 감소했습니다. 동일한 서비스에서 작동하는 일부 모듈이 결합되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-114">The number of modules were also reduced: Some modules that worked with the same services have been combined.</span></span> <span data-ttu-id="51dcf-115">이제 동일한 서비스의 관리 평면과 데이터 평면 cmdlet이 단일 모듈에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-115">Management plane and data plane cmdlets for the same service are now contained within a single module.</span></span> <span data-ttu-id="51dcf-116">이 통합 덕분에 종속성 및 가져오기를 수동으로 관리하는 분들의 작업이 훨씬 간단해집니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-116">For those of you who manually manage dependencies and imports, this consolidation makes things much simpler.</span></span>

<span data-ttu-id="51dcf-117">우리 팀은 이처럼 중요한 변경을 통해 그 어느 때보다도 쉽게, 이전보다 더 많은 플랫폼에서 PowerShell cmdlet을 통해 Azure를 사용할 수 있도록 최선을 다했습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-117">By making these important changes, the team has committed to making it easier than ever before and on more platforms than previously possible to use Azure with PowerShell cmdlets.</span></span>

## <a name="upgrading-to-az-powershell"></a><span data-ttu-id="51dcf-118">Az PowerShell로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="51dcf-118">Upgrading to Az PowerShell</span></span>

<span data-ttu-id="51dcf-119">AzureRM cmdlet용으로 작성된 스크립트는 자동으로 Az에서 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-119">Scripts written for the AzureRM cmdlets won't automatically work with Az.</span></span> <span data-ttu-id="51dcf-120">쉽게 전환할 수 있도록 [AzureRM에서 Az로의 마이그레이션 도구 키트](https://github.com/Azure/azure-powershell-migration)가 개발되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-120">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="51dcf-121">새 명령 집합으로 마이그레이션은 편리하지 않지만 이 문서는 Az PowerShell 모듈로 전환을 시작하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-121">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="51dcf-122">Az PowerShell 모듈을 만든 이유에 대한 자세한 내용은 [새로운 Azure PowerShell Az 모듈 소개](new-azureps-module-az.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="51dcf-122">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="51dcf-123">새로운 cmdlet 이름은 쉽게 익힐 수 있도록 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="51dcf-124">cmdlet 이름에 `AzureRm` 또는 `Azure`를 사용하는 대신 `Az`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="51dcf-125">예를 들어 이전 cmdlet `New-AzureRMVm`은 `New-AzVm`이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-125">For example, the old cmdlet `New-AzureRMVm` has become `New-AzVm`.</span></span>
<span data-ttu-id="51dcf-126">하지만 마이그레이션은 단순히 새 cmdlet 이름을 익히는 데서 그치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-126">However, migration is more than just becoming familiar with the new cmdlet names, though.</span></span> <span data-ttu-id="51dcf-127">이름이 바뀐 모듈, 매개 변수 및 기타 중요한 변경이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-127">There are renamed modules, parameters, and other important changes.</span></span>

<span data-ttu-id="51dcf-128">AzureRM과 Az 간의 호환성이 손상되는 변경의 전체 목록을 보려면 [AzureRM에서 Az으로의 완전한 변경](migrate-az-1.0.0.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="51dcf-128">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="51dcf-129">기존 스크립트가 최신 AzureRM 릴리스에서 작동하는지 확인</span><span class="sxs-lookup"><span data-stu-id="51dcf-129">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="51dcf-130">모든 마이그레이션 단계를 수행하기 전에 시스템에 설치된 AzureRM의 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-130">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="51dcf-131">이렇게 하면 스크립트가 최신 릴리스에서 이미 실행되고 있는지 확인할 수 있고 제거해야 하는 AzureRM 버전을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-131">Doing so allows you to make sure scripts are already running on the latest release and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="51dcf-132">설치한 AzureRM의 버전을 확인하려면 다음 예를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-132">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="51dcf-133">사용 가능한 **최신** AzureRM 릴리스는 **6.13.1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-133">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="51dcf-134">이 버전이 설치되어 있지 않으면 이 문서에서 설명하는 내용과 [호환성이 손상되는 변경 목록](migrate-az-1.0.0.md)의 범위에 해당하지 않는 Az 모듈에서 작동하도록 기존 스크립트를 추가로 수정해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-134">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond the scope of what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="51dcf-135">스크립트가 AzureRM 6.13.1에서 작동하지 않으면 [AzureRM 5.x에서 6.x로 마이그레이션 가이드](/powershell/azure/azurerm/migration-guide.6.0.0)에 따라 해당 스크립트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-135">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="51dcf-136">이전 버전의 AzureRM 모듈을 사용하는 경우 각 주 버전에 사용할 수 있는 마이그레이션 가이드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-136">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="51dcf-137">옵션 1(권장): PowerShell 스크립트 자동 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="51dcf-137">Option 1 (recommended): Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="51dcf-138">이 권장 옵션은 AzureRM 스크립트를 Az로 마이그레이션하는 데 필요한 작업을 최소화합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-138">This recommended option minimizes the effort required to migrate AzureRM scripts to Az.</span></span>

### <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="51dcf-139">AzureRM에서 Az로의 마이그레이션 도구 키트 설치</span><span class="sxs-lookup"><span data-stu-id="51dcf-139">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a><span data-ttu-id="51dcf-140">스크립트를 자동으로 변환</span><span class="sxs-lookup"><span data-stu-id="51dcf-140">Convert your scripts automatically</span></span>

<span data-ttu-id="51dcf-141">AzureRM에서 Az로의 마이그레이션 도구 키트를 사용하면 스크립트를 수정하기 전과 Az PowerShell 모듈을 설치하기 전에 스크립트에서 수행될 변경 사항을 결정하는 계획을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-141">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="51dcf-142">[AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션](quickstart-migrate-azurerm-to-az-automatically.md) 빠른 시작은 PowerShell 스크립트를 AzureRM에서 Az PowerShell 모듈로 자동 업데이트하는 전체 프로세스를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-142">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a><span data-ttu-id="51dcf-143">옵션 2: Enable-AzureRmAlias를 통해 호환성 모드 사용</span><span class="sxs-lookup"><span data-stu-id="51dcf-143">Option 2: Use compatibility mode with Enable-AzureRmAlias</span></span>

<span data-ttu-id="51dcf-144">Az 모듈에는 새 구문으로 업데이트하는 동안 기존 스크립트를 사용할 수 있게 하는 호환성 모드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-144">The Az module has a compatibility mode to help you use existing scripts while you update to the new syntax.</span></span> <span data-ttu-id="51dcf-145">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet은 별칭을 통해 호환성 모드를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-145">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet enables a compatibility mode through aliases.</span></span> <span data-ttu-id="51dcf-146">이 모드에서는 Az로 전체 마이그레이션 작업을 수행하는 동안 최소한의 수정으로 기존 스크립트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-146">This mode allows you to use existing scripts with minimal modification while working towards a full migration to Az.</span></span> <span data-ttu-id="51dcf-147">기본적으로 `Enable-AzureRmAlias`는 현재 PowerShell 세션에만 호환성 별칭을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-147">By default, `Enable-AzureRmAlias` only enables compatibility aliases for the current PowerShell session.</span></span> <span data-ttu-id="51dcf-148">PowerShell 세션 전체에서 호환성 별칭을 유지하려면 `Scope` 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-148">Use its `Scope` parameter to persist compatibility aliases across PowerShell sessions.</span></span> <span data-ttu-id="51dcf-149">자세한 내용은 [Enable-AzureRmAlias 참조 설명서](/powershell/module/az.accounts/enable-azurermalias)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="51dcf-149">For more information, see [the Enable-AzureRmAlias reference documentation](/powershell/module/az.accounts/enable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51dcf-150">cmdlet 이름이 별칭으로 지정되어 있더라도 여전히 Az cmdlet에 대한 새(또는 이름이 바뀐) 매개 변수가 있거나 반환 값이 변경되었을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-150">Even though the cmdlet names are aliased, there may still be new (or renamed) parameters or changed return values for the Az cmdlets.</span></span> <span data-ttu-id="51dcf-151">별칭을 사용하도록 설정하여 마이그레이션을 처리할 것으로 기대하지 마세요!</span><span class="sxs-lookup"><span data-stu-id="51dcf-151">Don't expect enabling aliases to take care of the migration for you!</span></span> <span data-ttu-id="51dcf-152">업데이트가 필요할 수 있는 스크립트의 위치를 찾으려면 [호환성이 손상되는 변경 전체 목록](migrate-az-1.0.0.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="51dcf-152">See the [full breaking changes list](migrate-az-1.0.0.md) to find where your scripts may require updates.</span></span>

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a><span data-ttu-id="51dcf-153">옵션 3: Azure PowerShell 확장을 사용하여 Visual Studio Code에서 스크립트 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="51dcf-153">Option 3: Migrate your scripts in Visual Studio Code with the Azure PowerShell extension</span></span>

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a><span data-ttu-id="51dcf-154">Visual Studio Code용 Azure PowerShell 확장 설치</span><span class="sxs-lookup"><span data-stu-id="51dcf-154">Install the Azure PowerShell extension for Visual Studio Code</span></span>

<span data-ttu-id="51dcf-155">[VSCode용 Azure PowerShell 확장](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools) 설치</span><span class="sxs-lookup"><span data-stu-id="51dcf-155">Install the [Azure PowerShell extension for VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)</span></span>

### <a name="convert-your-scripts-manually"></a><span data-ttu-id="51dcf-156">수동으로 스크립트 변환</span><span class="sxs-lookup"><span data-stu-id="51dcf-156">Convert your scripts manually</span></span>

1. <span data-ttu-id="51dcf-157">VSCode에서 AzureRM 스크립트 로드</span><span class="sxs-lookup"><span data-stu-id="51dcf-157">Load your AzureRM script in VSCode</span></span>
2. <span data-ttu-id="51dcf-158">명령 팔레트 `Ctrl+Shift+P`를 열고 `Migrate Azure PowerShell script`를 선택하여 마이그레이션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-158">Start the migration by opening the command palette `Ctrl+Shift+P` and select `Migrate Azure PowerShell script`</span></span>
3. <span data-ttu-id="51dcf-159">원본 버전 `AzureRM` 선택</span><span class="sxs-lookup"><span data-stu-id="51dcf-159">Select source version `AzureRM`</span></span>
4. <span data-ttu-id="51dcf-160">밑줄이 그어진 각 명령 또는 매개 변수에 대해 권장되는 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="51dcf-160">Follow the recommended actions for each underlined command or parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51dcf-161">다음 단계</span><span class="sxs-lookup"><span data-stu-id="51dcf-161">Next steps</span></span>

* [<span data-ttu-id="51dcf-162">AzureRM 제거</span><span class="sxs-lookup"><span data-stu-id="51dcf-162">Uninstall AzureRM</span></span>](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [<span data-ttu-id="51dcf-163">Azure PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="51dcf-163">Install Azure PowerShell</span></span>](install-az-ps.md)
