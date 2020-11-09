---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307982"
---
# <span data-ttu-id="3f97c-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3f97c-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="3f97c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f97c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f97c-103">해당 id의 목록을 가져옵니다 `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="3f97c-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="3f97c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f97c-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f97c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f97c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f97c-106">`ReservationOrder`이 구독에 적용할 수 있는 해당 s의 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f97c-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="3f97c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f97c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f97c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f97c-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="3f97c-109">`ReservationOrder`기본 구독에 적용</span><span class="sxs-lookup"><span data-stu-id="3f97c-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="3f97c-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="3f97c-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="3f97c-111">`ReservationOrder`지정 된 구독에 대해 적용 됨</span><span class="sxs-lookup"><span data-stu-id="3f97c-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="3f97c-112">변수</span><span class="sxs-lookup"><span data-stu-id="3f97c-112">PARAMETERS</span></span>

### <span data-ttu-id="3f97c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f97c-113">-DefaultProfile</span></span>
<span data-ttu-id="3f97c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f97c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f97c-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f97c-115">-SubscriptionId</span></span>
<span data-ttu-id="3f97c-116">적용 된 s를 가져오는 구독 Id `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3f97c-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="3f97c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f97c-117">CommonParameters</span></span>
<span data-ttu-id="3f97c-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f97c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f97c-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f97c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f97c-120">입력</span><span class="sxs-lookup"><span data-stu-id="3f97c-120">INPUTS</span></span>

### <span data-ttu-id="3f97c-121">않아야</span><span class="sxs-lookup"><span data-stu-id="3f97c-121">None</span></span>

## <span data-ttu-id="3f97c-122">출력</span><span class="sxs-lookup"><span data-stu-id="3f97c-122">OUTPUTS</span></span>

### <span data-ttu-id="3f97c-123">AppliedReservations를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f97c-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="3f97c-124">상속자</span><span class="sxs-lookup"><span data-stu-id="3f97c-124">NOTES</span></span>

## <span data-ttu-id="3f97c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f97c-125">RELATED LINKS</span></span>
