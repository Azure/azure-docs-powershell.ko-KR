---
title: PowerShell 세션 간에 Azure 자격 증명 유지
description: 여러 PowerShell 세션에 걸쳐 Azure 자격 증명 및 다른 정보를 재사용하는 방법에 대해 알아보세요.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 02b8090aa1868f24445ddff3a95c0d0c376e2cb8
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68658082"
---
# <a name="persist-azure-user-credentials-across-powershell-sessions"></a><span data-ttu-id="a98da-103">PowerShell 세션 간에 Azure 사용자 자격 증명 유지</span><span class="sxs-lookup"><span data-stu-id="a98da-103">Persist Azure user credentials across PowerShell sessions</span></span>

<span data-ttu-id="a98da-104">Azure PowerShell은 **Azure Context Autosave**라고 하는 기능을 제공하며, 이는 다음과 같은 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="a98da-105">새 PowerShell 세션에서 다시 사용하기 위한 로그인 정보 보존.</span><span class="sxs-lookup"><span data-stu-id="a98da-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="a98da-106">오랫동안 수행되는 cmdlet을 실행하기 위한 더 쉬운 백그라운드 작업 사용.</span><span class="sxs-lookup"><span data-stu-id="a98da-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="a98da-107">별도 로그인 없이 계정, 구독 및 환경 간 전환.</span><span class="sxs-lookup"><span data-stu-id="a98da-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="a98da-108">동일한 PowerShell 세션에서 다른 자격 증명 및 구독을 동시에 사용하여 작업 실행.</span><span class="sxs-lookup"><span data-stu-id="a98da-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="a98da-109">정의된 Azure 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a98da-109">Azure contexts defined</span></span>

<span data-ttu-id="a98da-110">*Azure 컨텍스트*는 Azure PowerShell cmdlet의 대상을 정의하는 정보 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a98da-111">컨텍스트는 5개의 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-111">The context consists of five parts:</span></span>

