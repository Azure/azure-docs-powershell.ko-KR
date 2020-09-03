---
title: 실험적 Azure PowerShell 모듈 사용
description: 실험적 Azure PowerShell 모듈의 기본 원칙 및 사용을 이해합니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: fd910e124a8589c2e5e187bc5a9d2a902ae57a07
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243891"
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="bd660-103">실험적 Azure PowerShell 모듈 사용</span><span class="sxs-lookup"><span data-stu-id="bd660-103">Using experimental Azure PowerShell modules</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="bd660-104">Azure PowerShell 팀은 Azure의 개발자 도구(특히 CLI)에 중점을 두고 Azure PowerShell 환경에 많은 향상된 기능을 실험하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="bd660-105">실험적 방법론</span><span class="sxs-lookup"><span data-stu-id="bd660-105">Experimentation methodology</span></span>

<span data-ttu-id="bd660-106">실험을 용이하게 하기 위해 기존 Azure SDK 기능을 새롭고 사용하기에 더 쉬운 방법으로 구현하는 새 Azure PowerShell 모듈을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="bd660-107">대부분의 경우에서 cmdlet은 기존 cmdlet을 정확하게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="bd660-108">단, 실험적 cmdlet은 Azure 리소스를 더 쉽게 만들고 관리할 수 있도록 약식 표기와 더 스마트한 기본값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="bd660-109">이러한 모듈은 기존 Azure PowerShell 모듈과 함께 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="bd660-110">cmdlet 이름은 더 짧은 이름을 제공하여 이름이 기존의 실험용이 아닌 cmdlet과 상충하는 것을 방지하기 위해 더 짧아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="bd660-111">실험적 모듈은 다음 명명 규칙을 사용합니다. `AzureRM.*.Experiments`</span><span class="sxs-lookup"><span data-stu-id="bd660-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="bd660-112">이 명명 규칙은 미리 보기 모듈의 이름 지정인 `AzureRM.*.Preview`와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="bd660-113">미리 보기 모듈은 실험적 모듈과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="bd660-114">미리 보기 모듈은 미리 보기 제품으로만 사용할 수 있는 Azure 서비스의 새로운 기능을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="bd660-115">미리 보기 모듈은 기존 Azure PowerShell 모듈을 대신하며 동일한 cmdlet 및 매개 변수 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="bd660-116">실험적 모듈 설치 방법</span><span class="sxs-lookup"><span data-stu-id="bd660-116">How to install an experimental module</span></span>

<span data-ttu-id="bd660-117">실험적 모듈은 기존 Azure PowerShell 모듈과 마찬가지로 PowerShell 갤러리에 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="bd660-118">실험적 모듈 목록을 보려면 다음 명령을 실행하십시오.</span><span class="sxs-lookup"><span data-stu-id="bd660-118">To see a list of experimental modules, run the following command:</span></span>

