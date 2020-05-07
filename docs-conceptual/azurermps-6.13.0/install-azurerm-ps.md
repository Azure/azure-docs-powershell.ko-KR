---
title: PowerShellGet으로 Azure PowerShell을 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 5de386bde1b8be5a4455b85d4f5fcdf38e4fcea2
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535010"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="0ac4b-103">PowerShellGet으로 Azure PowerShell을 설치</span><span class="sxs-lookup"><span data-stu-id="0ac4b-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="0ac4b-104">이 아티클에서는 PowerShellGet을 사용하여 Windows용 PowerShell 5.x용 Azure PowerShell 모듈을 설치하는 단계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="0ac4b-105">PowerShellGet 및 모듈 관리는 Azure PowerShell을 설치하는 더 좋은 방법이지만 대신 웹 플랫폼 설치 관리자 또는 MSI 패키지로 설치하려는 경우 [다른 설치 방법](other-install.md)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="0ac4b-106">Azure 클래식 배포 모델은 본 버전의 Azure PowerShell에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="0ac4b-107">클래식 배포에 대한 지원은 [Azure PowerShell Service Management 모듈 설치](/powershell/azure/servicemanagement/install-azure-ps) 지침을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ac4b-108">MacOS 또는 Linux 용 AzureRM 모듈은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="0ac4b-109">이러한 플랫폼에서 Azure PowerShell cmdlet을 사용하려면 [Az 모듈을 설치](/powershell/azure/install-az-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac4b-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="0ac4b-110">Requirements</span></span>

<span data-ttu-id="0ac4b-111">Azure PowerShell 버전 6.0부터 Azure PowerShell은 PowerShell 버전 5.0이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="0ac4b-112">시스템의 PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="0ac4b-113">만료된 버전을 사용하는 경우 [기존 Windows PowerShell 업그레이드](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ac4b-114">이 문서에서 설명된 모듈인 AzureRM에서는 .NET Framework를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="0ac4b-115">이렇게 하면 .NET Core를 사용하는 PowerShell 6.0과 호환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="0ac4b-116">PowerShell 6.0을 사용하는 경우, [macOS 및 Linux에 대한 설치 지침](install-azurermps-maclinux.md)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="0ac4b-117">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="0ac4b-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="0ac4b-118">PowerShell 갤러리에서 모듈을 설치하려면 상승된 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="0ac4b-119">Azure PowerShell을 설치하려면 승격된 세션에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="0ac4b-120">NuGet 2.8.5.201 이전 버전을 사용하는 경우 최신 버전의 NuGet을 다운로드하여 설치하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="0ac4b-121">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0ac4b-122">PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-122">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="0ac4b-123">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="0ac4b-124">`AzureRM` 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="0ac4b-125">설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="0ac4b-126">로그인</span><span class="sxs-lookup"><span data-stu-id="0ac4b-126">Sign in</span></span>

<span data-ttu-id="0ac4b-127">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="0ac4b-128">모듈 자동 로딩을 비활성화한 경우 `Import-Module AzureRM`을 사용하여 모듈을 수동으로 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="0ac4b-129">모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-129">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="0ac4b-130">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="0ac4b-131">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="0ac4b-132">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="0ac4b-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="0ac4b-133">[Update-Module](/powershell/module/powershellget/update-module)을 실행하여 Azure PowerShell 설치를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="0ac4b-134">이 명령은 이전 버전을 제거하지 __않습니다__.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-134">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="0ac4b-135">Azure PowerShell의 이전 버전을 시스템에서 제거하려면, [Azure PowerShell 모듈 제거](uninstall-azurerm-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="0ac4b-136">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="0ac4b-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="0ac4b-137">Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="0ac4b-138">여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="0ac4b-139">Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-azurerm-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="0ac4b-140">온-프레미스 Azure Stack 리소스로 작업하거나 이전 버전의 Windows를 실행하거나 Azure 클래식 배포 모델을 사용하는 경우 둘 이상의 버전이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="0ac4b-141">이전 버전을 설치하려면 `-RequiredVersion` 인수를 설치 시 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="0ac4b-142">Azure PowerShell 모듈 로드 시, 기본으로 최신 버전이 로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="0ac4b-143">다른 버전을 로드하려면 `-RequiredVersion` 인수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="0ac4b-144">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="0ac4b-144">Provide feedback</span></span>

<span data-ttu-id="0ac4b-145">Azure Powershell 사용 중 버그 발생 시, [ GitHub에서 문제를 제출](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="0ac4b-146">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0ac4b-147">다음 단계</span><span class="sxs-lookup"><span data-stu-id="0ac4b-147">Next Steps</span></span>

<span data-ttu-id="0ac4b-148">Azure PowerShell 사용을 시작하려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하여 모듈 및 모듈의 기능에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
