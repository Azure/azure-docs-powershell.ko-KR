---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000315"
---
# <span data-ttu-id="516b3-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="516b3-101">Get-AzReservation</span></span>

## <span data-ttu-id="516b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="516b3-102">SYNOPSIS</span></span>
<span data-ttu-id="516b3-103">주어진 `Reservation` 예약 주문에서 s를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="516b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="516b3-104">SYNTAX</span></span>

### <span data-ttu-id="516b3-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="516b3-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="516b3-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="516b3-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="516b3-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="516b3-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="516b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="516b3-108">DESCRIPTION</span></span>
<span data-ttu-id="516b3-109">단일 `Reservation` 에 s를 `ReservationOrder` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="516b3-110">예제</span><span class="sxs-lookup"><span data-stu-id="516b3-110">EXAMPLES</span></span>

### <span data-ttu-id="516b3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="516b3-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="516b3-112">지정된 `Reservation` 에 s를 `ReservationOrder` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="516b3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="516b3-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="516b3-114">특정 세부 `Reservation` 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="516b3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="516b3-115">PARAMETERS</span></span>

### <span data-ttu-id="516b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516b3-116">-DefaultProfile</span></span>
<span data-ttu-id="516b3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516b3-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="516b3-118">-ReservationId</span></span>
<span data-ttu-id="516b3-119">살펴 `Reservation` 볼 의 ID</span><span class="sxs-lookup"><span data-stu-id="516b3-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="516b3-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="516b3-120">-ReservationOrder</span></span>
<span data-ttu-id="516b3-121">에 대한 파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="516b3-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="516b3-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="516b3-122">-ReservationOrderId</span></span>
<span data-ttu-id="516b3-123">`ReservationOrder`을 포함하는 `Reservation` 의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="516b3-124">필수.</span><span class="sxs-lookup"><span data-stu-id="516b3-124">Required.</span></span>

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

### <span data-ttu-id="516b3-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="516b3-125">-ReservationOrderPage</span></span>
<span data-ttu-id="516b3-126">에 대한 파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="516b3-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="516b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516b3-127">CommonParameters</span></span>
<span data-ttu-id="516b3-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="516b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516b3-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="516b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516b3-130">입력</span><span class="sxs-lookup"><span data-stu-id="516b3-130">INPUTS</span></span>

### <span data-ttu-id="516b3-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="516b3-131">System.Guid</span></span>

### <span data-ttu-id="516b3-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="516b3-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="516b3-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="516b3-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="516b3-134">출력</span><span class="sxs-lookup"><span data-stu-id="516b3-134">OUTPUTS</span></span>

### <span data-ttu-id="516b3-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="516b3-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="516b3-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="516b3-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="516b3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="516b3-137">NOTES</span></span>

## <span data-ttu-id="516b3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="516b3-138">RELATED LINKS</span></span>