```powershell-interactive
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="bd660-119">실험적 모듈을 설치하려면 관리자 권한 PowerShell 세션에서 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="bd660-120">설명서 및 지원</span><span class="sxs-lookup"><span data-stu-id="bd660-120">Documentation and support</span></span>

<span data-ttu-id="bd660-121">설명서는 설치 패키지에 포함되어 있으며 `Get-Help` cmdlet을 사용하여 액세스됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="bd660-122">실험적 모듈에 대한 공식 설명서는 게시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="bd660-123">이러한 모듈을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-123">We encourage you to test these modules.</span></span> <span data-ttu-id="bd660-124">기능성을 개선하고 사용자의 요구에 응답할 수 있도록 사용자 의견을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="bd660-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="bd660-125">단, 실험을 위해 이러한 모듈에 대한 지원은 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="bd660-126">GitHub 리포지토리에서 [문제](https://github.com/Azure/azure-powershell/issues)를 만들면 질문 또는 문제 보고서를 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="bd660-127">향상된 기능의 실험 및 영역</span><span class="sxs-lookup"><span data-stu-id="bd660-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="bd660-128">이러한 향상된 기능은 경쟁 제품의 핵심적인 차이점을 기준으로 선택되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="bd660-129">예를 들어 Azure CLI 2.0은 _API 노출 영역_이 아닌 _시나리오_를 기준 명령으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="bd660-130">Azure CLI 2.0은 최종 사용자가 더 쉽게 시나리오를 “시작”할 수 있도록 여러 스마트한 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="bd660-131">주요 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="bd660-131">Core improvements</span></span>

<span data-ttu-id="bd660-132">주요 향상된 기능은 “상식”으로 간주되며, 약간의 실험은 이러한 업데이트 구현을 진전시키기 위해 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="bd660-133">시나리오 기반 cmdlet - <em>\*모든</em> cmdlet은 Azure REST 서비스가 아닌 시나리오로 설계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-133">Scenario-based Cmdlets - <em>\*All</em>- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="bd660-134">더 짧은 이름 - cmdlet의 이름(예: `New-AzureRmVM` => `New-AzVm`) 및 매개 변수 이름(예: `-ResourceGroupName` => `-Rg`)를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="bd660-135">“이전” cmdlet과의 호환성에 대한 별칭을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="bd660-136">_이전 버전과 호환되는_ 매개 변수 집합을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="bd660-137">스마트한 기본값 - 스마트한 기본값을 만들어 “필요한” 정보를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="bd660-138">다음은 그 예입니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-138">For example:</span></span>
  - <span data-ttu-id="bd660-139">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="bd660-139">Resource Group</span></span>
  - <span data-ttu-id="bd660-140">위치</span><span class="sxs-lookup"><span data-stu-id="bd660-140">Location</span></span>
  - <span data-ttu-id="bd660-141">종속 리소스</span><span class="sxs-lookup"><span data-stu-id="bd660-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="bd660-142">실험적 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="bd660-142">Experimental improvements</span></span>

<span data-ttu-id="bd660-143">실험적 향상된 기능은 팀에서 실험을 통해 유효성을 검사하려는 중요한 변경 내용을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="bd660-144">단순 형식 - 복잡한 형식과 구성 개체는 피해서 시나리오를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="bd660-145">하나 또는 두 개의 매개 변수로 구성을 간소화합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="bd660-146">“스마트한 만들기” - “스마트한 만들기”를 구현하는 모든 시나리오에는 매개 변수가 필요 _없습니다_. 모든 필수 정보는 Azure PowerShell에 의해 독자적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="bd660-147">회색 매개 변수 - 대부분의 경우에서 일부 매개 변수는 “회색” 또는 반 선택적일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="bd660-148">매개 변수가 지정되지 않은 경우 사용자에게 해당 항목에 대해 매개 변수를 생성할 것인지 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="bd660-149">또한 사용자 동의 하에 회색 매개 변수가 컨텍스트를 기준으로 값을 유추하는 것이 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="bd660-150">예를 들어 회색 매개 변수가 최근 사용된 값을 제안하는 것이 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="bd660-151">`-Auto` 스위치 - `-Auto` 스위치는 메인라인 경로에서 필수 매개 변수의 무결성을 유지 관리하는 동시에 사용자가 _모든 항목의 기본값을 설정_할 수 있는 “옵트인” 방식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="bd660-152">기능별 스위치</span><span class="sxs-lookup"><span data-stu-id="bd660-152">Feature-specific switches</span></span>

<span data-ttu-id="bd660-153">예를 들어 “웹앱 만들기” 시나리오에는 기존 git 리포지토리에 “azure” 원격을 자동으로 추가하는 `-Git` 또는 `-AddRemote` 스위치가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="bd660-154">설정 가능한 기본값 - 사용자는 `-ResourceGroupName` 및 `-Location`과 같은 특정 유비쿼터스 매개 변수의 기본값을 설정할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="bd660-155">크기 기본값 - 리소스 “크기”는 다양한 리소스 제공자가 서로 다른 이름을 사용하기 때문에 사용자가 혼란스러울 수 있습니다(예: “Standard\_DS1\_v2” 또는 “S1”).</span><span class="sxs-lookup"><span data-stu-id="bd660-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="bd660-156">그러나 대부분의 사용자는 비용에 더 민감합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-156">However, most users care more about cost.</span></span> <span data-ttu-id="bd660-157">따라서 가격 책정 일정에 따라 “범용” 크기를 정의하는 것이 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="bd660-158">사용자가 특정 크기를 정할 수도 있고, 아니면 Azure PowerShell에서 리소스 예산에 따라 _최상의 옵션_을 선택하도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="bd660-159">출력 형식 - Azure PowerShell은 현재 `PSObject`를 반환하고 약간의 콘솔 출력이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="bd660-160">Azure PowerShell은 “스마트한 기본값” 사용에 관해 사용자에게 몇 가지 정보를 표시해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd660-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
