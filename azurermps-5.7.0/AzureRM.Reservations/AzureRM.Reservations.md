---
Module Name: AzureRM.Reservations
Module Guid: 43d3b085-6323-4ac4-a7c3-81d75ea036e5
Download Help Link: ''
Help Version: 1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
ms.openlocfilehash: 10e22af397e5b5861eb9beb043e10abd04e08270
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522748"
---
# <span data-ttu-id="c1c79-101">AzureRM 모듈</span><span class="sxs-lookup"><span data-stu-id="c1c79-101">AzureRM.Reservations Module</span></span>
## <span data-ttu-id="c1c79-102">설명은</span><span class="sxs-lookup"><span data-stu-id="c1c79-102">Description</span></span>
<span data-ttu-id="c1c79-103">이 섹션의 항목에서는 azure 예약에 대 한 azure PowerShell cmdlet에 대 한 e 리소스 관리자 (ARM) 프레임 워크를 문서화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-103">The topics in this section document the Azure PowerShell cmdlets for Azure Reservations in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c1c79-104">이 cmdlet은 Microsoft Azure. 명령인 네임 스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-104">The cmdlets exist in the Microsoft.Azure.Commands.Reservations namespace.</span></span>

## <span data-ttu-id="c1c79-105">AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1c79-105">AzureRM.Reservations Cmdlets</span></span>
### [<span data-ttu-id="c1c79-106">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c1c79-106">Get-AzureRmReservation</span></span>](Get-AzureRmReservation.md)
<span data-ttu-id="c1c79-107">`Reservation`지정 된 예약 순서로 s 가져오기</span><span class="sxs-lookup"><span data-stu-id="c1c79-107">Get `Reservation`s in a given reservation Order</span></span>

### [<span data-ttu-id="c1c79-108">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="c1c79-108">Get-AzureRmReservationCatalog</span></span>](Get-AzureRmReservationCatalog.md)
<span data-ttu-id="c1c79-109">사용할 수 있는 예약 카탈로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-109">Get the catalog of available reservation.</span></span>

### [<span data-ttu-id="c1c79-110">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="c1c79-110">Get-AzureRmReservationHistory</span></span>](Get-AzureRmReservationHistory.md)
<span data-ttu-id="c1c79-111">의 수정 기록을 가져옵니다 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c1c79-111">Get the revision history of a `Reservation`.</span></span>

### [<span data-ttu-id="c1c79-112">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c1c79-112">Get-AzureRmReservationOrder</span></span>](Get-AzureRmReservationOrder.md)
<span data-ttu-id="c1c79-113">`ReservationOrder`현재 테 넌 트 아래에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-113">Get `ReservationOrder` under current tenant.</span></span> <span data-ttu-id="c1c79-114">주문 id를 제공 하는 경우에는 특정 주문이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-114">If order id is provided, specific order is retrieved.</span></span>

### [<span data-ttu-id="c1c79-115">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c1c79-115">Get-AzureRmReservationOrderId</span></span>](Get-AzureRmReservationOrderId.md)
<span data-ttu-id="c1c79-116">`ReservationOrder`지정 된 구독에서 해당 id의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-116">Get list of applicable `ReservationOrder` Ids under given subscription.</span></span>

### [<span data-ttu-id="c1c79-117">병합-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c1c79-117">Merge-AzureRmReservation</span></span>](Merge-AzureRmReservation.md)
<span data-ttu-id="c1c79-118">두 `Reservation` s를 하나로 병합 합니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c1c79-118">Merges two `Reservation`s into one `Reservation`</span></span>

### [<span data-ttu-id="c1c79-119">분할-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c1c79-119">Split-AzureRmReservation</span></span>](Split-AzureRmReservation.md)
<span data-ttu-id="c1c79-120">A `Reservation` 2 s로 `Reservation` 분할</span><span class="sxs-lookup"><span data-stu-id="c1c79-120">Split a `Reservation` into two `Reservation`s</span></span>

### [<span data-ttu-id="c1c79-121">업데이트-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c1c79-121">Update-AzureRmReservation</span></span>](Update-AzureRmReservation.md)
<span data-ttu-id="c1c79-122">의 적용 된 범위를 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c79-122">Update the applied scope of a `Reservation`.</span></span>

