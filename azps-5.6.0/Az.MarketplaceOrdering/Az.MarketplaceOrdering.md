---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991060"
---
# <span data-ttu-id="71cd8-101">Az.MarketplaceOrdering 모듈</span><span class="sxs-lookup"><span data-stu-id="71cd8-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="71cd8-102">설명</span><span class="sxs-lookup"><span data-stu-id="71cd8-102">Description</span></span>
<span data-ttu-id="71cd8-103">이 섹션의 항목에서는 Azure Resource Manager(Azure Resource Manager) 프레임워크에서 Azure MarketplaceOrdering용 Azure PowerShell cmdlet을 ARM 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="71cd8-104">cmdlet은 Microsoft.Azure.Commands.MarketplaceOrdering 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="71cd8-105">이러한 cmdlet을 사용하면 Azure 사용자가 이러한 솔루션에 대한 프로그래밍식 배포를 추가로 허용하는 마켓플레이스에 대한 법적 용어를 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="71cd8-106">사용자는 이미 수락된 법적 용어 집합을 거부할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="71cd8-107">Az.MarketplaceOrdering Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71cd8-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="71cd8-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="71cd8-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="71cd8-109">주어진 게시자 ID(Publisher), 제품 ID(제품) 및 계획 ID(이름)에 대한 계약 조건을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="71cd8-110">이 명령에서 반환되는 용어 개체는 법적 Set-AzMarketplaceTerms 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="71cd8-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="71cd8-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="71cd8-112">주어진 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름)에 대한 약관을 수락하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="71cd8-113">계약 조건을 Get-AzMarketplaceTerms 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="71cd8-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

