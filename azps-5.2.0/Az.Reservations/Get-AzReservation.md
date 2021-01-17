---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370168"
---
# <span data-ttu-id="8a2eb-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="8a2eb-101">Get-AzReservation</span></span>

## <span data-ttu-id="8a2eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2eb-103">주어진 `Reservation` 예약 주문에서 s를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="8a2eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a2eb-104">SYNTAX</span></span>

### <span data-ttu-id="8a2eb-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="8a2eb-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2eb-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="8a2eb-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2eb-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="8a2eb-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a2eb-108">설명</span><span class="sxs-lookup"><span data-stu-id="8a2eb-108">DESCRIPTION</span></span>
<span data-ttu-id="8a2eb-109">단일 `Reservation` 내에 s를 나열합니다. `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8a2eb-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="8a2eb-110">예제</span><span class="sxs-lookup"><span data-stu-id="8a2eb-110">EXAMPLES</span></span>

### <span data-ttu-id="8a2eb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a2eb-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="8a2eb-112">지정된 `Reservation` 내 s를 나열합니다. `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8a2eb-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="8a2eb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8a2eb-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="8a2eb-114">특정 세부 `Reservation` 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="8a2eb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a2eb-115">PARAMETERS</span></span>

### <span data-ttu-id="8a2eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2eb-116">-DefaultProfile</span></span>
<span data-ttu-id="8a2eb-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2eb-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8a2eb-118">-ReservationId</span></span>
<span data-ttu-id="8a2eb-119">`Reservation`살펴봐야 할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2eb-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8a2eb-120">-ReservationOrder</span></span>
<span data-ttu-id="8a2eb-121">다음에 대한 파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8a2eb-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2eb-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8a2eb-122">-ReservationOrderId</span></span>
<span data-ttu-id="8a2eb-123">`ReservationOrder`.를 포함하는 `Reservation` ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="8a2eb-124">필수.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2eb-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="8a2eb-125">-ReservationOrderPage</span></span>
<span data-ttu-id="8a2eb-126">다음에 대한 파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8a2eb-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2eb-127">CommonParameters</span></span>
<span data-ttu-id="8a2eb-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2eb-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a2eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2eb-130">입력</span><span class="sxs-lookup"><span data-stu-id="8a2eb-130">INPUTS</span></span>

### <span data-ttu-id="8a2eb-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8a2eb-131">System.Guid</span></span>

### <span data-ttu-id="8a2eb-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8a2eb-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="8a2eb-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="8a2eb-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="8a2eb-134">출력</span><span class="sxs-lookup"><span data-stu-id="8a2eb-134">OUTPUTS</span></span>

### <span data-ttu-id="8a2eb-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="8a2eb-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="8a2eb-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="8a2eb-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8a2eb-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a2eb-137">NOTES</span></span>

## <span data-ttu-id="8a2eb-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a2eb-138">RELATED LINKS</span></span>
