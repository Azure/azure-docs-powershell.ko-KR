---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cf68c40a13247d1101f6d25abac92f01ae1a0053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699481"
---
# <span data-ttu-id="3ff9a-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="3ff9a-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="3ff9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff9a-103">`Reservation`수정 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ff9a-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="3ff9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ff9a-104">SYNTAX</span></span>

### <span data-ttu-id="3ff9a-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ff9a-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff9a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="3ff9a-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ff9a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ff9a-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff9a-108">의 모든 수정 내용 목록 `Reservation` 입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff9a-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="3ff9a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3ff9a-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff9a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ff9a-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="3ff9a-111">특정 예약의 수정 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ff9a-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="3ff9a-112">변수</span><span class="sxs-lookup"><span data-stu-id="3ff9a-112">PARAMETERS</span></span>

### <span data-ttu-id="3ff9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff9a-113">-DefaultProfile</span></span>
<span data-ttu-id="3ff9a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff9a-115">-예약</span><span class="sxs-lookup"><span data-stu-id="3ff9a-115">-Reservation</span></span>
<span data-ttu-id="3ff9a-116">S의 Pipe 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3ff9a-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="3ff9a-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3ff9a-117">-ReservationId</span></span>
<span data-ttu-id="3ff9a-118">`Reservation`기록이 표시 되는 ReservationId</span><span class="sxs-lookup"><span data-stu-id="3ff9a-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="3ff9a-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3ff9a-119">-ReservationOrderId</span></span>
<span data-ttu-id="3ff9a-120">ReservationOrderId에 `ReservationOrder` 포함 된 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3ff9a-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="3ff9a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff9a-121">CommonParameters</span></span>
<span data-ttu-id="3ff9a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff9a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff9a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff9a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff9a-124">입력</span><span class="sxs-lookup"><span data-stu-id="3ff9a-124">INPUTS</span></span>

### <span data-ttu-id="3ff9a-125">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="3ff9a-125">System.Guid</span></span>

### <span data-ttu-id="3ff9a-126">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="3ff9a-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3ff9a-127">출력</span><span class="sxs-lookup"><span data-stu-id="3ff9a-127">OUTPUTS</span></span>

### <span data-ttu-id="3ff9a-128">PSReservationPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="3ff9a-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="3ff9a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3ff9a-129">NOTES</span></span>

## <span data-ttu-id="3ff9a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ff9a-130">RELATED LINKS</span></span>
