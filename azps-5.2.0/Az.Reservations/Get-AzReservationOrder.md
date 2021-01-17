---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370119"
---
# <span data-ttu-id="f6df9-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f6df9-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="f6df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6df9-102">SYNOPSIS</span></span>
<span data-ttu-id="f6df9-103">가져오기 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f6df9-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="f6df9-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6df9-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6df9-105">설명</span><span class="sxs-lookup"><span data-stu-id="f6df9-105">DESCRIPTION</span></span>
<span data-ttu-id="f6df9-106">사용자가 현재 테넌트에서 액세스할 수 있는 `ReservationOrder` 모든 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f6df9-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="f6df9-107">ReservationOrderId 매개 변수가 설정된 경우 해당 특정 ReservationOrder를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6df9-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="f6df9-108">예제</span><span class="sxs-lookup"><span data-stu-id="f6df9-108">EXAMPLES</span></span>

### <span data-ttu-id="f6df9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6df9-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="f6df9-110">사용자가 현재 테넌트에 액세스할 수 `ReservationOrder` 있는 모든 항목 나열</span><span class="sxs-lookup"><span data-stu-id="f6df9-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="f6df9-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="f6df9-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f6df9-112">지정된 `ReservationOrder` ReservationOrderId를 사용</span><span class="sxs-lookup"><span data-stu-id="f6df9-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="f6df9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6df9-113">PARAMETERS</span></span>

### <span data-ttu-id="f6df9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6df9-114">-DefaultProfile</span></span>
<span data-ttu-id="f6df9-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6df9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6df9-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f6df9-116">-ReservationOrderId</span></span>
<span data-ttu-id="f6df9-117">사용자가 보게 하려는 특정 ReservationOrder의 ID</span><span class="sxs-lookup"><span data-stu-id="f6df9-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="f6df9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6df9-118">CommonParameters</span></span>
<span data-ttu-id="f6df9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6df9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6df9-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6df9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6df9-121">입력</span><span class="sxs-lookup"><span data-stu-id="f6df9-121">INPUTS</span></span>

### <span data-ttu-id="f6df9-122">없음</span><span class="sxs-lookup"><span data-stu-id="f6df9-122">None</span></span>

## <span data-ttu-id="f6df9-123">출력</span><span class="sxs-lookup"><span data-stu-id="f6df9-123">OUTPUTS</span></span>

### <span data-ttu-id="f6df9-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f6df9-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="f6df9-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f6df9-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="f6df9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6df9-126">NOTES</span></span>

## <span data-ttu-id="f6df9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6df9-127">RELATED LINKS</span></span>
