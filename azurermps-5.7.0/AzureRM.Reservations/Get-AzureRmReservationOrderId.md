---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529737"
---
# <span data-ttu-id="f451e-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f451e-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="f451e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f451e-102">SYNOPSIS</span></span>
<span data-ttu-id="f451e-103">해당 id의 목록을 가져옵니다 `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="f451e-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f451e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f451e-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="f451e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f451e-105">DESCRIPTION</span></span>
<span data-ttu-id="f451e-106">`ReservationOrder`이 구독에 적용할 수 있는 해당 s의 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f451e-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="f451e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f451e-107">EXAMPLES</span></span>

### <span data-ttu-id="f451e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f451e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="f451e-109">`ReservationOrder`기본 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="f451e-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="f451e-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="f451e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="f451e-111">`ReservationOrder`지정 된 구독에 대해 적용 됨</span><span class="sxs-lookup"><span data-stu-id="f451e-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="f451e-112">변수</span><span class="sxs-lookup"><span data-stu-id="f451e-112">PARAMETERS</span></span>

### <span data-ttu-id="f451e-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f451e-113">-SubscriptionId</span></span>
<span data-ttu-id="f451e-114">적용 된 s를 가져오는 구독 Id `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f451e-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f451e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f451e-115">CommonParameters</span></span>
<span data-ttu-id="f451e-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f451e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f451e-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f451e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f451e-118">입력</span><span class="sxs-lookup"><span data-stu-id="f451e-118">INPUTS</span></span>

### <span data-ttu-id="f451e-119">않아야</span><span class="sxs-lookup"><span data-stu-id="f451e-119">None</span></span>

## <span data-ttu-id="f451e-120">출력</span><span class="sxs-lookup"><span data-stu-id="f451e-120">OUTPUTS</span></span>

### <span data-ttu-id="f451e-121">PSAppliedReservationOrderId에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="f451e-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="f451e-122">상속자</span><span class="sxs-lookup"><span data-stu-id="f451e-122">NOTES</span></span>

## <span data-ttu-id="f451e-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f451e-123">RELATED LINKS</span></span>

