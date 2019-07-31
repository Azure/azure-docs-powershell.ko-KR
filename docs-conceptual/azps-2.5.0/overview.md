---
title: Azure PowerShell 개요
description: 설치 방법 및 시작 방법에 대한 정보가 담긴 Azure PowerShell Az 모듈의 개요입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657623"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="d8258-103">Azure PowerShell 개요</span><span class="sxs-lookup"><span data-stu-id="d8258-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="d8258-104">Azure PowerShell은 Azure 리소스를 관리하기 위해 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 모델을 사용하는 cmdlet 집합을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="d8258-105">Azure PowerShell은.NET 표준을 사용하여 Windows, macOS 및 Linux에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="d8258-106">Azure PowerShell은 Azure Cloud Shell에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="d8258-107">새 Az 모듈 정보</span><span class="sxs-lookup"><span data-stu-id="d8258-107">About the new Az module</span></span>

<span data-ttu-id="d8258-108">이 설명서에서는 Azure PowerShell을 위한 새 Az 모듈을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="d8258-109">이 새 모듈은.NET 표준으로 처음부터 작성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="d8258-110">.NET Standard를 사용하면 Azure PowerShell을 Windows의 PowerShell 5.1 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="d8258-111">Az 모듈은 이제 PowerShell을 통해 Azure와 상호 작용하도록 의도된 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="d8258-112">AzureRM의 버그 수정은 계속되지만, 새로운 기능은 더 이상 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="d8258-113">[Azure PowerShell Az 모듈 소개](new-azureps-module-az.md)에서 명령의 이름이 변경된 내용과 AzureRM의 유지 관리 계획을 포함하여 새 모듈에 대한 자세한 내용을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="d8258-114">지금 바로 새 모듈을 사용하여 시작하려는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="d8258-115">[AzureRM 설명서](/powershell/azure/azurerm)도 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d8258-116">Azure 설명서가 새로운 모듈 cmdlet 이름을 반영하도록 업데이트되는 동안 아티클은 여전히 AzureRM 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="d8258-117">Az 모듈을 설치한 후 `Enable-AzureRmAlias`를 사용하여 AzureRM cmdlet 별칭을 사용하도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="d8258-118">자세한 내용은 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8258-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="d8258-119">실행 또는 설치</span><span class="sxs-lookup"><span data-stu-id="d8258-119">Run or install</span></span>

<span data-ttu-id="d8258-120">Azure PowerShell은 Windows의 PowerShell 5.1 이상 및 모든 플랫폼의 PowerShell Core 6.x 이상에 설치하거나 Azure Cloud Shell에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="d8258-121">Azure Cloud Shell을 사용하여 브라우저에서 실행하려면 [Azure Cloud Shell에서 PowerShell 빠른 시작](/azure/cloud-shell/quickstart-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8258-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="d8258-122">시스템에 Azure PowerShell을 설치하려면 [Azure PowerShell 설치](install-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="d8258-123">Azure PowerShell 최신 릴리스에 대한 자세한 내용은 [릴리스 정보](release-notes-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8258-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="d8258-124">시작</span><span class="sxs-lookup"><span data-stu-id="d8258-124">Get Started</span></span>

<span data-ttu-id="d8258-125">[Azure PowerShell 시작하기](get-started-azureps.md) 아티클을 읽고 Azure PowerShell 기본 사항을 배워보세요.</span><span class="sxs-lookup"><span data-stu-id="d8258-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="d8258-126">PowerShell에 대해 익숙하지 않으면 소개가 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="d8258-127">PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="d8258-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="d8258-128">PowerShell 스크립팅</span><span class="sxs-lookup"><span data-stu-id="d8258-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="d8258-129">PowerShell 기본 사항: (파트 1)PowerShell 시작</span><span class="sxs-lookup"><span data-stu-id="d8258-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

<span data-ttu-id="d8258-130">다음 예제는 Azure의 일반적인 사용법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8258-130">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="d8258-131">Linux Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="d8258-131">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d8258-132">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="d8258-132">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d8258-133">Web Apps</span><span class="sxs-lookup"><span data-stu-id="d8258-133">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d8258-134">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="d8258-134">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="d8258-135">Microsoft Learn을 통해 기술 쌓기</span><span class="sxs-lookup"><span data-stu-id="d8258-135">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="d8258-136">PowerShell을 사용하여 스크립트로 Azure 작업 자동화</span><span class="sxs-lookup"><span data-stu-id="d8258-136">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="d8258-137">더 많은 대화형 학습 보기...</span><span class="sxs-lookup"><span data-stu-id="d8258-137">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="d8258-138">다른 Azure PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="d8258-138">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="d8258-139">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d8258-139">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="d8258-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d8258-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="d8258-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="d8258-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
