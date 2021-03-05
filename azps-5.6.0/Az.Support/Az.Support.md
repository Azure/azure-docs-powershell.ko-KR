---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979115"
---
# <span data-ttu-id="5b265-101">Az.Support 모듈</span><span class="sxs-lookup"><span data-stu-id="5b265-101">Az.Support Module</span></span>
## <span data-ttu-id="5b265-102">설명</span><span class="sxs-lookup"><span data-stu-id="5b265-102">Description</span></span>
<span data-ttu-id="5b265-103">이 섹션의 항목에서는 Azure Resource Manager(azure Resource Manager) 프레임워크에서 Azure 지원 티켓을 만들고 관리하기 위한 Azure PowerShell cmdlet을 ARM 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="5b265-104">cmdlet은 Microsoft.Azure.Commands.Support 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="5b265-105">Az.Support Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b265-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="5b265-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="5b265-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="5b265-107">지원이 가능한 Azure 서비스의 현재 목록을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="5b265-108">각 Azure 서비스에는 문제 분류라는 자체 범주 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="5b265-109">Get-AzSupportProblemClassification을 사용하여 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="5b265-110">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="5b265-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="5b265-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="5b265-112">Azure 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="5b265-113">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="5b265-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="5b265-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="5b265-115">도우미 cmdlet을 사용하여 지원 연락처 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="5b265-116">이 개체를 cmdlet에 New-AzSupportTicket 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="5b265-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5b265-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="5b265-118">새 Azure 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="5b265-119">이 작업은 Azure New 지원 요청 페이지의 동작을 [모델링합니다.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="5b265-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="5b265-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5b265-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="5b265-121">지원 티켓 목록을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-121">Gets the list of support tickets.</span></span> <span data-ttu-id="5b265-122">티켓 이름으로 전체 지원 티켓 세부 정보를 얻거나  상태 또는 *CreatedDate로* 지원 티켓을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="5b265-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5b265-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="5b265-124">지원 티켓의 심각도, 상태 또는 고객 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="5b265-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="5b265-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="5b265-126">지원 티켓에 대한 통신을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="5b265-127">*CreatedDate* 또는 CommunicationType 을 사용하여 지원 티켓 통신을 *필터링할 수도 있습니다.*</span><span class="sxs-lookup"><span data-stu-id="5b265-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="5b265-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="5b265-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="5b265-129">Azure 지원 티켓에 새 고객 통신을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b265-129">Adds a new customer communication to an Azure support ticket.</span></span> 



