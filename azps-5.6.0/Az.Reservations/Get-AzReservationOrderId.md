---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 9783d1ff8d3a42d3ad6627abcaae792f966b7828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000267"
---
# <span data-ttu-id="5d188-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5d188-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="5d188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d188-102">SYNOPSIS</span></span>
<span data-ttu-id="5d188-103">해당 ID 목록을 `ReservationOrder` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d188-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="5d188-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d188-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d188-105">설명</span><span class="sxs-lookup"><span data-stu-id="5d188-105">DESCRIPTION</span></span>
<span data-ttu-id="5d188-106">이 구독에 적용할 수 있는 해당 s의 `ReservationOrder` ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d188-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="5d188-107">예제</span><span class="sxs-lookup"><span data-stu-id="5d188-107">EXAMPLES</span></span>

### <span data-ttu-id="5d188-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d188-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="5d188-109">기본 `ReservationOrder` 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="5d188-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="5d188-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d188-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5d188-111">지정된 `ReservationOrder` 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="5d188-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="5d188-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d188-112">PARAMETERS</span></span>

### <span data-ttu-id="5d188-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d188-113">-DefaultProfile</span></span>
<span data-ttu-id="5d188-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d188-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d188-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d188-115">-SubscriptionId</span></span>
<span data-ttu-id="5d188-116">적용된 s를 얻을 `ReservationOrder` 구독의 ID</span><span class="sxs-lookup"><span data-stu-id="5d188-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="5d188-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d188-117">CommonParameters</span></span>
<span data-ttu-id="5d188-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d188-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d188-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d188-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d188-120">입력</span><span class="sxs-lookup"><span data-stu-id="5d188-120">INPUTS</span></span>

### <span data-ttu-id="5d188-121">없음</span><span class="sxs-lookup"><span data-stu-id="5d188-121">None</span></span>

## <span data-ttu-id="5d188-122">출력</span><span class="sxs-lookup"><span data-stu-id="5d188-122">OUTPUTS</span></span>

### <span data-ttu-id="5d188-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="5d188-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="5d188-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d188-124">NOTES</span></span>

## <span data-ttu-id="5d188-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d188-125">RELATED LINKS</span></span>
