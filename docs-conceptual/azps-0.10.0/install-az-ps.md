---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: c6767d99690a04d1001dd76a218cc90c9cecca39
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409887"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="5d5d1-103">Azure Powershell 설치</span><span class="sxs-lookup"><span data-stu-id="5d5d1-103">Install Azure PowerShell</span></span>

<span data-ttu-id="5d5d1-104">이 문서에서는 [PowerShellGet](/powershell/scripting/gallery/installing-psget)을 사용하여 Azure PowerShell 모듈을 설치하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="5d5d1-105">이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="5d5d1-106">Azure PowerShell은 Azure [Cloud Shell](/azure/cloud-shell/overview)에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d5d1-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="5d5d1-107">Requirements</span></span>

<span data-ttu-id="5d5d1-108">Azure PowerShell은 Windows의 PowerShell 5.1 이상 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="5d5d1-109">운영 체제에 사용할 수 있는 [최신 버전의 PowerShell](/powershell/scripting/install/installing-powershell)을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-109">You should install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="5d5d1-110">PowerShell 6.2.4 이상에서 실행하는 경우 Azure PowerShell과 관련된 추가 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-110">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="5d5d1-111">PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-111">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="5d5d1-112">Windows의 PowerShell 5.1에서 Azure PowerShell을 사용하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="5d5d1-113">[Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="5d5d1-114">Windows 10 버전 1607 이상을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-114">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="5d5d1-115">[.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="5d5d1-116">최신 버전의 PowerShellGet이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="5d5d1-117">`Install-Module -Name PowerShellGet -Force`을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-117">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="5d5d1-118">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="5d5d1-118">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="5d5d1-119">Windows에서 PowerShell 5.1용 AzureRM과 Az 모듈을 동시에 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-119">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="5d5d1-120">시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell 6.2.4 이상용 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-120">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="5d5d1-121">기본 설치 방법은 PowerShellGet cmdlet을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-121">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="5d5d1-122">현재 사용자에 대해서만 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-122">Install the Az module for the current user only.</span></span> <span data-ttu-id="5d5d1-123">이는 추천되는 설치 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-123">This is the recommended installation scope.</span></span> <span data-ttu-id="5d5d1-124">이 방법은 Windows, macOS 및 Linux 플랫폼에서 동일하게 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-124">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="5d5d1-125">PowerShell 세션에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-125">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="5d5d1-126">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-126">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="5d5d1-127">PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="5d5d1-128">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-128">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="5d5d1-129">시스템의 모든 사용자에 대해 모듈을 설치하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-129">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="5d5d1-130">Windows에서 **관리자 권한으로 실행** 을 사용하여 PowerShell 세션을 시작하거나 macOS 또는 Linux에서 `sudo` 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-130">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="5d5d1-131">Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-131">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5d5d1-132">이 모듈을 설치하면 갤러리의 모든 사용 가능한 Az PowerShell 모듈이 다운로드되고, cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-132">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="5d5d1-133">오프라인 설치</span><span class="sxs-lookup"><span data-stu-id="5d5d1-133">Install offline</span></span>

<span data-ttu-id="5d5d1-134">일부 환경에서는 PowerShell 갤러리에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-134">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="5d5d1-135">이러한 경우에도 다음 방법 중 하나를 사용하여 오프라인으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-135">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="5d5d1-136">모듈을 네트워크의 다른 위치에 다운로드하여 이 모듈을 네트워크의 설치 원본으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-136">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="5d5d1-137">이 방법을 사용하면 단일 서버 또는 파일 공유에서 PowerShell 모듈을 캐시하여 PowerShellGet을 사용하여 연결이 끊긴 시스템에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-137">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="5d5d1-138">[로컬 PowerShellGet 리포지토리로 작업](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)을 통해 로컬 리포지토리를 설정하고 연결이 끊어진 시스템에 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-138">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="5d5d1-139">네트워크에 연결된 컴퓨터에 [Azure PowerShell MSI](install-az-ps-msi.md)를 다운로드한 다음, PowerShell 갤러리에 액세스하지 않고 설치 관리자를 시스템에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-139">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="5d5d1-140">MSI 설치 관리자는 Windows의 PowerShell 5.1에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-140">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="5d5d1-141">[Save-Module](/powershell/module/PowershellGet/Save-Module)을 사용하여 모듈을 파일 공유에 저장하거나 다른 소스에 저장하고 다른 컴퓨터에 수동으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-141">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="5d5d1-142">문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d5d1-142">Troubleshooting</span></span>

<span data-ttu-id="5d5d1-143">Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-143">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="5d5d1-144">여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-144">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="5d5d1-145">프록시 연결 차단</span><span class="sxs-lookup"><span data-stu-id="5d5d1-145">Proxy blocks connection</span></span>

<span data-ttu-id="5d5d1-146">`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-146">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="5d5d1-147">운영 체제와 네트워크 환경에 따라 시스템 수준 프록시 구성에 대한 요구 사항이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-147">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="5d5d1-148">프록시 설정 및 환경에 맞게 구성하는 방법에 대해서는 시스템 관리자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-148">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="5d5d1-149">PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-149">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="5d5d1-150">PowerShell 5.1 이상에서는 다음 명령을 사용하여 프록시를 사용하도록 PowerShell 세션을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-150">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="5d5d1-151">운영 체제 자격 증명이 올바르게 구성되면 이 구성에서 프록시를 통해 PowerShell 요청을 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-151">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="5d5d1-152">이 설정이 세션 간에 유지되도록 하려면 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-152">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="5d5d1-153">패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-153">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="5d5d1-154">로그인</span><span class="sxs-lookup"><span data-stu-id="5d5d1-154">Sign in</span></span>

<span data-ttu-id="5d5d1-155">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-155">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="5d5d1-156">모듈 자동 로딩을 비활성화한 경우 `Import-Module -Name Az`을 사용하여 모듈을 수동으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-156">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="5d5d1-157">모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-157">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="5d5d1-158">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-158">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5d5d1-159">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-159">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="5d5d1-160">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d5d1-160">Update the Azure PowerShell module</span></span>

<span data-ttu-id="5d5d1-161">PowerShell 모듈을 업데이트하려면 모듈을 설치하는 데 사용한 것과 동일한 방법을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-161">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="5d5d1-162">예를 들어 처음에 `Install-Module`을 사용한 경우 [Update-Module](/powershell/module/powershellget/update-module)을 사용하여 최신 버전을 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-162">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="5d5d1-163">처음에 MSI 패키지를 사용한 경우 새 MSI 패키지를 다운로드하여 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-163">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="5d5d1-164">PowerShellGet cmdlet은 MSI 패키지에서 설치된 모듈을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-164">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="5d5d1-165">MSI 패키지는 PowerShellGet을 사용하여 설치한 모듈을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-165">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="5d5d1-166">PowershellGet을 사용하여 업데이트하는 데 문제가 있는 경우 **업데이트** 하는 대신 **다시 설치** 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-166">If you have any issues updating using PowershellGet, then you should **reinstall** , rather than **update**.</span></span> <span data-ttu-id="5d5d1-167">다시 설치는 설치와 동일한 방식으로 수행되지만 `-Force` 매개 변수를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-167">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="5d5d1-168">MSI 기반 설치와 달리 PowerShellGet을 사용하여 설치하거나 업데이트해도 시스템에 있을 수 있는 이전 버전은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-168">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="5d5d1-169">시스템에서 이전 버전의 Azure PowerShell을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-169">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="5d5d1-170">MSI 기반 설치에 대한 자세한 내용은 [MSI를 사용하여 Azure PowerShell 설치](install-az-ps-msi.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-170">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="5d5d1-171">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="5d5d1-171">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="5d5d1-172">Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-172">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="5d5d1-173">여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-173">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="5d5d1-174">Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-174">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="5d5d1-175">모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-175">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="5d5d1-176">`-RequiredVersion` 매개 변수를 사용하여 특정 버전의 `Az` 모듈을 설치하거나 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-176">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="5d5d1-177">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="5d5d1-177">Provide feedback</span></span>

<span data-ttu-id="5d5d1-178">버그가 Azure PowerShell에 있으면 [GitHub에서 문제를 제기](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-178">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="5d5d1-179">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-179">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5d5d1-180">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5d5d1-180">Next Steps</span></span>

<span data-ttu-id="5d5d1-181">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-181">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="5d5d1-182">Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-182">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
