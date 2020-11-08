---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204703"
---
# <span data-ttu-id="fe856-101">Az 지원 모듈</span><span class="sxs-lookup"><span data-stu-id="fe856-101">Az.Support Module</span></span>
## <span data-ttu-id="fe856-102">설명은</span><span class="sxs-lookup"><span data-stu-id="fe856-102">Description</span></span>
<span data-ttu-id="fe856-103">이 섹션의 항목에서는 azure Resource Manager (ARM) 프레임 워크에서 Azure 지원 티켓을 만들고 관리 하기 위한 Azure PowerShell cmdlet을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="fe856-104">이 cmdlet은 Microsoft Azure. 명령인. 지원 네임 스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="fe856-105">Az 지원 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe856-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="fe856-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="fe856-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="fe856-107">지원을 사용할 수 있는 현재 Azure services 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="fe856-108">각 Azure 서비스에는 고유한 범주 집합 (문제 분류 라고 함)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="fe856-109">Get-AzSupportProblemClassification를 사용 하 여 서비스에 대 한 최신 문제 분류 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="fe856-110">서비스 및 문제 분류 GUID를 사용 하 여 새 AzSupportTicket를 사용 하 여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="fe856-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="fe856-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="fe856-112">Azure 서비스에 대 한 문제 분류의 현재 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="fe856-113">서비스 및 문제 분류 GUID를 사용 하 여 새 AzSupportTicket를 사용 하 여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="fe856-114">새로운 AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="fe856-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="fe856-115">도우미 cmdlet을 통해 지원 연락처 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="fe856-116">New-AzSupportTicket cmdlet에이 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="fe856-117">새로운 AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe856-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="fe856-118">새 Azure 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="fe856-119">이 작업은 Azure [새 지원 요청 페이지](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)의 동작을 모델링 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="fe856-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe856-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="fe856-121">지원 티켓 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-121">Gets the list of support tickets.</span></span> <span data-ttu-id="fe856-122">티켓 이름에 따라 전체 지원 티켓을 가져오거나 *상태* 또는 *CreatedDate* 지원 티켓을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="fe856-123">업데이트-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe856-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="fe856-124">지원 티켓의 심각도, 상태 또는 고객 연락처 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="fe856-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="fe856-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="fe856-126">지원 티켓에 대 한 통신을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="fe856-127">*CreatedDate*   또는 *CommunicationType* 에서 지원 티켓 통신을 필터링 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="fe856-128">새로운 AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="fe856-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="fe856-129">Azure 지원 티켓에 새 고객 통신을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe856-129">Adds a new customer communication to an Azure support ticket.</span></span> 



