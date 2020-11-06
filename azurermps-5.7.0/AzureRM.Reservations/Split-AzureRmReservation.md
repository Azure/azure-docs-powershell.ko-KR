---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529739"
---
# <span data-ttu-id="debdd-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="debdd-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="debdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="debdd-102">SYNOPSIS</span></span>
<span data-ttu-id="debdd-103">분할 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="debdd-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="debdd-104">SYNTAX</span></span>

### <span data-ttu-id="debdd-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="debdd-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="debdd-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="debdd-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="debdd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="debdd-107">DESCRIPTION</span></span>
<span data-ttu-id="debdd-108">지정 된 `Reservation` `Reservation` 수량 분포를 사용 하 여 a를 2 개의 s로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="debdd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="debdd-109">EXAMPLES</span></span>

### <span data-ttu-id="debdd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="debdd-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="debdd-111">지정 된을 `Reservation` 해당 수량의 2 s로 나눕니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="debdd-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="debdd-112">변수</span><span class="sxs-lookup"><span data-stu-id="debdd-112">PARAMETERS</span></span>

### <span data-ttu-id="debdd-113">-수량</span><span class="sxs-lookup"><span data-stu-id="debdd-113">-Quantity</span></span>
<span data-ttu-id="debdd-114">2 s의 수량 필드에 대해 쉼표로 구분 된 정수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="debdd-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-115">-예약</span><span class="sxs-lookup"><span data-stu-id="debdd-115">-Reservation</span></span>
<span data-ttu-id="debdd-116">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="debdd-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="debdd-117">-ReservationId</span></span>
<span data-ttu-id="debdd-118">분할할의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="debdd-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="debdd-119">-ReservationOrderId</span></span>
<span data-ttu-id="debdd-120">`ReservationOrder` `Reservation` 해당 사용자에 게 나누려는의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-121">-확인</span><span class="sxs-lookup"><span data-stu-id="debdd-121">-Confirm</span></span>
<span data-ttu-id="debdd-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debdd-123">-WhatIf</span></span>
<span data-ttu-id="debdd-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="debdd-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debdd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debdd-126">CommonParameters</span></span>
<span data-ttu-id="debdd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="debdd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debdd-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debdd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debdd-129">입력</span><span class="sxs-lookup"><span data-stu-id="debdd-129">INPUTS</span></span>

### <span data-ttu-id="debdd-130">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="debdd-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="debdd-131">출력</span><span class="sxs-lookup"><span data-stu-id="debdd-131">OUTPUTS</span></span>

### <span data-ttu-id="debdd-132">System.webserver. List ' 1 [[Microsoft Azure.] 예약과 PSReservation, Microsoft Azure. 명령 예약, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="debdd-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="debdd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="debdd-133">NOTES</span></span>

## <span data-ttu-id="debdd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="debdd-134">RELATED LINKS</span></span>

