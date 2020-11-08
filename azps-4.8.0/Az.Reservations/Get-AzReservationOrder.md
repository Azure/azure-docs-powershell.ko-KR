---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214684"
---
# <span data-ttu-id="8eb83-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8eb83-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="8eb83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eb83-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb83-103">가져오기 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8eb83-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="8eb83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eb83-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eb83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8eb83-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb83-106">`ReservationOrder`사용자가 현재 테 넌 트에서 액세스할 수 있는 모든 s의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb83-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="8eb83-107">ReservationOrderId 매개 변수가 설정 된 경우 특정 ReservationOrder를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eb83-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="8eb83-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8eb83-108">EXAMPLES</span></span>

### <span data-ttu-id="8eb83-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8eb83-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="8eb83-110">사용자가 `ReservationOrder` 현재 테 넌 트에서 액세스할 수 있는 모든 목록</span><span class="sxs-lookup"><span data-stu-id="8eb83-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="8eb83-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="8eb83-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="8eb83-112">`ReservationOrder`지정 된 ReservationOrderId으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="8eb83-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="8eb83-113">변수</span><span class="sxs-lookup"><span data-stu-id="8eb83-113">PARAMETERS</span></span>

### <span data-ttu-id="8eb83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb83-114">-DefaultProfile</span></span>
<span data-ttu-id="8eb83-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb83-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8eb83-116">-ReservationOrderId</span></span>
<span data-ttu-id="8eb83-117">사용자에 게 표시 하려는 특정 ReservationOrder의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb83-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="8eb83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb83-118">CommonParameters</span></span>
<span data-ttu-id="8eb83-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb83-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8eb83-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb83-121">입력</span><span class="sxs-lookup"><span data-stu-id="8eb83-121">INPUTS</span></span>

### <span data-ttu-id="8eb83-122">않아야</span><span class="sxs-lookup"><span data-stu-id="8eb83-122">None</span></span>

## <span data-ttu-id="8eb83-123">출력</span><span class="sxs-lookup"><span data-stu-id="8eb83-123">OUTPUTS</span></span>

### <span data-ttu-id="8eb83-124">PSReservationOrderPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="8eb83-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="8eb83-125">PSReservationOrder에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="8eb83-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="8eb83-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8eb83-126">NOTES</span></span>

## <span data-ttu-id="8eb83-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eb83-127">RELATED LINKS</span></span>
