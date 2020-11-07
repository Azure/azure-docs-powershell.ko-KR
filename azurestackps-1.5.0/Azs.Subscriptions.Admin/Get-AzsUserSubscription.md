---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701797"
---
# <span data-ttu-id="80f3d-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="80f3d-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="80f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="80f3d-103">사용자 구독 목록을 교환원으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="80f3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80f3d-104">SYNTAX</span></span>

### <span data-ttu-id="80f3d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="80f3d-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="80f3d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="80f3d-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="80f3d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="80f3d-107">DESCRIPTION</span></span>
<span data-ttu-id="80f3d-108">사용자 구독 목록을 교환원으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="80f3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="80f3d-109">EXAMPLES</span></span>

### <span data-ttu-id="80f3d-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80f3d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="80f3d-111">사용자 구독 목록을 교환원으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="80f3d-112">변수</span><span class="sxs-lookup"><span data-stu-id="80f3d-112">PARAMETERS</span></span>

### <span data-ttu-id="80f3d-113">-필터</span><span class="sxs-lookup"><span data-stu-id="80f3d-113">-Filter</span></span>
<span data-ttu-id="80f3d-114">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f3d-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80f3d-115">-SubscriptionId</span></span>
<span data-ttu-id="80f3d-116">구독 Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f3d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f3d-117">CommonParameters</span></span>
<span data-ttu-id="80f3d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f3d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f3d-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f3d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f3d-120">입력</span><span class="sxs-lookup"><span data-stu-id="80f3d-120">INPUTS</span></span>

## <span data-ttu-id="80f3d-121">출력</span><span class="sxs-lookup"><span data-stu-id="80f3d-121">OUTPUTS</span></span>

### <span data-ttu-id="80f3d-122">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="80f3d-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="80f3d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="80f3d-123">NOTES</span></span>

## <span data-ttu-id="80f3d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80f3d-124">RELATED LINKS</span></span>

