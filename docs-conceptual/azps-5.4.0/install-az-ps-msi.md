---
title: MSI로 Azure PowerShell 설치
description: PowerShellGet을 사용하지 않고 MSI를 사용하여 Azure PowerShell을 설치하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573757"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="b9369-103">MSI로 Windows에 Azure PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="b9369-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="b9369-104">이 문서에서는 MSI를 사용하여 Azure PowerShell을 Windows에 설치하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="b9369-105">MSI 설치 관리자는 PowerShell 갤러리가 방화벽에 의해 차단될 수 있거나 오프라인 설치 관리자가 필요한 환경에 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="b9369-106">Azure PowerShell 설치에는 PowerShellGet을 사용하는 방법이 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="b9369-107">PowerShellGet을 사용하여 Azure PowerShell을 설치하는 방법은 [PowerShellGet으로 Azure PowerShell 설치하기](install-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9369-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b9369-108">Requirements</span></span>

<span data-ttu-id="b9369-109">Windows의 MSI 설치 관리자는 PowerShell 5.1용 Azure PowerShell만 설치하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="b9369-110">Windows 이외의 플랫폼 또는 이후 버전의 PowerShell에 설치하려면 [PowerShellGet을 사용하여 설치](install-az-ps.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="b9369-111">PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="b9369-112">PowerShell 5.1에서 Azure PowerShell을 사용하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="b9369-113">필요한 경우 [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="b9369-114">Windows 10을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="b9369-115">[.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="b9369-116">MSI 패키지를 사용하여 Windows에 설치 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="b9369-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="b9369-117">Azure PowerShell용 MSI 패키지는 [GitHub](https://github.com/Azure/azure-powershell/releases)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="b9369-118"> https://github.com/Azure/azure-powershell/releases로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="b9369-119">Azure PowerShell용 최신 갤러리 모듈을 찾으세요(이러한 모듈은 시간순으로 나열되어 있으며 일반적으로 "4.7.0"처럼 이름 없는 릴리스 버전입니다).</span><span class="sxs-lookup"><span data-stu-id="b9369-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="b9369-120">패치 노트의 아래쪽으로 스크롤한 다음, "자산" 옆의 화살표를 클릭하여 MSI 옵션을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="b9369-121">원하는 Az-Cmdlets MSI를 클릭하여 다운로드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="b9369-122">MSI를 사용하여 이전 버전의 Azure PowerShell 모듈을 설치한 경우 설치 관리자에서 자동으로 이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="b9369-123">MSI 패키지는 `${env:ProgramFiles}\WindowsPowerShell\Modules`에서 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="b9369-124">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="b9369-125">모듈 자동 로딩을 비활성화한 경우 `Import-Module Az`을 사용하여 모듈을 수동으로 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="b9369-126">모듈 구조화 방식으로 인해 최대 1분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="b9369-127">모든 새 PowerShell 세션에 대해 이 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9369-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="b9369-128">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9369-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="b9369-129">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="b9369-129">Provide feedback</span></span>

<span data-ttu-id="b9369-130">버그가 Azure PowerShell에 있으면 [GitHub에서 문제를 제기](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="b9369-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="b9369-131">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="b9369-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b9369-132">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b9369-132">Next Steps</span></span>

<span data-ttu-id="b9369-133">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9369-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="b9369-134">Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9369-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
