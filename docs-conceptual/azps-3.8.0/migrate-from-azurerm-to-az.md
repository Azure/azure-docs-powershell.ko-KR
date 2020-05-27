---
title: AzureRM에서 Az로 Azure PowerShell 스크립트 마이그레이션
description: AzureRM 모듈에서 새 Az 모듈로 스크립트를 마이그레이션하는 단계와 도구에 대해 알아보세요.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 0b0b951d540ed91e15472853bba46e4f302921bc
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387601"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="fa9ce-103">Azure PowerShell을 AzureRM에서 Az로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="fa9ce-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="fa9ce-104">Az 모듈은 AzureRM과 기능 패리티를 가지고 있지만 더 짧고 일관된 cmdlet 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="fa9ce-105">AzureRM cmdlet용으로 작성된 스크립트는 새 모듈과 자동으로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="fa9ce-106">쉽게 전환하기 위해 Az는 AzureRM을 사용하여 기존 스크립트를 실행할 수 있는 도구를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="fa9ce-107">새 명령 집합으로 마이그레이션은 편리하지 않지만 이 문서는 새로운 모듈로 전환을 시작하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

<span data-ttu-id="fa9ce-108">AzureRM과 Az 간의 호환성이 손상되는 변경의 전체 목록을 보려면 [AzureRM에서 Az으로의 완전한 변경](migrate-az-1.0.0.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-108">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="fa9ce-109">기존 스크립트가 최신 AzureRM 릴리스에서 작동하는지 확인</span><span class="sxs-lookup"><span data-stu-id="fa9ce-109">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="fa9ce-110">모든 마이그레이션 단계를 수행하기 전에 시스템에 설치된 AzureRM의 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-110">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span> <span data-ttu-id="fa9ce-111">이렇게 하면 스크립트가 최신 릴리스에서 이미 실행되고 있는지 확인할 수 있고 제거해야 하는 AzureRM 버전을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-111">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="fa9ce-112">설치한 AzureRM의 버전을 확인하려면 다음 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-112">To check which version(s) of AzureRM you have installed, run the command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

<span data-ttu-id="fa9ce-113">사용 가능한 __최신__ AzureRM 릴리스는 __6.13.1__ 입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-113">The __latest__ available release of AzureRM is __6.13.1__.</span></span> <span data-ttu-id="fa9ce-114">이 버전이 설치되어 있지 않으면 여기서 설명하는 내용과 [호환성이 손상되는 변경 목록](migrate-az-1.0.0.md)에 해당하지 않는 Az 모듈에서 작동하도록 기존 스크립트를 추가로 수정해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-114">If you don't have this version installed, your existing scripts may need additional modification to work with the Az module beyond what's described here and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="fa9ce-115">스크립트가 AzureRM 6.13.1에서 작동하지 않으면 [AzureRM 5.x에서 6.x로 마이그레이션 가이드](/powershell/azure/azurerm/migration-guide.6.0.0)에 따라 해당 스크립트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-115">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span>
<span data-ttu-id="fa9ce-116">이전 버전의 AzureRM 모듈을 사용하는 경우 각 주 버전에 사용할 수 있는 마이그레이션 가이드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-116">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="uninstall-azurerm"></a><span data-ttu-id="fa9ce-117">AzureRM 제거</span><span class="sxs-lookup"><span data-stu-id="fa9ce-117">Uninstall AzureRM</span></span>

<span data-ttu-id="fa9ce-118">Az 모듈은 Windows용 PowerShell 5.1에 설치된 기존 AzureRM과 호환되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-118">The Az module is not guaranteed to be compatible with any existing AzureRM installs in PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="fa9ce-119">Az 모듈을 설치하기 전에 [AzureRM을 제거](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-119">Before you install the Az module, [uninstall AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fa9ce-120">시스템에서 AzureRM 모듈을 제거할 준비가 되지 않았으면 [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x 이상용 Az 모듈을 대신 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-120">If you're not ready to remove the AzureRM module from your system, you can install the Az module for [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x or later instead.</span></span> <span data-ttu-id="fa9ce-121">Windows용 PowerShell Core와 PowerShell 5.1은 서로 다른 모듈 라이브러리를 사용하므로 충돌이 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-121">PowerShell Core and PowerShell 5.1 for Windows use different module libraries, so there will be no conflicts.</span></span> <span data-ttu-id="fa9ce-122">PowerShell Core에서도 [별칭을 사용하도록 설정](#enable-azurerm-compatibility-aliases)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-122">You can still [enable aliases](#enable-azurerm-compatibility-aliases) in PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="fa9ce-123">Azure PowerShell Az 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="fa9ce-123">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="fa9ce-124">첫 번째 단계는 플랫폼에 Az 모듈을 설치하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-124">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="fa9ce-125">Az를 설치할 때는 AzureRM을 제거하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-125">When you install Az, it's recommended that you uninstall AzureRM.</span></span> <span data-ttu-id="fa9ce-126">다음 단계에서는 기존 스크립트를 계속 실행하고 이전 cmdlet 이름과의 호환성을 유지하는 방법을 알아보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-126">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="fa9ce-127">Azure PowerShell Az 모듈을 설치하려면 [Az 모듈 설치](install-az-ps.md)의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-127">To install the Azure PowerShell Az module, follow the instructions in [Install the Az module](install-az-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fa9ce-128">이때 모든 버전의 AzureRM을 제거하여 충돌이 발생하지 않도록 Az 모듈에 제공된 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet을 실행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-128">At this point, you might want to run the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet provided in the Az module, just to make sure that all versions of AzureRM have been uninstalled and won't cause conflicts.</span></span>

## <a name="enable-azurerm-compatibility-aliases"></a><span data-ttu-id="fa9ce-129">AzureRM 호환성 별칭을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="fa9ce-129">Enable AzureRM compatibility aliases</span></span>

<span data-ttu-id="fa9ce-130">AzureRM을 제거하고 최신 AzureRM 버전과 함께 스크립트가 작동하면 이제 Az 모듈에 대한 호환 모드를 사용할 때입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-130">With AzureRM uninstalled and your scripts working with the latest AzureRM version, the next step is to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="fa9ce-131">호환성은 다음 명령으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-131">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="fa9ce-132">별칭을 사용하면 Az 모듈이 설치된 이전 cmdlet 이름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-132">Aliases enable the ability to use old cmdlet names with the Az module installed.</span></span> <span data-ttu-id="fa9ce-133">이러한 별칭은 선택한 범위에 대한 프로필에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-133">These aliases are written to the profile for the selected scope.</span></span> <span data-ttu-id="fa9ce-134">프로필이 없으면 새 프로필이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-134">If no profile exists, one is created.</span></span>
<span data-ttu-id="fa9ce-135">`CurrentUser`보다 넓은 `-Scope`를 사용하는 경우 해당 프로필 파일을 만들거나 업데이트하려면 적절한 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-135">When using a `-Scope` broader than `CurrentUser`, the appropriate permissions are required to create or update the corresponding profile file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa9ce-136">모듈 이름이 아니라 __cmdlet 이름에만__ 별칭이 지정됩니다!</span><span class="sxs-lookup"><span data-stu-id="fa9ce-136">__Only__ cmdlet names are aliased - module names aren't!</span></span> <span data-ttu-id="fa9ce-137">`#Requires`, `Import-Module`, `.psd1`의 종속성 목록 또는 정규화된 cmdlet 이름을 사용하는 경우 이 시점에서 모듈 이름과 관련하여 [호환성이 손상되는 변경 목록](migrate-az-1.0.0.md)에 설명된 프로세스에 따라 해당 이름을 마이그레이션해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-137">If you're using `#Requires`, `Import-Module`, dependency lists in a `.psd1`, or fully-qualified cmdlet names, make sure that you migrate them at this point by following the process outlined in the [breaking changes list](migrate-az-1.0.0.md) regarding module names.</span></span>

> [!WARNING]
>
> <span data-ttu-id="fa9ce-138">이 명령에 대해 다른 `-Scope`를 사용할 수 있지만 권장되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-138">You can use a different `-Scope` for this command, but it's not recommended.</span></span> <span data-ttu-id="fa9ce-139">별칭은 선택된 범위에 대한 사용자 프로필에 기록되므로 가능한 한 범위를 제한적으로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-139">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="fa9ce-140">별칭을 시스템 전체에서 사용하도록 설정하면 AzureRM을 로컬 범위에 설치한 다른 사용자에게 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-140">Enabling aliases system-wide can cause issues for other users who have AzureRM installed in their local scope.</span></span>

<span data-ttu-id="fa9ce-141">별칭 모드가 활성화되면 스크립트를 다시 실행하여 스크립트가 여전히 예상대로 작동하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-141">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span>
<span data-ttu-id="fa9ce-142">일부 매개 변수 이름은 Az 모듈에서 변경, 추가 또는 요구되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-142">Some parameter names have been changed, added, or made required by the Az module.</span></span> <span data-ttu-id="fa9ce-143">cmdlet의 출력 형식도 변경되었을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-143">Output types of cmdlets may have changed as well.</span></span> <span data-ttu-id="fa9ce-144">이러한 변경 내용은 [호환성이 손상되는 변경 목록](migrate-az-1.0.0.md)에서 자세히 설명하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-144">These changes are detailed in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

## <a name="update-cmdlets-modules-and-parameters"></a><span data-ttu-id="fa9ce-145">cmdlet, 모듈 및 매개 변수 업데이트</span><span class="sxs-lookup"><span data-stu-id="fa9ce-145">Update cmdlets, modules, and parameters</span></span>

<span data-ttu-id="fa9ce-146">스크립트를 별칭에 따라 업데이트하고 실행하면 새 cmdlet을 사용하고 새로운 기능과 같은 다른 변경을 활용할 수 있도록 스크립트를 업데이트하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-146">With scripts updated and running under aliases, you can take your time to update them to use the new cmdlets and take advantage of other changes like new features.</span></span> <span data-ttu-id="fa9ce-147">대부분의 스크립트의 경우 [Az의 새 cmdlet 명명 체계에 따라](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes) cmdlet 이름만 업데이트하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-147">For most scripts, you will only need to update cmdlet names, [following the new cmdlet naming scheme in Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes).</span></span> <span data-ttu-id="fa9ce-148">또한 스크립트에서 수행하는 작업과 활용하는 Azure PowerShell 기능에 따라 스크립트를 작동시키는 데 필요한 몇 가지 다른 변경이 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-148">There may also be some other changes that you need to make in order to have your scripts work, depending on what they do and which Azure PowerShell features they take advantage of.</span></span>

<span data-ttu-id="fa9ce-149">예를 들어 [Blob Storage cmdlet](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage)에서 새 비동기 모델을 사용하도록 완전히 다시 수정되었으므로 이러한 cmdlet을 사용하는 스크립트에는 cmdlet 이름만 변경한 스크립트보다 더 많은 업데이트 작업이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-149">For example, the [Blob Storage cmdlets](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) have been completely reworked to use a new asynchronous model, so scripts using them will take more work to update than those where the only relevant changes were cmdlet names.</span></span>

<span data-ttu-id="fa9ce-150">지금까지 스크립트를 작고 간단하게 변경해야 했거나 별칭을 사용하도록 설정된 상태에서 추가 수정 없이 스크립트가 작동하는 경우에도, cmdlet 이름을 변경하고 별칭을 사용하지 않도록 설정한 후 사라질 수 있는 별칭의 '투명한' 동작을 사용하지 않도록 [Az 1.0.0의 호환성이 손상되는 변경 전체 목록](migrate-az-1.0.0.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-150">Even if you've only had to make small, simple changes to your scripts up to this point - or they even work without additional modification when aliases are enabled -  read the [full list of breaking changes in Az 1.0.0](migrate-az-1.0.0.md) to make sure that you're not relying on 'transparent' behavior of aliases which could disappear after you change cmdlet names and disable aliases.</span></span>

## <a name="disable-aliases"></a><span data-ttu-id="fa9ce-151">별칭을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="fa9ce-151">Disable aliases</span></span>

<span data-ttu-id="fa9ce-152">마이그레이션이 완료되고 앨리어싱 동작이 더 이상 사용되지 않으면 별칭을 사용하지 않도록 설정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-152">Once you've completed your migration and are no longer relying on aliasing behavior, it's recommended that you disable aliases.</span></span> <span data-ttu-id="fa9ce-153">이 작업은 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) cmdlet을 사용하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-153">This is done with the [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa9ce-154">이 cmdlet을 실행하는 경우 `Enable-AzureRmAlias`가 호출된 각 `-Scope`에 대해 이 cmdlet을 __호출해야 합니다__. 그렇지 않으면 앨리어싱 동작을 사용하는 스크립트가 시스템에 계속 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9ce-154">When running this cmdlet, __make sure__ that you invoke it for each `-Scope` that `Enable-AzureRmAlias` was invoked for, otherwise there may still be scripts on your system relying on the aliasing behavior.</span></span>
