---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325821"
---
# <span data-ttu-id="faca2-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="faca2-101">Split-AzReservation</span></span>

## <span data-ttu-id="faca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faca2-102">SYNOPSIS</span></span>
<span data-ttu-id="faca2-103">`Reservation`.를 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="faca2-104">구문</span><span class="sxs-lookup"><span data-stu-id="faca2-104">SYNTAX</span></span>

### <span data-ttu-id="faca2-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="faca2-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faca2-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="faca2-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faca2-107">설명</span><span class="sxs-lookup"><span data-stu-id="faca2-107">DESCRIPTION</span></span>
<span data-ttu-id="faca2-108">지정된 수량 분포를 통해 a를 `Reservation` `Reservation` 2 s로 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="faca2-109">예제</span><span class="sxs-lookup"><span data-stu-id="faca2-109">EXAMPLES</span></span>

### <span data-ttu-id="faca2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="faca2-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="faca2-111">지정된 수량을 `Reservation` 2 `Reservation` s로 분할</span><span class="sxs-lookup"><span data-stu-id="faca2-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="faca2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faca2-112">PARAMETERS</span></span>

### <span data-ttu-id="faca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faca2-113">-DefaultProfile</span></span>
<span data-ttu-id="faca2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faca2-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="faca2-115">-Quantity</span></span>
<span data-ttu-id="faca2-116">두 개의 수량 필드에 대한 콤마로 구분된 `Reservation` 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="faca2-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="faca2-117">-Reservation</span></span>
<span data-ttu-id="faca2-118">다음에 대한 파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="faca2-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="faca2-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="faca2-119">-ReservationId</span></span>
<span data-ttu-id="faca2-120">분할할 `Reservation` ID</span><span class="sxs-lookup"><span data-stu-id="faca2-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="faca2-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="faca2-121">-ReservationOrderId</span></span>
<span data-ttu-id="faca2-122">분할하려는 사용자가 포함된 `ReservationOrder` `Reservation` ID입니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="faca2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faca2-123">-Confirm</span></span>
<span data-ttu-id="faca2-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faca2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faca2-125">-WhatIf</span></span>
<span data-ttu-id="faca2-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="faca2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faca2-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faca2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faca2-128">CommonParameters</span></span>
<span data-ttu-id="faca2-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="faca2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faca2-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="faca2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faca2-131">입력</span><span class="sxs-lookup"><span data-stu-id="faca2-131">INPUTS</span></span>

### <span data-ttu-id="faca2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="faca2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="faca2-133">출력</span><span class="sxs-lookup"><span data-stu-id="faca2-133">OUTPUTS</span></span>

### <span data-ttu-id="faca2-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="faca2-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="faca2-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="faca2-135">NOTES</span></span>

## <span data-ttu-id="faca2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faca2-136">RELATED LINKS</span></span>