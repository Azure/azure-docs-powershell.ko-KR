---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329882"
---
# <span data-ttu-id="ac215-101">Az.MarketplaceOrdering 모듈</span><span class="sxs-lookup"><span data-stu-id="ac215-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="ac215-102">설명</span><span class="sxs-lookup"><span data-stu-id="ac215-102">Description</span></span>
<span data-ttu-id="ac215-103">이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크의 Azure MarketplaceOrdering용 Azure PowerShell cmdlet을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="ac215-104">cmdlet은 Microsoft.Azure.Commands.MarketplaceOrdering 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="ac215-105">이러한 cmdlet을 사용하면 Azure 사용자가 이러한 솔루션에 대한 프로그래밍식 배포를 추가로 허용하는 마켓플레이스 제안에 대한 약관에 동의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="ac215-106">사용자는 이미 동의한 약관 집합을 거부할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="ac215-107">Az.MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac215-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="ac215-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ac215-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="ac215-109">제공된 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름)에 대한 계약 조건을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ac215-110">이 명령에서 반환되는 용어 개체는 약관에 동의하기 위해 Set-AzMarketplaceTerms 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="ac215-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ac215-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="ac215-112">제공된 게시자 ID(퍼블리셔), 제품 ID(제품) 및 계획 ID(이름)에 대한 약관에 동의하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ac215-113">계약 조건을 Get-AzMarketplaceTerms 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="ac215-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

