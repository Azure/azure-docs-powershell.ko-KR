---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93688840"
---
# <span data-ttu-id="54353-101">Az MarketplaceOrdering 모듈</span><span class="sxs-lookup"><span data-stu-id="54353-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="54353-102">설명은</span><span class="sxs-lookup"><span data-stu-id="54353-102">Description</span></span>
<span data-ttu-id="54353-103">이 섹션의 항목에서는 MarketplaceOrdering (Azure Resource Manager) 프레임 워크에서 Azure for의 azure PowerShell cmdlet을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="54353-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="54353-104">MarketplaceOrdering 네임 스페이스에 cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54353-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="54353-105">이러한 cmdlet을 통해 azure 사용자는 이러한 솔루션에 대 한 프로그래밍 방식의 배포를 추가로 허용 하 여 marketplace에 대 한 법적 약관을 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54353-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="54353-106">사용자는 이미 수락 된 약관의 집합을 거부할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54353-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="54353-107">Az MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54353-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="54353-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="54353-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="54353-109">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 계약 조건을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54353-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="54353-110">이 명령으로 반환 되는 약관 개체는 약관에 동의 하도록 Set-AzMarketplaceTerms에 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54353-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="54353-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="54353-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="54353-112">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 조건을 적용 하거나 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="54353-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="54353-113">Get-AzMarketplaceTerms를 사용 하 여 약관에 동의 하세요.</span><span class="sxs-lookup"><span data-stu-id="54353-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

