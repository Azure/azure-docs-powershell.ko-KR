---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526067"
---
# <span data-ttu-id="a0c56-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="a0c56-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="a0c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c56-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c56-103">분할 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a0c56-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0c56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0c56-104">SYNTAX</span></span>

### <span data-ttu-id="a0c56-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0c56-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0c56-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a0c56-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0c56-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a0c56-107">DESCRIPTION</span></span>
<span data-ttu-id="a0c56-108">지정 된 `Reservation` `Reservation` 수량 분포를 사용 하 여 a를 2 개의 s로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="a0c56-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a0c56-109">EXAMPLES</span></span>

### <span data-ttu-id="a0c56-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0c56-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="a0c56-111">지정 된을 `Reservation` 해당 수량의 2 s로 나눕니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a0c56-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="a0c56-112">변수</span><span class="sxs-lookup"><span data-stu-id="a0c56-112">PARAMETERS</span></span>

### <span data-ttu-id="a0c56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c56-113">-DefaultProfile</span></span>
<span data-ttu-id="a0c56-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c56-115">-수량</span><span class="sxs-lookup"><span data-stu-id="a0c56-115">-Quantity</span></span>
<span data-ttu-id="a0c56-116">2 s의 수량 필드에 대해 쉼표로 구분 된 정수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a0c56-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="a0c56-117">-예약</span><span class="sxs-lookup"><span data-stu-id="a0c56-117">-Reservation</span></span>
<span data-ttu-id="a0c56-118">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a0c56-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="a0c56-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a0c56-119">-ReservationId</span></span>
<span data-ttu-id="a0c56-120">분할할의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a0c56-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="a0c56-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a0c56-121">-ReservationOrderId</span></span>
<span data-ttu-id="a0c56-122">`ReservationOrder` `Reservation` 해당 사용자에 게 나누려는의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="a0c56-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a0c56-123">-Confirm</span></span>
<span data-ttu-id="a0c56-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c56-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c56-125">-WhatIf</span></span>
<span data-ttu-id="a0c56-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0c56-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c56-128">CommonParameters</span></span>
<span data-ttu-id="a0c56-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c56-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c56-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c56-131">입력</span><span class="sxs-lookup"><span data-stu-id="a0c56-131">INPUTS</span></span>

### <span data-ttu-id="a0c56-132">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a0c56-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="a0c56-133">매개 변수: Reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0c56-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="a0c56-134">출력</span><span class="sxs-lookup"><span data-stu-id="a0c56-134">OUTPUTS</span></span>

### <span data-ttu-id="a0c56-135">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a0c56-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a0c56-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a0c56-136">NOTES</span></span>

## <span data-ttu-id="a0c56-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0c56-137">RELATED LINKS</span></span>
