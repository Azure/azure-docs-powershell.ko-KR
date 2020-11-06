---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524964"
---
# <span data-ttu-id="f3741-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="f3741-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="f3741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3741-102">SYNOPSIS</span></span>
<span data-ttu-id="f3741-103">`Reservation`지정 된 예약 순서로 s 가져오기</span><span class="sxs-lookup"><span data-stu-id="f3741-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3741-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3741-104">SYNTAX</span></span>

### <span data-ttu-id="f3741-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3741-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3741-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f3741-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="f3741-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3741-107">DESCRIPTION</span></span>
<span data-ttu-id="f3741-108">`Reservation`단일에서 s를 나열 `ReservationOrder` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3741-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="f3741-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3741-109">EXAMPLES</span></span>

### <span data-ttu-id="f3741-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3741-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="f3741-111">지정 된에서 `Reservation` s를 나열 `ReservationOrder` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3741-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="f3741-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f3741-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="f3741-113">특정 `Reservation` 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3741-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="f3741-114">변수</span><span class="sxs-lookup"><span data-stu-id="f3741-114">PARAMETERS</span></span>

### <span data-ttu-id="f3741-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f3741-115">-ReservationId</span></span>
<span data-ttu-id="f3741-116">보려는의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f3741-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3741-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f3741-117">-ReservationOrder</span></span>
<span data-ttu-id="f3741-118">파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f3741-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3741-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f3741-119">-ReservationOrderId</span></span>
<span data-ttu-id="f3741-120">이 포함 된의 Id입니다 `ReservationOrder` `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f3741-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="f3741-121">필수.</span><span class="sxs-lookup"><span data-stu-id="f3741-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3741-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f3741-122">-ReservationOrderPage</span></span>
<span data-ttu-id="f3741-123">파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f3741-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3741-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3741-124">CommonParameters</span></span>
<span data-ttu-id="f3741-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3741-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3741-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3741-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3741-127">입력</span><span class="sxs-lookup"><span data-stu-id="f3741-127">INPUTS</span></span>

### <span data-ttu-id="f3741-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3741-128">System.String</span></span>
<span data-ttu-id="f3741-129">PSReservationOrder. PSReservationOrderPage에 대 한. a i m. \*.</span><span class="sxs-lookup"><span data-stu-id="f3741-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="f3741-130">출력</span><span class="sxs-lookup"><span data-stu-id="f3741-130">OUTPUTS</span></span>

### <span data-ttu-id="f3741-131">PSReservationPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="f3741-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="f3741-132">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="f3741-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f3741-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f3741-133">NOTES</span></span>

## <span data-ttu-id="f3741-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3741-134">RELATED LINKS</span></span>

