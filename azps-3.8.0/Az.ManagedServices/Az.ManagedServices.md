---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044202"
---
# <span data-ttu-id="7c2ab-101">Az Services 모듈</span><span class="sxs-lookup"><span data-stu-id="7c2ab-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="7c2ab-102">설명은</span><span class="sxs-lookup"><span data-stu-id="7c2ab-102">Description</span></span>
<span data-ttu-id="7c2ab-103">이 기능은 MSPs (관리 서비스 공급자)의 고객이 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="7c2ab-104">고객은 MSP에 구독을 관리 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="7c2ab-105">고객은 액세스를 허용 하는 것 외에도 액세스를 제거 하거나 기존 액세스 위임을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="7c2ab-106">MSPs는 구독에 대 한 액세스 권한을 부여한 고객 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="7c2ab-107">이 프로세스에는 MSP 및 MSP에 부여 된 역할 정의를 식별 하는 등록 정의가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="7c2ab-108">MSP는 구독을 정의와 연결 하는 액세스 할당을 제공 하는 관리 서비스 마켓플레이스를 사용 하 여이 개체를 선택적으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="7c2ab-109">Az 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7c2ab-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="7c2ab-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ab-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="7c2ab-111">등록 과제의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="7c2ab-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c2ab-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="7c2ab-113">등록 정의의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="7c2ab-114">새로운 AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ab-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="7c2ab-115">등록 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="7c2ab-116">새로운 AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c2ab-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="7c2ab-117">등록 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="7c2ab-118">제거-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ab-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="7c2ab-119">등록 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="7c2ab-120">제거-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c2ab-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="7c2ab-121">등록 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-121">Deletes the registration definition.</span></span>

