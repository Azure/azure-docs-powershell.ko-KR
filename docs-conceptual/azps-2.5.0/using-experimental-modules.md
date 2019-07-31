---
title: 실험적 Azure PowerShell 모듈 사용
description: 실험적 Azure PowerShell 모듈의 기본 원칙 및 사용을 이해합니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657589"
---
# <a name="use-experimental-azure-powershell-modules"></a><span data-ttu-id="73d1f-103">실험적 Azure PowerShell 모듈 사용</span><span class="sxs-lookup"><span data-stu-id="73d1f-103">Use experimental Azure PowerShell modules</span></span>

<span data-ttu-id="73d1f-104">Azure PowerShell 팀은 Azure의 개발자 도구에 중점을 두고 Azure PowerShell 환경에 많은 향상된 기능을 실험하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-104">With the emphasis on developer tools in Azure, the Azure PowerShell team experiments with many improvements to the Azure PowerShell experience.</span></span> <span data-ttu-id="73d1f-105">이 아티클에서는 Azure PowerShell을 사용하여 실험에 옵트인하고 개발 팀에 피드백을 제공하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-105">This article describes how to opt-in to experiments with Azure PowerShell and give feedback to the development team.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="73d1f-106">실험적 방법론</span><span class="sxs-lookup"><span data-stu-id="73d1f-106">Experimentation methodology</span></span>

<span data-ttu-id="73d1f-107">실험을 용이하게 하기 위해 기존 Azure SDK 기능을 새롭고 사용하기에 더 쉬운 방법으로 구현하는 새 Azure PowerShell 모듈을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-107">To facilitate experimentation, we're creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="73d1f-108">대부분의 경우에서 cmdlet은 기존 cmdlet을 정확하게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-108">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="73d1f-109">단, 실험적 cmdlet은 Azure 리소스를 더 쉽게 만들고 관리할 수 있도록 약식 표기와 더 스마트한 기본값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-109">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="73d1f-110">이러한 모듈은 기존 Azure PowerShell 모듈과 함께 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-110">These modules can be installed side by side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="73d1f-111">cmdlet 이름은 더 짧은 이름을 제공하여 이름이 기존의 실험용이 아닌 cmdlet과 상충하는 것을 방지하기 위해 더 짧아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-111">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="73d1f-112">실험적 모듈은 다음 명명 규칙을 사용합니다. `Az.*.Experiments`</span><span class="sxs-lookup"><span data-stu-id="73d1f-112">The experimental modules use the following naming convention: `Az.*.Experiments`.</span></span> <span data-ttu-id="73d1f-113">이 명명 규칙은 미리 보기 모듈의 이름 지정인 `Az.*.Preview`와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-113">This naming convention is similar to the naming of Preview modules: `Az.*.Preview`.</span></span> <span data-ttu-id="73d1f-114">미리 보기 모듈은 실험적 모듈과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-114">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="73d1f-115">미리 보기 모듈은 미리 보기 제품으로만 사용할 수 있는 Azure 서비스의 새로운 기능을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-115">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="73d1f-116">미리 보기 모듈은 기존 Azure PowerShell 모듈을 대신하며 동일한 cmdlet 및 매개 변수 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-116">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="73d1f-117">실험적 모듈 설치 방법</span><span class="sxs-lookup"><span data-stu-id="73d1f-117">How to install an experimental module</span></span>

<span data-ttu-id="73d1f-118">실험적 모듈은 기존 Azure PowerShell 모듈과 마찬가지로 PowerShell 갤러리에 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-118">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="73d1f-119">실험적 모듈 목록을 보려면 다음 명령을 실행하십시오.</span><span class="sxs-lookup"><span data-stu-id="73d1f-119">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

<span data-ttu-id="73d1f-120">실험적 모듈을 설치하려면 `Install-Module` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-120">To install an experimental module, use the `Install-Module` cmdlet.</span></span>

### <a name="documentation-and-support"></a><span data-ttu-id="73d1f-121">설명서 및 지원</span><span class="sxs-lookup"><span data-stu-id="73d1f-121">Documentation and support</span></span>

