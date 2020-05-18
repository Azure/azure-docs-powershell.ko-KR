---
title: Azure PowerShell을 설치하는 다른 방법
description: PowerShellGet을 사용하지 않고 Azure PowerShell을 설치하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: aaba0ce38129b96e3d691f1a9d9cfdc929188ffd
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722410"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="5b354-103">MSI 또는 웹 플랫폼 설치 관리자를 사용하여 Windows에 Azure PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="5b354-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="5b354-104">이 문서에서는 MSI 또는 웹 플랫폼 설치 관리자(WebPI)를 사용하여 Azure PowerShell을 Windows에 설치하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="5b354-105">시스템에 필요한 경우에만 이러한 설치 방법을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="5b354-106">Windows에 Azure PowerShell 설치에는 PowerShellGet을 사용하는 방법이 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="5b354-107">PowerShellGet을 사용하여 Azure PowerShell을 설치하는 방법은 [PowerShellGet으로 Azure PowerShell 설치하기](install-azurerm-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="5b354-108">MSI 패키지를 사용하여 Windows에 설치 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b354-108">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="5b354-109">Azure PowerShell은 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018)에서 사용할 수 있는 MSI 파일을 사용하여 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-109">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="5b354-110">이전 버전의 Azure 모듈이 MSI로 설치된 경우 설치 관리자에서 자동으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-110">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="5b354-111">MSI 패키지는 `${env:ProgramFiles}\WindowsPowerShell\Modules`에서 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-111">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="5b354-112">`AzureRM` 및 `Azure` 모듈 모두 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-112">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="5b354-113">Azure 클래식 배포 모델을 사용하는 경우 `Azure` 모듈만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-113">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="5b354-114">Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-114">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="5b354-115">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-115">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5b354-116">`AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-116">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="5b354-117">Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-117">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="5b354-118">웹 플랫폼 설치 관리자를 사용하여 Windows에 설치 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b354-118">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="5b354-119">[Azure PowerShell WebPI 패키지](https://aka.ms/webpi-azps)를 다운로드하고 설치를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-119">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="5b354-120">이전 버전의 Azure 모듈이 MSI로부터 또는 WebPI로 설치된 경우 설치 관리자에서 자동으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-120">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="5b354-121">모듈이 `${env:ProgramFiles}\WindowsPowerShell\Modules`에 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-121">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="5b354-122">`AzureRM` 및 `Azure` 모듈 모두 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-122">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="5b354-123">Azure 클래식 배포 모델을 사용하는 경우 `Azure` 모듈만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-123">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="5b354-124">Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-124">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="5b354-125">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5b354-126">`AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-126">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="5b354-127">Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5b354-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>