- <span data-ttu-id="a98da-112">*계정* - Azure와의 통신을 인증하는 데 사용되는 사용자 이름 또는 서비스 주체</span><span class="sxs-lookup"><span data-stu-id="a98da-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="a98da-113">*구독* - 동작하는 리소스를 포함하는 Azure 구독.</span><span class="sxs-lookup"><span data-stu-id="a98da-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="a98da-114">*테넌트* - 구독을 포함하는 Azure Active Directory 테넌트.</span><span class="sxs-lookup"><span data-stu-id="a98da-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="a98da-115">테넌트는 ServicePrincipal 인증에서 더 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="a98da-116">*환경* - 목표가 되는 특정 Azure Cloud(보통 Azure 전역 클라우드).</span><span class="sxs-lookup"><span data-stu-id="a98da-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="a98da-117">그러나 환경 설정을 사용하여 대상 국가, 정부 및 온-프레미스(Azure Stack) 클라우드도 대상으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="a98da-118">*자격 증명* - Azure에서 사용자 ID를 확인하고 Azure의 리소스에 액세스하기 위한 사용자의 권한 부여를 확인하는 데 사용되는 정보</span><span class="sxs-lookup"><span data-stu-id="a98da-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="a98da-119">Azure PowerShell 최신 버전에서는 새 PowerShell 세션을 열 때마다 Azure 컨텍스트를 자동으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="a98da-120">다음 로그인을 위해 컨텍스트를 자동으로 저장</span><span class="sxs-lookup"><span data-stu-id="a98da-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="a98da-121">Azure PowerShell은 세션 간에 자동으로 컨텍스트 정보를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="a98da-122">PowerShell이 사용자의 컨텍스트 및 자격 증명을 기억하지 않도록 설정하려면 `Disable-AzContextAutoSave`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="a98da-123">컨텍스트 저장을 사용할 수 없으므로 PowerShell 세션을 열 때마다 Azure에 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="a98da-124">Azure PowerShell이 PowerShell 세션을 닫은 후 사용자의 컨텍스트를 기억하도록 하려면 `Enable-AzContextAutosave`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="a98da-125">컨텍스트 및 자격 증명 정보는 사용자 디렉터리의 숨겨진 특수 폴더(Windows의 경우 `$env:USERPROFILE\.Azure`, 기타 플랫폼에서는 `$HOME/.Azure`)에 자동으로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="a98da-126">새로운 PowerShell 세션마다 마지막 세션에 사용된 컨텍스트가 대상으로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="a98da-127">Azure 컨텍스트를 관리할 수 있는 cmdlet을 사용하면 세분화된 제어가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="a98da-128">변경 내용을 현재 PowerShell 세션(`Process` 범위)에만 적용하거나 또는 모든 PowerShell 세션(`CurrentUser` 범위)에 적용하려는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="a98da-129">이러한 옵션은 [컨텍스트 범위 사용](#using-context-scopes)에서 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-129">These options are discussed in more detail in [Using Context Scopes](#using-context-scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="a98da-130">Azure PowerShell cmdlet을 백그라운드 작업으로 실행</span><span class="sxs-lookup"><span data-stu-id="a98da-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="a98da-131">**Azure 컨텍스트 자동 저장** 기능을 사용하면 PowerShell 백그라운드 작업으로 컨텍스트를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="a98da-132">PowerShell을 사용하면 장기 실행 작업을 작업이 완료될 때까지 기다리지 않고 백그라운드 작업으로 시작하고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="a98da-133">두 가지 방법을 통해 백그라운드 작업으로 자격 증명을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="a98da-134">컨텍스트를 인수로 전달</span><span class="sxs-lookup"><span data-stu-id="a98da-134">Passing the context as an argument</span></span>

  <span data-ttu-id="a98da-135">대부분 AzureRM cmdlet을 사용하면 cmdlet에 컨텍스트를 매개 변수로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="a98da-136">다음 예제와 같이 백그라운드 작업으로 컨텍스트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="a98da-137">자동 저장이 활성화된 기본 컨텍스트 사용</span><span class="sxs-lookup"><span data-stu-id="a98da-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="a98da-138">**컨텍스트 자동 저장**을 사용하도록 설정한 경우 백그라운드 작업은 자동으로 기본 저장된 기본 컨텍스트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="a98da-139">백그라운드 작업의 결과를 알아야 하는 경우 `Get-Job`을 사용하여 작업 상태를 확인하고 `Wait-Job`을 사용하여 작업이 완료될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="a98da-140">백그라운드 작업의 출력을 캡처하거나 표시하려면 `Receive-Job`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="a98da-141">자세한 내용은 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a98da-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="a98da-142">컨텍스트 생성, 선택, 이름 바꾸기 및 제거</span><span class="sxs-lookup"><span data-stu-id="a98da-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="a98da-143">컨텍스트를 작성하려면 Azure에 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="a98da-144">`Connect-AzAccount` cmdlet(또는 해당 별칭인 `Login-AzAccount`)은 Azure PowerShell cmdlet에서 사용하는 기본 컨텍스트를 설정하고, 사용자는 이를 통해 자격 증명에서 허용하는 모든 테넌트 또는 구독에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="a98da-145">로그인한 후 새 컨텍스트를 추가하려면 `Set-AzContext`(또는 해당 별칭인 `Select-AzSubscription`)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="a98da-146">앞의 예제는 현재 자격 증명을 사용하여 새 컨텍스트 대상인 ‘Contoso Subscription 1’을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="a98da-147">새 컨텍스트는 ‘Contoso1’이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="a98da-148">컨텍스트에 대한 이름을 제공하지 않은 경우 계정 ID 및 구독 ID를 사용하는 기본 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="a98da-149">기존 컨텍스트 이름을 바꾸려면 `Rename-AzContext` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="a98da-150">예:</span><span class="sxs-lookup"><span data-stu-id="a98da-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="a98da-151">이 예제에서는 자동 이름 `[user1@contoso.org; 123456-7890-1234-564321]`을 사용하는 컨텍스트 이름을 간단한 이름인 ‘Contoso2’로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="a98da-152">또한 컨텍스트를 관리하는 cmdlet에서 탭 완성 기능을 사용하면 컨텍스트를 빠르게 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="a98da-153">마지막으로, 컨텍스트를 제거하려면 `Remove-AzContext` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="a98da-154">예:</span><span class="sxs-lookup"><span data-stu-id="a98da-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="a98da-155">‘Contoso2’로 명명된 컨텍스트를 잊었습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="a98da-156">`Set-AzContext`를 사용하여 나중에 다시 이 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="a98da-157">자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="a98da-157">Removing credentials</span></span>

<span data-ttu-id="a98da-158">`Disconnect-AzAccount`(`Logout-AzAccount`라고도 함)를 사용하여 사용자 또는 서비스 주체에 대한 모든 자격 증명 및 연결된 컨텍스트를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="a98da-159">`Disconnect-AzAccount` cmdlet을 매개 변수 없이 실행하면 현재 컨텍스트에서 사용자 또는 서비스 주체에 연결된 모든 자격 증명 및 컨텍스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="a98da-160">사용자 이름, 서비스 주체 이름 또는 컨텍스트를 특정 보안 주체를 대상으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="a98da-161">컨텍스트 범위 사용</span><span class="sxs-lookup"><span data-stu-id="a98da-161">Using context scopes</span></span>

<span data-ttu-id="a98da-162">경우에 따라 다른 세션에 영향을 주지 않고 PowerShell 세션에서 컨텍스트를 선택, 변경 또는 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="a98da-163">컨텍스트 cmdlet의 기본 동작을 변경하려면 `Scope` 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="a98da-164">`Process` 범위는 현재 세션에만 적용되도록 기본 동작을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="a98da-165">반대로 `CurrentUser` 범위는 현재 세션만이 아닌 모든 세션의 컨텍스트를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="a98da-166">예를 들어, 다른 창에 영향을 주지 않고 현재 PowerShell 세션의 기본 컨텍스트 또는 다음에 세션을 열 때 사용되는 컨텍스트를 변경하려면 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="a98da-167">컨텍스트 자동 저장 설정이 기억되는 방식</span><span class="sxs-lookup"><span data-stu-id="a98da-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="a98da-168">컨텍스트 자동 저장 설정은 사용자 Azure PowerShell 디렉터리(Windows에서는 `$env:USERPROFILE\.Azure`, 기타 플랫폼에서는 `$HOME/.Azure`)에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="a98da-169">컴퓨터 계정 중 일부 유형은 이 디렉터리에 액세스하지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="a98da-170">이러한 시나리오에서 환경 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="a98da-171">‘true’로 설정하면 컨텍스트가 자동으로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="a98da-172">‘false’로 설정하면 컨텍스트가 저장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="a98da-173">컨텍스트 관리 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a98da-173">Context management cmdlets</span></span>

- <span data-ttu-id="a98da-174">[Enable-AzContextAutosave][enable] - powershell 세션 간에 컨텍스트를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="a98da-175">변경 내용이 전역 컨텍스트를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="a98da-176">[Disable-AzContextAutosave][disable] - 컨텍스트 자동 저장을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="a98da-177">새로운 각 PowerShell 세션은 다시 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="a98da-178">[Select-AzContext][select] - 기본값으로 컨텍스트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="a98da-179">모든 cmdlet이 인증을 위해 이 컨텍스트에서 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="a98da-180">[Disconnect-AzAccount][remove-cred] - 계정과 관련된 자격 증명 및 컨텍스트를 모두 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="a98da-181">[Remove-AzContext][remove-context] - 명명된 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="a98da-182">[Rename-AzContext][rename] - 기존 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="a98da-183">[Add-AzAccount][login] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="a98da-184">인증 후 기본 컨텍스트의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="a98da-185">[Import-AzContext][import] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="a98da-186">[Set-AzContext][set-context] - 기존의 명명된 컨텍스트를 선택하고, 프로세스 또는 현재 사용자로 범위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98da-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
