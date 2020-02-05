---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 88861b63846db04e901d2a216657307c456c48fe
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002931"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="eafca-103">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="eafca-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="eafca-104">이 문서에서는 PowerShellGet을 사용하여 Azure PowerShell 모듈을 설치하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="eafca-105">이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="eafca-106">Az 모듈에 대해 현재 다른 설치 방법은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafca-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="eafca-107">Requirements</span></span>

<span data-ttu-id="eafca-108">Azure PowerShell은 Windows의 PowerShell 5.1 이상 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="eafca-109">PowerShell이 있거나 macOS 또는 Linux에 있는지 확실하지 않은 경우 [최신 버전의 PowerShell Core를 설치](/powershell/scripting/install/installing-powershell#powershell-core)하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="eafca-110">PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="eafca-111">Windows의 PowerShell 5.1에서 Azure PowerShell을 실행하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="eafca-112">필요한 경우 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="eafca-113">Windows 10을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="eafca-114">[.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="eafca-115">PowerShell Core를 사용하는 경우 Azure PowerShell에 대한 추가 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="eafca-116">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="eafca-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="eafca-117">Windows용 PowerShell 5.1에서 사용하기 위해 AzureRM 및 Az 모듈을 모두 동시에 __설치할 수는 없습니다__.</span><span class="sxs-lookup"><span data-stu-id="eafca-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="eafca-118">시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell Core 6.x 이상용 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="eafca-119">이렇게 하려면 [PowerShell Core 6.x 이상을 설치](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows)한 다음, PowerShell Core 터미널에서 다음 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="eafca-120">권장 설치 방법은 활성 사용자에 대해서만 설치하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="eafca-121">시스템의 모든 사용자에 대해 설치하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="eafca-122">관리자 권한 PowerShell 세션에서 관리자 권한으로 실행하거나 macOS 또는 Linux에서 `sudo` 명령을 사용하여 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="eafca-123">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="eafca-124">PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="eafca-125">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="eafca-126">Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="eafca-127">설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="eafca-128">오프라인 설치</span><span class="sxs-lookup"><span data-stu-id="eafca-128">Install offline</span></span>

<span data-ttu-id="eafca-129">일부 환경에서는 PowerShell 갤러리에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="eafca-130">이러한 경우에도 다음 방법 중 하나를 사용하여 오프라인으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="eafca-131">모듈을 다른 위치에 다운로드한 다음, 이 모듈을 네트워크의 설치 소스로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="eafca-132">다소 복잡해 보일 수도 있지만 이 프로세스를 사용하면 단일 서버 또는 파일 공유에서 PowerShell 모듈을 캐시하여 PowerShellGet으로 연결이 끊긴 시스템에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="eafca-133">[로컬 PowerShellGet 리포지토리로 작업](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)을 통해 로컬 리포지토리를 설정하고 연결이 끊어진 시스템에 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="eafca-134">네트워크에 연결된 컴퓨터에 [Azure PowerShell MSI](install-az-ps-msi.md)를 다운로드한 다음, PowerShell 갤러리에 액세스하지 않고 설치 관리자를 시스템에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="eafca-135">MSI 설치 관리자는 Windows의 PowerShell 5.1에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="eafca-136">[Save-Module](/powershell/module/PowershellGet/Save-Module)을 사용하여 모듈을 파일 공유에 저장하거나 다른 소스에 저장하고 다른 컴퓨터에 수동으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="eafca-137">문제 해결</span><span class="sxs-lookup"><span data-stu-id="eafca-137">Troubleshooting</span></span>

<span data-ttu-id="eafca-138">Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="eafca-139">여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="eafca-140">프록시 연결 차단</span><span class="sxs-lookup"><span data-stu-id="eafca-140">Proxy blocks connection</span></span>

<span data-ttu-id="eafca-141">`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="eafca-142">운영 체제마다 시스템 전체 프록시 구성에 대한 요구 사항이 다르며 여기서는 자세히 다루지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="eafca-143">프록시 설정 및 OS에 맞게 구성하는 방법은 시스템 관리자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="eafca-144">PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="eafca-145">PowerShell 5.1 이상에서는 다음 명령을 사용하여 PowerShell 세션에 사용할 프록시를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="eafca-146">운영 체제 자격 증명이 올바르게 구성되어 있으면 PowerShell 요청이 프록시를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="eafca-147">세션 간에 이 설정을 유지하려면 해당 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="eafca-148">패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="eafca-149">로그인</span><span class="sxs-lookup"><span data-stu-id="eafca-149">Sign in</span></span>

<span data-ttu-id="eafca-150">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="eafca-151">모듈 자동 로딩을 비활성화한 경우 `Import-Module Az`을 사용하여 모듈을 수동으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="eafca-152">모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="eafca-153">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="eafca-154">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="eafca-155">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="eafca-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="eafca-156">처음에 Install-Module을 사용한 경우 [Update-Module](/powershell/module/powershellget/update-module)을 사용하여 최신 버전을 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-156">If you originally used Install-Module, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="eafca-157">처음에 MSI 패키지를 사용한 경우 업데이트하려면 새 MSI를 다운로드하여 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-157">If you originally used th MSI package then you should download and install the new MSI in order to udpate.</span></span> <span data-ttu-id="eafca-158">PowershellGet의 패키지를 사용하여 업데이트하는 데 문제가 있는 경우 __업데이트__하기 보다는 __다시 설치__해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-158">If you have any issues with updating using the package from PowershellGet then you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="eafca-159">이 작업은 설치와 동일한 방식으로 수행되지만 `-Force` 인수를 추가해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="eafca-160">이렇게 하면 설치된 모듈을 덮어쓸 수 있지만 시스템에 이전 버전이 아직 남아 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="eafca-161">Azure PowerShell의 이전 버전을 시스템에서 제거하는 방법을 알아보려면, [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="eafca-162">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="eafca-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="eafca-163">Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="eafca-164">여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="eafca-165">Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="eafca-166">`-RequiredVersion` 인수를 사용하여 `Az` 모듈의 특정 버전을 설치하거나 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="eafca-167">모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="eafca-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="eafca-168">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="eafca-168">Provide feedback</span></span>

<span data-ttu-id="eafca-169">Azure Powershell에서 버그 발생 시, [ GitHub에서 문제를 제출](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="eafca-170">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eafca-171">다음 단계</span><span class="sxs-lookup"><span data-stu-id="eafca-171">Next Steps</span></span>

<span data-ttu-id="eafca-172">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="eafca-173">Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eafca-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
