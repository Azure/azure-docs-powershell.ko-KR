---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529740"
---
# <span data-ttu-id="7b0e0-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7b0e0-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="7b0e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0e0-103">가져오기 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7b0e0-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b0e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b0e0-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b0e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b0e0-105">DESCRIPTION</span></span>
<span data-ttu-id="7b0e0-106">`ReservationOrder`사용자가 현재 테 넌 트에서 액세스할 수 있는 모든 s의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0e0-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="7b0e0-107">ReservationOrderId 매개 변수가 설정 된 경우 특정 ReservationOrder를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b0e0-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="7b0e0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7b0e0-108">EXAMPLES</span></span>

### <span data-ttu-id="7b0e0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b0e0-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="7b0e0-110">사용자가 `ReservationOrder` 현재 테 넌 트에서 액세스할 수 있는 모든 목록</span><span class="sxs-lookup"><span data-stu-id="7b0e0-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="7b0e0-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="7b0e0-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="7b0e0-112">`ReservationOrder`지정 된 ReservationOrderId으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="7b0e0-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="7b0e0-113">변수</span><span class="sxs-lookup"><span data-stu-id="7b0e0-113">PARAMETERS</span></span>

### <span data-ttu-id="7b0e0-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7b0e0-114">-ReservationOrderId</span></span>
<span data-ttu-id="7b0e0-115">사용자에 게 표시 하려는 특정 ReservationOrder의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0e0-115">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0e0-116">CommonParameters</span></span>
<span data-ttu-id="7b0e0-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b0e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0e0-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0e0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0e0-119">입력</span><span class="sxs-lookup"><span data-stu-id="7b0e0-119">INPUTS</span></span>

### <span data-ttu-id="7b0e0-120">않아야</span><span class="sxs-lookup"><span data-stu-id="7b0e0-120">None</span></span>

## <span data-ttu-id="7b0e0-121">출력</span><span class="sxs-lookup"><span data-stu-id="7b0e0-121">OUTPUTS</span></span>

### <span data-ttu-id="7b0e0-122">PSReservationOrderPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="7b0e0-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="7b0e0-123">PSReservationOrder에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="7b0e0-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="7b0e0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7b0e0-124">NOTES</span></span>

## <span data-ttu-id="7b0e0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b0e0-125">RELATED LINKS</span></span>

