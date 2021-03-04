---
title: Azure 컨텍스트 및 로그인 자격 증명
description: 여러 PowerShell 세션에 걸쳐 Azure 자격 증명 및 다른 정보를 재사용하는 방법에 대해 알아보세요.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: be9113ab1ad6a359832634ae2c21fd177b09318f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872310"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="e5ae2-103">Azure PowerShell 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="e5ae2-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="e5ae2-104">Azure PowerShell은 _Azure PowerShell 컨텍스트 개체_(Azure 컨텍스트)를 사용하여 구독 및 인증 정보를 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="e5ae2-105">둘 이상의 구독이 있는 경우 Azure 컨텍스트를 사용하여 Azure PowerShell cmdlet을 실행할 구독을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="e5ae2-106">Azure 컨텍스트는 여러 PowerShell 세션에서 로그인 정보를 저장하고 백그라운드 작업을 실행하는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="e5ae2-107">이 문서에서는 구독 또는 계정 관리가 아닌 Azure 컨텍스트 관리에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="e5ae2-108">사용자, 구독, 테넌트 또는 기타 계정 정보를 관리하려면 [Azure Active Directory](/azure/active-directory) 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="e5ae2-109">백그라운드 또는 병렬 작업을 실행하기 위한 컨텍스트 사용에 대한 자세한 내용은 Azure 컨텍스트에 익숙해진 후 [PowerShell 작업 에서 Azure PowerShell cmdlet 사용](using-psjobs.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="e5ae2-110">Azure 컨텍스트 개체 개요</span><span class="sxs-lookup"><span data-stu-id="e5ae2-110">Overview of Azure context objects</span></span>

<span data-ttu-id="e5ae2-111">Azure 컨텍스트는 명령을 실행할 활성 구독과 Azure Cloud에 연결하는 데 필요한 인증 정보를 나타내는 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="e5ae2-112">Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 인증할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="e5ae2-113">컨텍스트는 다음과 같이 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-113">An Azure context consists of:</span></span>

* <span data-ttu-id="e5ae2-114">[Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount)를 사용하여 Azure에 로그인하는 데 사용된 _계정_.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="e5ae2-115">Azure 컨텍스트는 계정 관점에서 사용자, 애플리케이션 ID 및 서비스 주체를 동일하게 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="e5ae2-116">_테넌트_ 와 연결된 Azure 리소스를 만들고 실행하기 위한 Microsoft와의 서비스 계약인 활성 _구독_.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="e5ae2-117">테넌트는 종종 설명서에서 또는 Active Directory로 작업할 때 _조직_ 이라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="e5ae2-118">Azure Cloud에 액세스하기 위해 저장된 인증 토큰인 _토큰 캐시_ 에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="e5ae2-119">이 토큰이 저장되는 위치와 지속 기간은 [컨텍스트 자동 저장 설정](#save-azure-contexts-across-powershell-sessions)에 의해 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="e5ae2-120">이러한 용어에 대한 자세한 내용은 [Azure Active Directory 용어](/azure/active-directory/fundamentals/active-directory-whatis#terminology)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="e5ae2-121">Azure 컨텍스트에서 사용되는 인증 토큰은 영구 세션의 일부인 다른 저장된 토큰과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span>

<span data-ttu-id="e5ae2-122">`Connect-AzAccount`에 로그인하면 기본 구독에 대해 하나 이상의 Azure 컨텍스트가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="e5ae2-123">`Connect-AzAccount`에 의해 반환된 개체는 PowerShell 세션의 나머지 부분에 사용되는 기본 Azure 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="e5ae2-124">Azure 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="e5ae2-124">Get Azure contexts</span></span>

<span data-ttu-id="e5ae2-125">사용 가능한 Azure 컨텍스트는 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet을 사용하여 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="e5ae2-126">`-ListAvailable`을 사용하여 사용 가능한 모든 컨텍스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="e5ae2-127">또는 이름별로 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="e5ae2-128">컨텍스트 이름은 연결된 구독의 이름과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5ae2-129">사용 가능한 Azure 컨텍스트가 항상 사용 가능한 구독은 __아닙니다__.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="e5ae2-130">Azure 컨텍스트는 로컬에 저장된 정보만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="e5ae2-131">[Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) cmdlet을 사용하여 구독을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="e5ae2-132">구독 정보에서 새 Azure 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="e5ae2-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="e5ae2-133">[Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet을 사용하여 새 Azure 컨텍스트를 만들고 활성 컨텍스트로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="e5ae2-134">새 Azure 컨텍스트를 만드는 가장 쉬운 방법은 기존 구독 정보를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="e5ae2-135">이 cmdlet은 `Get-AzSubscription`의 출력 개체를 파이프된 값으로 사용하고 새 Azure 컨텍스트를 구성하도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="e5ae2-136">또는 필요한 경우 구독 이름 또는 ID와 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="e5ae2-137">`-Name` 인수를 생략하면 구독의 이름과 ID는 `Subscription Name (subscription-id)` 형식의 컨텍스트 이름으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="e5ae2-138">활성 Azure 컨텍스트 변경</span><span class="sxs-lookup"><span data-stu-id="e5ae2-138">Change the active Azure context</span></span>

<span data-ttu-id="e5ae2-139">`Set-AzContext` 및 [Select-AzContext](/powershell/module/az.accounts/set-azcontext)를 사용하여 활성 Azure 컨텍스트를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="e5ae2-140">[새 Azure 컨텍스트 만들기](#create-a-new-azure-context-from-subscription-information)에 설명된 대로 `Set-AzContext`는 구독에 대한 Azure 컨텍스트가 없는 경우 새로 하나 만든 다음, 해당 컨텍스트를 활성 컨텍스트로 사용하도록 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="e5ae2-141">`Select-AzContext`는 기존 Azure 컨텍스트에만 사용하도록 되어 있으며 `Set-AzContext -Context`를 사용하는 것과 유사하게 작동하지만 파이프와 함께 사용하도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="e5ae2-142">Azure PowerShell의 다른 많은 계정 및 컨텍스트 관리 명령과 마찬가지로 `Set-AzContext` 및 `Select-AzContext`는 컨텍스트 활성 시간을 제어할 수 있도록 `-Scope` 인수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="e5ae2-143">`-Scope`를 사용하면 기본값을 변경하지 않고 단일 세션의 활성 컨텍스트를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="e5ae2-144">전체 PowerShell 세션에서 컨텍스트를 전환하지 않으려면 `-AzContext` 인수를 사용하여 지정된 컨텍스트에 대해 모든 Azure PowerShell 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="e5ae2-145">Azure PowerShell cmdlet을 사용한 컨텍스트의 다른 주요 용도는 백그라운드 명령을 실행하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="e5ae2-146">Azure PowerShell을 사용하여 PowerShell 작업을 실행하는 방법에 대한 자세한 내용은 [PowerShell 작업에서 Azure PowerShell cmdlet 실행](using-psjobs.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="e5ae2-147">PowerShell 세션에서 Azure 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="e5ae2-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="e5ae2-148">기본적으로 Azure 컨텍스트는 PowerShell 세션 간에 사용하기 위해 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="e5ae2-149">다음과 같은 방법으로 이 동작을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="e5ae2-150">`Connect-AzAccount`와 함께 `-Scope Process`를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="e5ae2-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="e5ae2-151">이 로그인의 일부로 반환된 Azure 컨텍스트는 현재 세션에 _대해서만_ 유효하며 Azure PowerShell 컨텍스트 자동 저장 설정에 관계없이 자동으로 저장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="e5ae2-152">[Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet을 사용하여 AzurePowershell의 컨텍스트 자동 저장을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="e5ae2-153">컨텍스트 자동 저장을 사용하지 않으면 저장된 토큰이 지워지지 __않습니다__.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="e5ae2-154">저장된 Azure 컨텍스트 정보를 지우는 방법에 대해 알아보려면 [Azure 컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="e5ae2-155">[Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet을 사용하여 Azure 컨텍스트 자동 저장을 명시적으로 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="e5ae2-156">자동 저장을 사용하면 사용자의 모든 컨텍스트가 이후의 PowerShell 세션을 위해 로컬로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="e5ae2-157">컨텍스트를 [Import-AzContext](/powershell/module/az.accounts/import-azcontext)와 함께 로드할 수 있는 향후 PowerShell 세션에서 사용할 [Save-AzContext](/powershell/module/az.accounts/save-azcontext)와 함께 컨텍스트를 수동으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="e5ae2-158">컨텍스트 자동 저장을 사용하지 않으면 저장된 모든 컨텍스트 정보는 지워지지 __않습니다__.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="e5ae2-159">저장된 정보를 제거하려면 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="e5ae2-160">저장된 컨텍스트 제거에 대한 자세한 내용은 [컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="e5ae2-161">이러한 각각의 명령은 `-Scope` 매개 변수를 지원하며, 현재 실행중인 프로세스에만 적용되는 `Process` 값을 취합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="e5ae2-162">예를 들어, PowerShell 세션을 종료한 후 새로 만든 컨텍스트가 저장되지 않도록 하기 위해</span><span class="sxs-lookup"><span data-stu-id="e5ae2-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="e5ae2-163">컨텍스트 정보 및 토큰은 Windows의 `$env:USERPROFILE\.Azure` 디렉토리 및 다른 플랫폼의 `$HOME/.Azure`에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="e5ae2-164">구독 ID 및 테넌트 ID와 같은 중요한 정보가 로그 또는 저장된 컨텍스트를 통해 저장된 정보에 계속 노출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="e5ae2-165">저장된 정보를 지우는 방법에 대해 알아보려면 [컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="e5ae2-166">Azure 컨텍스트 및 저장된 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="e5ae2-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="e5ae2-167">Azure 컨텍스트 및 로그인 자격 증명을 지우기 위해</span><span class="sxs-lookup"><span data-stu-id="e5ae2-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="e5ae2-168">[Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount)를 사용하여 계정에서 로그아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="e5ae2-169">계정 또는 컨텍스트별로 계정에서 로그아웃할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="e5ae2-170">연결을 끊으면 항상 저장된 인증 토큰이 제거되고 연결이 끊어진 사용자 또는 컨텍스트와 관련된 저장된 컨텍스트가 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="e5ae2-171">[Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="e5ae2-172">이 cmdlet은 항상 저장된 컨텍스트 및 인증 토큰을 제거하고 또한 사용자도 로그아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="e5ae2-173">[Remove-AzContext](/powershell/module/az.accounts/remove-azcontext)를 사용하여 컨텍스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>

  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="e5ae2-174">활성 컨텍스트를 제거하면 Azure에서 연결이 끊어지며 `Connect-AzAccount`를 사용하여 다시 인증해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ae2-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5ae2-175">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e5ae2-175">See also</span></span>

* [<span data-ttu-id="e5ae2-176">PowerShell 작업에서 Azure PowerShell cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e5ae2-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="e5ae2-177">Azure Active Directory 용어</span><span class="sxs-lookup"><span data-stu-id="e5ae2-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="e5ae2-178">Az.Accounts 참조</span><span class="sxs-lookup"><span data-stu-id="e5ae2-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
