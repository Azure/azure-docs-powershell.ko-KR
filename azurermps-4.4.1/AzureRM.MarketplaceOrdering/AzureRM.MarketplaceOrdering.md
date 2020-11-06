---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: f1446494d4eb68195ec0cefba248f519039a91ce
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522363"
---
# <span data-ttu-id="2d278-101">MarketplaceOrdering 모듈 AzureRM</span><span class="sxs-lookup"><span data-stu-id="2d278-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="2d278-102">설명은</span><span class="sxs-lookup"><span data-stu-id="2d278-102">Description</span></span>
<span data-ttu-id="2d278-103">이 섹션의 항목에서는 MarketplaceOrdering (Azure Resource Manager) 프레임 워크에서 Azure for의 azure PowerShell cmdlet을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="2d278-104">MarketplaceOrdering 네임 스페이스에 cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="2d278-105">이러한 cmdlet을 사용 하 여 azure 사용자는 이러한 솔루션에 대 한 사용자의 구현에 대 한 해당 조항에 대 한 적절 한 조항을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmtic deployment for these solutions.</span></span> <span data-ttu-id="2d278-106">사용자는 이미 수락 된 약관의 집합을 거부할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="2d278-107">MarketplaceOrdering Cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="2d278-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="2d278-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="2d278-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="2d278-109">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 계약 조건을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="2d278-110">이 명령으로 반환 되는 약관 개체는 약관에 동의 하도록 Set-AzureRmMarketplaceTerms에 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="2d278-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="2d278-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="2d278-112">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 약관을 적용 하거나 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d278-112">Accept or reject the legal terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="2d278-113">Get-AzureRmMarketplaceTerms를 사용 하 여 약관에 동의 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d278-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

