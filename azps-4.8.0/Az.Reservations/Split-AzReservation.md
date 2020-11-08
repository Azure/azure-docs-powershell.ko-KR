---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048064"
---
# <span data-ttu-id="6fb4d-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="6fb4d-101">Split-AzReservation</span></span>

## <span data-ttu-id="6fb4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb4d-103">분할 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6fb4d-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="6fb4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fb4d-104">SYNTAX</span></span>

### <span data-ttu-id="6fb4d-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fb4d-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb4d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6fb4d-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb4d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6fb4d-107">DESCRIPTION</span></span>
<span data-ttu-id="6fb4d-108">지정 된 `Reservation` `Reservation` 수량 분포를 사용 하 여 a를 2 개의 s로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="6fb4d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6fb4d-109">EXAMPLES</span></span>

### <span data-ttu-id="6fb4d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fb4d-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="6fb4d-111">지정 된을 `Reservation` 해당 수량의 2 s로 나눕니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6fb4d-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="6fb4d-112">변수</span><span class="sxs-lookup"><span data-stu-id="6fb4d-112">PARAMETERS</span></span>

### <span data-ttu-id="6fb4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb4d-113">-DefaultProfile</span></span>
<span data-ttu-id="6fb4d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-115">-수량</span><span class="sxs-lookup"><span data-stu-id="6fb4d-115">-Quantity</span></span>
<span data-ttu-id="6fb4d-116">2 s의 수량 필드에 대해 쉼표로 구분 된 정수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6fb4d-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-117">-예약</span><span class="sxs-lookup"><span data-stu-id="6fb4d-117">-Reservation</span></span>
<span data-ttu-id="6fb4d-118">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6fb4d-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6fb4d-119">-ReservationId</span></span>
<span data-ttu-id="6fb4d-120">분할할의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6fb4d-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6fb4d-121">-ReservationOrderId</span></span>
<span data-ttu-id="6fb4d-122">`ReservationOrder` `Reservation` 해당 사용자에 게 나누려는의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6fb4d-123">-Confirm</span></span>
<span data-ttu-id="6fb4d-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb4d-125">-WhatIf</span></span>
<span data-ttu-id="6fb4d-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fb4d-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb4d-128">CommonParameters</span></span>
<span data-ttu-id="6fb4d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb4d-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fb4d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb4d-131">입력</span><span class="sxs-lookup"><span data-stu-id="6fb4d-131">INPUTS</span></span>

### <span data-ttu-id="6fb4d-132">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6fb4d-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6fb4d-133">출력</span><span class="sxs-lookup"><span data-stu-id="6fb4d-133">OUTPUTS</span></span>

### <span data-ttu-id="6fb4d-134">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6fb4d-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6fb4d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6fb4d-135">NOTES</span></span>

## <span data-ttu-id="6fb4d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fb4d-136">RELATED LINKS</span></span>
