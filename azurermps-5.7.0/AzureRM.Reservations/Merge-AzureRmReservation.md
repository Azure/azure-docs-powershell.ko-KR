---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529738"
---
# <span data-ttu-id="1e878-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1e878-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="1e878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e878-102">SYNOPSIS</span></span>
<span data-ttu-id="1e878-103">두 개의 `Reservation` s를 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e878-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e878-104">SYNTAX</span></span>

### <span data-ttu-id="1e878-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e878-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e878-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="1e878-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e878-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1e878-107">DESCRIPTION</span></span>
<span data-ttu-id="1e878-108">지정 된 `Reservation` s를 새에 병합 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="1e878-109">`Reservation`병합 되는 두 s의 속성은 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="1e878-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1e878-110">EXAMPLES</span></span>

### <span data-ttu-id="1e878-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e878-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="1e878-112">지정 된 두 s를 하나로 병합 합니다. `Reservation``Reservation`</span><span class="sxs-lookup"><span data-stu-id="1e878-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="1e878-113">변수</span><span class="sxs-lookup"><span data-stu-id="1e878-113">PARAMETERS</span></span>

### <span data-ttu-id="1e878-114">-예약</span><span class="sxs-lookup"><span data-stu-id="1e878-114">-Reservation</span></span>
<span data-ttu-id="1e878-115">결합할 두 ReservationIds의 쉼표로 구분 된 문자열</span><span class="sxs-lookup"><span data-stu-id="1e878-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e878-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="1e878-116">-ReservationId</span></span>
<span data-ttu-id="1e878-117">`ReservationOrder`2 s이 (가) 포함 된에 대 한 ReservationOrderId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="1e878-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e878-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1e878-118">-ReservationOrderId</span></span>
<span data-ttu-id="1e878-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="1e878-119">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="1e878-120">-확인</span><span class="sxs-lookup"><span data-stu-id="1e878-120">-Confirm</span></span>
<span data-ttu-id="1e878-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e878-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e878-122">-WhatIf</span></span>
<span data-ttu-id="1e878-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e878-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e878-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e878-125">CommonParameters</span></span>
<span data-ttu-id="1e878-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e878-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e878-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e878-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e878-128">입력</span><span class="sxs-lookup"><span data-stu-id="1e878-128">INPUTS</span></span>

### <span data-ttu-id="1e878-129">Microsoft. Azure. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="1e878-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="1e878-130">출력</span><span class="sxs-lookup"><span data-stu-id="1e878-130">OUTPUTS</span></span>

### <span data-ttu-id="1e878-131">System.webserver. List ' 1 [[Microsoft Azure.] 예약과 PSReservation, Microsoft Azure. 명령 예약, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1e878-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1e878-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1e878-132">NOTES</span></span>

## <span data-ttu-id="1e878-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e878-133">RELATED LINKS</span></span>

