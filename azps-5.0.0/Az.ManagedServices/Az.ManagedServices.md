---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217692"
---
# <span data-ttu-id="685a6-101">Az Services 모듈</span><span class="sxs-lookup"><span data-stu-id="685a6-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="685a6-102">설명은</span><span class="sxs-lookup"><span data-stu-id="685a6-102">Description</span></span>
<span data-ttu-id="685a6-103">이 기능은 MSPs (관리 서비스 공급자)의 고객이 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="685a6-104">고객은 구독 또는 리소스 그룹을 관리 하는 기능을 MSP에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="685a6-105">액세스를 허용 하는 것 외에도 고객은 액세스를 제거 하거나 기존 액세스를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="685a6-106">MSPs는 구독에 대 한 액세스 권한을 부여한 고객 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="685a6-107">이 프로세스에는 msp 사용자에 게 부여 되는 .MSP 및 역할 정의를 식별 하는 등록 정의가 두 가지로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="685a6-108">MSP는 구독을 정의와 연결 하는 액세스 할당을 제공 하는 관리 서비스 마켓플레이스를 사용 하 여이 개체를 선택적으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="685a6-109">Az 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="685a6-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="685a6-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="685a6-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="685a6-111">특정 등록 할당 또는 등록 할당 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="685a6-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="685a6-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="685a6-113">특정 등록 정의 또는 등록 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="685a6-114">새로운 AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="685a6-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="685a6-115">등록 과제를 작성 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="685a6-116">새로운 AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="685a6-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="685a6-117">등록 정의를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="685a6-118">제거-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="685a6-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="685a6-119">등록 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="685a6-120">제거-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="685a6-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="685a6-121">등록 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="685a6-121">Removes a registration definition.</span></span>
