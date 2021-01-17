---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377987"
---
# <span data-ttu-id="92990-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="92990-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="92990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92990-102">SYNOPSIS</span></span>
<span data-ttu-id="92990-103">적용 가능한 ID 목록을 `ReservationOrder` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92990-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="92990-104">구문</span><span class="sxs-lookup"><span data-stu-id="92990-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92990-105">설명</span><span class="sxs-lookup"><span data-stu-id="92990-105">DESCRIPTION</span></span>
<span data-ttu-id="92990-106">이 구독에 적용할 수 있는 해당 S의 `ReservationOrder` ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92990-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="92990-107">예제</span><span class="sxs-lookup"><span data-stu-id="92990-107">EXAMPLES</span></span>

### <span data-ttu-id="92990-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="92990-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="92990-109">기본 `ReservationOrder` 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="92990-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="92990-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="92990-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="92990-111">지정된 `ReservationOrder` 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="92990-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="92990-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92990-112">PARAMETERS</span></span>

### <span data-ttu-id="92990-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92990-113">-DefaultProfile</span></span>
<span data-ttu-id="92990-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92990-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92990-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92990-115">-SubscriptionId</span></span>
<span data-ttu-id="92990-116">적용된 구독을 받을 `ReservationOrder` 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="92990-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92990-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92990-117">CommonParameters</span></span>
<span data-ttu-id="92990-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92990-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92990-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92990-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92990-120">입력</span><span class="sxs-lookup"><span data-stu-id="92990-120">INPUTS</span></span>

### <span data-ttu-id="92990-121">없음</span><span class="sxs-lookup"><span data-stu-id="92990-121">None</span></span>

## <span data-ttu-id="92990-122">출력</span><span class="sxs-lookup"><span data-stu-id="92990-122">OUTPUTS</span></span>

### <span data-ttu-id="92990-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="92990-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="92990-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92990-124">NOTES</span></span>

## <span data-ttu-id="92990-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92990-125">RELATED LINKS</span></span>