<span data-ttu-id="73d1f-122">설명서는 설치 패키지에 포함되어 있으며 `Get-Help` cmdlet을 사용하여 액세스됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-122">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="73d1f-123">실험적 모듈에 대한 공식 설명서는 게시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-123">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="73d1f-124">이러한 모듈을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-124">We encourage you to test these modules.</span></span> <span data-ttu-id="73d1f-125">기능성을 개선하고 사용자의 요구에 응답할 수 있도록 사용자 의견을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="73d1f-125">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="73d1f-126">단, 실험을 위해 이러한 모듈에 대한 지원은 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-126">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="73d1f-127">GitHub 리포지토리에서 [문제](https://github.com/Azure/azure-powershell/issues)를 만들면 질문 또는 문제 보고서를 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-127">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="73d1f-128">향상된 기능의 실험 및 영역</span><span class="sxs-lookup"><span data-stu-id="73d1f-128">Experiments and areas of improvement</span></span>

<span data-ttu-id="73d1f-129">이러한 향상된 기능은 경쟁 제품의 핵심적인 차이점을 기준으로 선택되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-129">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="73d1f-130">예를 들어 Azure CLI는 _API 노출 영역_이 아닌 _시나리오_를 기준 명령으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-130">For example, Azure CLI has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="73d1f-131">Azure CLI는 최종 사용자가 더 쉽게 시나리오를 “시작”할 수 있도록 여러 스마트한 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-131">Azure CLI uses a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="73d1f-132">주요 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="73d1f-132">Core improvements</span></span>

<span data-ttu-id="73d1f-133">주요 향상된 기능은 “상식”으로 간주되며, 약간의 실험은 이러한 업데이트 구현을 진전시키기 위해 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-133">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="73d1f-134">시나리오 기반 cmdlet - \**모든* cmdlet은 Azure REST 서비스가 아닌 시나리오로 설계되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-134">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="73d1f-135">더 짧은 이름 - cmdlet의 이름 및 매개 변수 이름을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-135">Shorter Names - Includes the names of cmdlets and the names of parameters.</span></span>
  <span data-ttu-id="73d1f-136">“이전” cmdlet과의 호환성에 대한 별칭을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-136">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="73d1f-137">_이전 버전과 호환되는_ 매개 변수 집합을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-137">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="73d1f-138">스마트한 기본값 - 스마트한 기본값을 만들어 “필요한” 정보를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-138">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="73d1f-139">예:</span><span class="sxs-lookup"><span data-stu-id="73d1f-139">For example:</span></span>
  - <span data-ttu-id="73d1f-140">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="73d1f-140">Resource Group</span></span>
  - <span data-ttu-id="73d1f-141">위치</span><span class="sxs-lookup"><span data-stu-id="73d1f-141">Location</span></span>
  - <span data-ttu-id="73d1f-142">종속 리소스</span><span class="sxs-lookup"><span data-stu-id="73d1f-142">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="73d1f-143">실험적 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="73d1f-143">Experimental improvements</span></span>

<span data-ttu-id="73d1f-144">실험적 향상된 기능은 팀에서 실험을 통해 유효성을 검사하려는 중요한 변경 내용을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-144">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="73d1f-145">단순 형식 - 복잡한 형식과 구성 개체는 피해서 시나리오를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-145">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="73d1f-146">하나 또는 두 개의 매개 변수로 구성을 간소화합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-146">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="73d1f-147">“스마트한 만들기” - “스마트한 만들기”를 구현하는 모든 시나리오에는 매개 변수가 필요 _없습니다_. 모든 필수 정보는 Azure PowerShell에 의해 독자적으로 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-147">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="73d1f-148">회색 매개 변수 - 대부분의 경우에서 일부 매개 변수는 “회색” 또는 반 선택적일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-148">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="73d1f-149">매개 변수가 지정되지 않은 경우 사용자에게 해당 항목에 대해 매개 변수를 생성할 것인지 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-149">If the parameter isn't specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="73d1f-150">또한 사용자 동의 하에 회색 매개 변수가 컨텍스트를 기준으로 값을 유추하는 것이 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-150">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="73d1f-151">예를 들어 회색 매개 변수가 최근 사용된 값을 제안하는 것이 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-151">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="73d1f-152">`-Auto` 스위치 - `-Auto` 스위치는 메인라인 경로에서 필수 매개 변수의 무결성을 유지 관리하는 동시에 사용자가 _모든 항목의 기본값을 설정_할 수 있는 “옵트인” 방식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-152">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="73d1f-153">기능별 스위치</span><span class="sxs-lookup"><span data-stu-id="73d1f-153">Feature-specific switches</span></span>

<span data-ttu-id="73d1f-154">예를 들어 “웹앱 만들기” 시나리오에는 기존 git 리포지토리에 “azure” 원격을 자동으로 추가하는 `-Git` 또는 `-AddRemote` 스위치가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-154">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="73d1f-155">설정 가능한 기본값 - 사용자가 `-ResourceGroupName` 및 `-Location`과 같은 일반 매개 변수의 기본값을 설정할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-155">Settable Defaults - Users should be able to set defaults for common parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="73d1f-156">크기 기본값 - 리소스 “크기”는 다양한 리소스 제공자가 서로 다른 이름을 사용하기 때문에 사용자가 혼란스러울 수 있습니다(예: “Standard\_DS1\_v2” 또는 “S1”).</span><span class="sxs-lookup"><span data-stu-id="73d1f-156">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="73d1f-157">그러나 대부분의 사용자는 비용에 더 민감합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-157">However, most users care more about cost.</span></span> <span data-ttu-id="73d1f-158">따라서 가격 책정 일정에 따라 “범용” 크기를 정의하는 것이 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-158">So it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="73d1f-159">사용자가 특정 크기를 정할 수도 있고, 아니면 Azure PowerShell에서 리소스 예산에 따라 _최상의 옵션_을 선택하도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-159">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="73d1f-160">출력 형식 - Azure PowerShell은 현재 `PSObject`를 반환하고 약간의 콘솔 출력이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-160">Output Format - Azure PowerShell currently returns `PSObject`s and there's little console output.</span></span> <span data-ttu-id="73d1f-161">Azure PowerShell은 “스마트한 기본값” 사용에 관해 사용자에게 몇 가지 정보를 표시해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73d1f-161">Azure PowerShell may need to display some information to the user about the "smart defaults" used.</span></span>
