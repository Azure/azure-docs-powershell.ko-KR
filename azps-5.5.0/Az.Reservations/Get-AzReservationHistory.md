---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183737"
---
# <span data-ttu-id="f1d8a-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="f1d8a-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="f1d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d8a-103">개정 `Reservation` 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d8a-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="f1d8a-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1d8a-104">SYNTAX</span></span>

### <span data-ttu-id="f1d8a-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1d8a-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d8a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f1d8a-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1d8a-107">설명</span><span class="sxs-lookup"><span data-stu-id="f1d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="f1d8a-108">.에 대한 모든 개정 목록 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f1d8a-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="f1d8a-109">예제</span><span class="sxs-lookup"><span data-stu-id="f1d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="f1d8a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1d8a-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f1d8a-111">특정 예약의 개정 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d8a-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="f1d8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1d8a-112">PARAMETERS</span></span>

### <span data-ttu-id="f1d8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d8a-113">-DefaultProfile</span></span>
<span data-ttu-id="f1d8a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d8a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d8a-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="f1d8a-115">-Reservation</span></span>
<span data-ttu-id="f1d8a-116">s에 대한 파이프 `Reservation` 개체 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1d8a-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="f1d8a-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f1d8a-117">-ReservationId</span></span>
<span data-ttu-id="f1d8a-118">기록을 표시하는 ReservationId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f1d8a-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="f1d8a-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f1d8a-119">-ReservationOrderId</span></span>
<span data-ttu-id="f1d8a-120">다음을 포함하는 ReservationOrderId `ReservationOrder``Reservation`</span><span class="sxs-lookup"><span data-stu-id="f1d8a-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="f1d8a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d8a-121">CommonParameters</span></span>
<span data-ttu-id="f1d8a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d8a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d8a-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1d8a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d8a-124">입력</span><span class="sxs-lookup"><span data-stu-id="f1d8a-124">INPUTS</span></span>

### <span data-ttu-id="f1d8a-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f1d8a-125">System.Guid</span></span>

### <span data-ttu-id="f1d8a-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="f1d8a-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f1d8a-127">출력</span><span class="sxs-lookup"><span data-stu-id="f1d8a-127">OUTPUTS</span></span>

### <span data-ttu-id="f1d8a-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="f1d8a-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="f1d8a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1d8a-129">NOTES</span></span>

## <span data-ttu-id="f1d8a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d8a-130">RELATED LINKS</span></span>
