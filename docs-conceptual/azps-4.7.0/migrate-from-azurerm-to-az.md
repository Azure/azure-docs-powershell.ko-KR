---
title: AzureRM에서 Az로 Azure PowerShell 스크립트 마이그레이션
description: AzureRM 모듈에서 새 Az 모듈로 스크립트를 마이그레이션하는 단계와 도구에 대해 알아보세요.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001564"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="b892d-103">Azure PowerShell을 AzureRM에서 Az로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="b892d-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="b892d-104">모든 버전의 AzureRM PowerShell 모듈이 최신 버전이 아니지만 계속 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="b892d-105">이제는 [Az PowerShell 모듈](install-az-ps.md)이 Azure와 상호 작용하는 데 추천되는 PowerShell 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="b892d-106">AzureRM cmdlet용으로 작성된 스크립트는 새 모듈과 자동으로 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="b892d-107">쉽게 전환할 수 있도록 [AzureRM에서 Az로의 마이그레이션 도구 키트](https://github.com/Azure/azure-powershell-migration)가 개발되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="b892d-108">새 명령 집합으로 마이그레이션은 편리하지 않지만 이 문서는 Az PowerShell 모듈로 전환을 시작하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="b892d-109">Az PowerShell 모듈을 만든 이유에 대한 자세한 내용은 [새로운 Azure PowerShell Az 모듈 소개](new-azureps-module-az.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b892d-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="b892d-110">AzureRM과 Az 간의 호환성이 손상되는 변경의 전체 목록을 보려면 [AzureRM에서 Az으로의 완전한 변경](migrate-az-1.0.0.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b892d-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="b892d-111">기존 스크립트가 최신 AzureRM 릴리스에서 작동하는지 확인</span><span class="sxs-lookup"><span data-stu-id="b892d-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="b892d-112">모든 마이그레이션 단계를 수행하기 전에 시스템에 설치된 AzureRM의 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="b892d-113">이렇게 하면 스크립트가 최신 릴리스에서 이미 실행되고 있는지 확인할 수 있고 제거해야 하는 AzureRM 버전을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="b892d-114">설치한 AzureRM의 버전을 확인하려면 다음 예를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="b892d-115">사용 가능한 **최신** AzureRM 릴리스는 **6.13.1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-115">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="b892d-116">이 버전이 설치되어 있지 않으면 이 문서에서 설명하는 내용과 [호환성이 손상되는 변경 목록](migrate-az-1.0.0.md)에 해당하지 않는 Az 모듈에서 작동하도록 기존 스크립트를 추가로 수정해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="b892d-117">스크립트가 AzureRM 6.13.1에서 작동하지 않으면 [AzureRM 5.x에서 6.x로 마이그레이션 가이드](/powershell/azure/azurerm/migration-guide.6.0.0)에 따라 해당 스크립트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="b892d-118">이전 버전의 AzureRM 모듈을 사용하는 경우 각 주 버전에 사용할 수 있는 마이그레이션 가이드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="b892d-119">AzureRM에서 Az로의 마이그레이션 도구 키트 설치</span><span class="sxs-lookup"><span data-stu-id="b892d-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="b892d-120">PowerShell 스크립트 자동 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="b892d-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="b892d-121">AzureRM에서 Az로의 마이그레이션 도구 키트를 사용하면 스크립트를 수정하기 전과 Az PowerShell 모듈을 설치하기 전에 스크립트에서 수행될 변경 사항을 결정하는 계획을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="b892d-122">[AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션](quickstart-migrate-azurerm-to-az-automatically.md) 빠른 시작은 PowerShell 스크립트를 AzureRM에서 Az PowerShell 모듈로 자동 업데이트하는 전체 프로세스를 안내합니다.</span><span class="sxs-lookup"><span data-stu-id="b892d-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b892d-123">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b892d-123">Next steps</span></span>

<span data-ttu-id="b892d-124">[Azure PowerShell 설치](install-az-ps.md)
[AzureRM 제거](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="b892d-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
