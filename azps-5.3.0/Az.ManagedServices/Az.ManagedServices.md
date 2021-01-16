---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493404"
---
# <span data-ttu-id="79ba4-101">Az.ManagedServices 모듈</span><span class="sxs-lookup"><span data-stu-id="79ba4-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="79ba4-102">설명</span><span class="sxs-lookup"><span data-stu-id="79ba4-102">Description</span></span>
<span data-ttu-id="79ba4-103">이 기능은 MSP(관리 서비스 공급자)의 고객이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="79ba4-104">고객은 MSP에 구독 또는 리소스 그룹을 관리하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="79ba4-105">고객은 액세스 권한을 부여하는 것 외에도 액세스 권한을 제거하거나 기존 액세스를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="79ba4-106">MSP는 구독에 대한 액세스 권한을 부여한 고객 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="79ba4-107">이 프로세스에는 MSP 사용자에게 부여된 MSP 및 역할 정의를 식별하는 등록 정의와 같은 두 가지 개체가 관련됩니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="79ba4-108">MSP는 선택적으로 구독을 정의와 연결되는 액세스 할당을 제공하는 Managed Services 마켓플레이스를 사용하여 이 개체를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="79ba4-109">Az.ManagedServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="79ba4-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="79ba4-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="79ba4-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="79ba4-111">특정 등록 할당 또는 등록 할당 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="79ba4-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="79ba4-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="79ba4-113">특정 등록 정의 또는 등록 정의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="79ba4-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="79ba4-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="79ba4-115">등록 할당을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="79ba4-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="79ba4-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="79ba4-117">등록 정의를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="79ba4-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="79ba4-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="79ba4-119">등록 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="79ba4-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="79ba4-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="79ba4-121">등록 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="79ba4-121">Removes a registration definition.</span></span>
