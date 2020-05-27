---
title: PowerShellGet으로 Azure PowerShell을 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 17e625dacfadff07b0498ac173b7b2c312172f87
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387771"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="a65dd-103">PowerShellGet으로 Azure PowerShell을 설치</span><span class="sxs-lookup"><span data-stu-id="a65dd-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="a65dd-104">이 아티클에서는 PowerShellGet을 사용하여 Windows용 PowerShell 5.x용 Azure PowerShell 모듈을 설치하는 단계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="a65dd-105">PowerShellGet 및 모듈 관리는 Azure PowerShell을 설치하는 더 좋은 방법이지만 대신 웹 플랫폼 설치 관리자 또는 MSI 패키지로 설치하려는 경우 [다른 설치 방법](other-install.md)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="a65dd-106">Azure 클래식 배포 모델은 본 버전의 Azure PowerShell에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="a65dd-107">클래식 배포에 대한 지원은 [Azure PowerShell Service Management 모듈 설치](/powershell/azure/servicemanagement/install-azure-ps) 지침을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a65dd-108">MacOS 또는 Linux 용 AzureRM 모듈은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="a65dd-109">이러한 플랫폼에서 Azure PowerShell cmdlet을 사용하려면 [Az 모듈을 설치](/powershell/azure/install-az-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="a65dd-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a65dd-110">Requirements</span></span>

<span data-ttu-id="a65dd-111">Azure PowerShell을 설치하려면, PowerShellGet 버전 1.1.2.0 이상이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="a65dd-112">귀하의 시스템에서 가능한지 확인하려면 다음 명령을 실행합니다:</span><span class="sxs-lookup"><span data-stu-id="a65dd-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="a65dd-113">다음과 비슷하게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="a65dd-114">PowerShellGet 설치를 업데이트하려면 다음 명령을 실행합니다:</span><span class="sxs-lookup"><span data-stu-id="a65dd-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="a65dd-115">PowerShellGet이 설치되지 않은 경우, 귀하의 시스템을 위해 아래 표의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="a65dd-116">시나리오</span><span class="sxs-lookup"><span data-stu-id="a65dd-116">Scenario</span></span>|<span data-ttu-id="a65dd-117">설치 지침</span><span class="sxs-lookup"><span data-stu-id="a65dd-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="a65dd-118">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="a65dd-118">Windows 10</span></span><br/><span data-ttu-id="a65dd-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a65dd-119">Windows Server 2016</span></span>|<span data-ttu-id="a65dd-120">OS에 포함된 WMF(Windows Management Framework) 5.0으로 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="a65dd-121">PowerShell 5로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="a65dd-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="a65dd-122">최신 버전의 WMF 설치</span><span class="sxs-lookup"><span data-stu-id="a65dd-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="a65dd-123">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="a65dd-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="a65dd-124">PowerShell 3 또는 PowerShell 4이 설치된 Windows</span><span class="sxs-lookup"><span data-stu-id="a65dd-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="a65dd-125"><il>[PackageManagement 모듈 가져오기](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="a65dd-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="a65dd-126">다음 명령 실행:</span><span class="sxs-lookup"><span data-stu-id="a65dd-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="a65dd-127">PowerShellGet을 사용하려면 스크립트를 실행할 수 있게 하는 실행 정책이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="a65dd-128">PowerShell의 실행 정책에 대한 자세한 내용은 [실행 정책 정보](/powershell/module/microsoft.powershell.core/about/about_execution_policies)(영문)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a65dd-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="a65dd-129">이 문서에서 설명된 모듈인 AzureRM에서는 .NET Framework를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="a65dd-130">이렇게 하면 .NET Core를 사용하는 PowerShell 6.0과 호환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="a65dd-131">PowerShell 6.0을 사용하는 경우, [macOS 및 Linux에 대한 설치 지침](install-azurermps-maclinux.md)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="a65dd-132">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="a65dd-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="a65dd-133">PowerShell 갤러리에서 모듈을 설치하려면 상승된 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="a65dd-134">Azure PowerShell을 설치하려면 승격된 세션에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="a65dd-135">NuGet 2.8.5.201 이전 버전을 사용하는 경우 최신 버전의 NuGet을 다운로드하여 설치하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="a65dd-136">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a65dd-137">PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="a65dd-138">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="a65dd-139">`AzureRM` 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a65dd-140">설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="a65dd-141">로그인</span><span class="sxs-lookup"><span data-stu-id="a65dd-141">Sign in</span></span>

<span data-ttu-id="a65dd-142">Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a65dd-143">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a65dd-144">`AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a65dd-145">Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="a65dd-146">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="a65dd-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="a65dd-147">[Update-Module](/powershell/module/powershellget/update-module)을 실행하여 Azure PowerShell 설치를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="a65dd-148">이 명령은 이전 버전을 제거하지 __않습니다__.</span><span class="sxs-lookup"><span data-stu-id="a65dd-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="a65dd-149">Azure PowerShell의 이전 버전을 시스템에서 제거하려면, [Azure PowerShell 모듈 제거](uninstall-azurerm-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="a65dd-150">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="a65dd-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="a65dd-151">여러 버전의 Azure PowerShell을 설치하는 것은 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="a65dd-152">온-프레미스 Azure Stack 리소스로 작업하거나 PowerShell 5.0으로 업데이트할 수 없는 이전 버전의 Windows를 실행하거나 Azure 클래식 배포 모델을 사용하는 경우 둘 이상의 버전이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="a65dd-153">이전 버전을 설치하려면 `-RequiredVersion` 인수를 설치 시 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="a65dd-154">Azure PowerShell 모듈 로드 시, 기본으로 최신 버전이 로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="a65dd-155">다른 버전을 로드하려면 `-RequiredVersion` 인수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a65dd-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="a65dd-156">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="a65dd-156">Provide feedback</span></span>

<span data-ttu-id="a65dd-157">Azure Powershell 사용 중 버그 발생 시, [ GitHub에서 문제 제출](https://github.com/Azure/azure-powershell/issues)을 해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="a65dd-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="a65dd-158">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a65dd-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a65dd-159">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a65dd-159">Next Steps</span></span>

<span data-ttu-id="a65dd-160">Azure PowerShell 사용을 시작하려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하여 모듈 및 모듈의 기능에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="a65dd-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
