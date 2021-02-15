---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176444"
---
# <span data-ttu-id="aeae5-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="aeae5-101">Merge-AzReservation</span></span>

## <span data-ttu-id="aeae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeae5-102">SYNOPSIS</span></span>
<span data-ttu-id="aeae5-103">두 s를 `Reservation` 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="aeae5-104">구문</span><span class="sxs-lookup"><span data-stu-id="aeae5-104">SYNTAX</span></span>

### <span data-ttu-id="aeae5-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="aeae5-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeae5-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="aeae5-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeae5-107">설명</span><span class="sxs-lookup"><span data-stu-id="aeae5-107">DESCRIPTION</span></span>
<span data-ttu-id="aeae5-108">지정된 `Reservation` s를 새 에 `Reservation` 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="aeae5-109">병합되는 `Reservation` 두 개의 속성은 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="aeae5-110">예제</span><span class="sxs-lookup"><span data-stu-id="aeae5-110">EXAMPLES</span></span>

### <span data-ttu-id="aeae5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aeae5-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="aeae5-112">지정된 두 `Reservation` s를 하나에 병합 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="aeae5-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="aeae5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeae5-113">PARAMETERS</span></span>

### <span data-ttu-id="aeae5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeae5-114">-DefaultProfile</span></span>
<span data-ttu-id="aeae5-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeae5-116">-Reservation</span><span class="sxs-lookup"><span data-stu-id="aeae5-116">-Reservation</span></span>
<span data-ttu-id="aeae5-117">병합할 두 ReservationId의 콤마로 구분된 문자열</span><span class="sxs-lookup"><span data-stu-id="aeae5-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeae5-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="aeae5-118">-ReservationId</span></span>
<span data-ttu-id="aeae5-119">두 s를 포함하는 ReservationOrderId `ReservationOrder` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="aeae5-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeae5-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="aeae5-120">-ReservationOrderId</span></span>
<span data-ttu-id="aeae5-121">{{ReservationOrderId 설명 입력}}</span><span class="sxs-lookup"><span data-stu-id="aeae5-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="aeae5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeae5-122">-Confirm</span></span>
<span data-ttu-id="aeae5-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeae5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeae5-124">-WhatIf</span></span>
<span data-ttu-id="aeae5-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aeae5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeae5-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeae5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeae5-127">CommonParameters</span></span>
<span data-ttu-id="aeae5-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aeae5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeae5-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aeae5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeae5-130">입력</span><span class="sxs-lookup"><span data-stu-id="aeae5-130">INPUTS</span></span>

### <span data-ttu-id="aeae5-131">없음</span><span class="sxs-lookup"><span data-stu-id="aeae5-131">None</span></span>

## <span data-ttu-id="aeae5-132">출력</span><span class="sxs-lookup"><span data-stu-id="aeae5-132">OUTPUTS</span></span>

### <span data-ttu-id="aeae5-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="aeae5-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="aeae5-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aeae5-134">NOTES</span></span>

## <span data-ttu-id="aeae5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeae5-135">RELATED LINKS</span></span>
