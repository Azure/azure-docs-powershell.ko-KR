---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: e302e49d95b6bc15750366c9eb960a6fec80c1a4
ms.sourcegitcommit: e5b029312d17e12257b2b5351b808fdab0b4634c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2019
ms.locfileid: "70386839"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="5171e-103">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="5171e-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="5171e-104">이 문서에서는 PowerShellGet을 사용하여 Azure PowerShell 모듈을 설치하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="5171e-105">이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="5171e-106">Az 모듈에 대해 현재 다른 설치 방법은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5171e-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="5171e-107">Requirements</span></span>

<span data-ttu-id="5171e-108">Azure PowerShell은 Windows의 PowerShell 5.1 이상 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="5171e-109">PowerShell이 있거나 macOS 또는 Linux에 있는지 확실하지 않은 경우 [최신 버전의 PowerShell Core를 설치](/powershell/scripting/install/installing-powershell#powershell-core)하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="5171e-110">PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="5171e-111">Windows의 PowerShell 5.1에서 Azure PowerShell을 실행하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="5171e-112">필요한 경우 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="5171e-113">Windows 10을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="5171e-114">[.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="5171e-115">PowerShell Core를 사용하는 경우 Azure PowerShell에 대한 추가 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="5171e-116">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="5171e-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="5171e-117">Windows용 PowerShell 5.1에서 사용하기 위해 AzureRM 및 Az 모듈을 모두 동시에 __설치할 수는 없습니다__.</span><span class="sxs-lookup"><span data-stu-id="5171e-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="5171e-118">시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell Core 6.x 이상용 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="5171e-119">이렇게 하려면 [PowerShell Core 6.x 이상을 설치](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows)한 다음, PowerShell Core 터미널에서 다음 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="5171e-120">권장 설치 방법은 활성 사용자에 대해서만 설치하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="5171e-121">시스템의 모든 사용자에 대해 설치하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="5171e-122">관리자 권한 PowerShell 세션에서 관리자 권한으로 실행하거나 macOS 또는 Linux에서 `sudo` 명령을 사용하여 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="5171e-123">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="5171e-124">PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="5171e-125">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="5171e-126">Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5171e-127">설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5171e-128">문제 해결</span><span class="sxs-lookup"><span data-stu-id="5171e-128">Troubleshooting</span></span>

<span data-ttu-id="5171e-129">Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="5171e-130">여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="5171e-131">프록시 연결 차단</span><span class="sxs-lookup"><span data-stu-id="5171e-131">Proxy blocks connection</span></span>

<span data-ttu-id="5171e-132">`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="5171e-133">운영 체제마다 시스템 전체 프록시 구성에 대한 요구 사항이 다르며 여기서는 자세히 다루지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="5171e-134">프록시 설정 및 OS에 맞게 구성하는 방법은 시스템 관리자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="5171e-135">PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="5171e-136">PowerShell 5.1 이상에서는 다음 명령을 사용하여 PowerShell 세션에 사용할 프록시를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="5171e-137">운영 체제 자격 증명이 올바르게 구성되어 있으면 PowerShell 요청이 프록시를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="5171e-138">세션 간에 이 설정을 유지하려면 해당 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="5171e-139">패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="5171e-140">로그인</span><span class="sxs-lookup"><span data-stu-id="5171e-140">Sign in</span></span>

<span data-ttu-id="5171e-141">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="5171e-142">모듈 자동 로딩을 비활성화한 경우 `Import-Module Az`을 사용하여 모듈을 수동으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-142">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="5171e-143">모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="5171e-144">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5171e-145">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="5171e-146">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="5171e-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="5171e-147">Az 모듈의 패키지 방식으로 인해 [Update-Module](/powershell/module/powershellget/update-module) 명령에서 설치를 올바르게 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="5171e-148">Az 모듈을 설치하면 실제로 모든 종속 하위 모듈을 수집하고 설치하며, 각 서비스에 대한 cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-148">When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service.</span></span>
<span data-ttu-id="5171e-149">즉, Azure PowerShell 모듈을 업데이트하려면 __업데이트__ 하는 대신 __다시 설치__ 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="5171e-150">이 작업은 설치와 동일한 방식으로 수행되지만 `-Force` 인수를 추가해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="5171e-151">이렇게 하면 설치된 모듈을 덮어쓸 수 있지만 시스템에 이전 버전이 아직 남아 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="5171e-152">Azure PowerShell의 이전 버전을 시스템에서 제거하는 방법을 알아보려면, [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="5171e-153">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="5171e-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="5171e-154">Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="5171e-155">여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="5171e-156">Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="5171e-157">`-RequiredVersion` 인수를 사용하여 `Az` 모듈의 특정 버전을 설치하거나 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="5171e-158">모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5171e-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="5171e-159">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="5171e-159">Provide feedback</span></span>

<span data-ttu-id="5171e-160">Azure Powershell에서 버그 발생 시, [ GitHub에서 문제를 제출](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="5171e-161">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5171e-162">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5171e-162">Next Steps</span></span>

<span data-ttu-id="5171e-163">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="5171e-164">Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5171e-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
