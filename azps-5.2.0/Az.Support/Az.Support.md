---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349082"
---
# <span data-ttu-id="c90d1-101">Az.Support 모듈</span><span class="sxs-lookup"><span data-stu-id="c90d1-101">Az.Support Module</span></span>
## <span data-ttu-id="c90d1-102">설명</span><span class="sxs-lookup"><span data-stu-id="c90d1-102">Description</span></span>
<span data-ttu-id="c90d1-103">이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크에서 Azure 지원 티켓을 만들고 관리하기 위한 Azure PowerShell cmdlet을 문서화합니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c90d1-104">cmdlet은 Microsoft.Azure.Commands.Support 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="c90d1-105">Az.Support Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c90d1-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="c90d1-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="c90d1-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="c90d1-107">지원을 사용할 수 있는 Azure 서비스의 현재 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="c90d1-108">각 Azure 서비스에는 문제 분류라는 자체 범주 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="c90d1-109">Get-AzSupportProblemClassification을 사용하여 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="c90d1-110">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="c90d1-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="c90d1-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="c90d1-112">Azure 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="c90d1-113">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="c90d1-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="c90d1-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="c90d1-115">지원 연락처 프로필 개체를 만드는 도우미 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="c90d1-116">이 개체는 cmdlet에 New-AzSupportTicket 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="c90d1-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c90d1-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="c90d1-118">새 Azure 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="c90d1-119">이 작업은 Azure 새 지원 요청 페이지의 동작을 [모델링합니다.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="c90d1-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="c90d1-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c90d1-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="c90d1-121">지원 티켓 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-121">Gets the list of support tickets.</span></span> <span data-ttu-id="c90d1-122">티켓 이름으로 전체 지원 티켓 세부 정보를 얻거나  상태 또는 *CreatedDate를* 통해 지원 티켓을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="c90d1-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c90d1-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="c90d1-124">지원 티켓의 심각도, 상태 또는 고객 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="c90d1-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c90d1-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="c90d1-126">지원 티켓에 대한 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="c90d1-127">*CreatedDate* 또는 *CommunicationType을* 통해 지원 티켓 통신을 필터링할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="c90d1-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c90d1-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="c90d1-129">Azure 지원 티켓에 새 고객 통신을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c90d1-129">Adds a new customer communication to an Azure support ticket.</span></span> 



