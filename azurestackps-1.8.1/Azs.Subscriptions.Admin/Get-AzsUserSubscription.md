---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874961"
---
# <span data-ttu-id="a35c8-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="a35c8-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="a35c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a35c8-103">사용자 구독 목록을 관리자로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="a35c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a35c8-104">SYNTAX</span></span>

### <span data-ttu-id="a35c8-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a35c8-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="a35c8-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a35c8-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="a35c8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a35c8-107">DESCRIPTION</span></span>
<span data-ttu-id="a35c8-108">사용자 구독 목록을 관리자로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="a35c8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a35c8-109">EXAMPLES</span></span>

### <span data-ttu-id="a35c8-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a35c8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="a35c8-111">사용자 구독 목록을 관리자로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="a35c8-112">변수</span><span class="sxs-lookup"><span data-stu-id="a35c8-112">PARAMETERS</span></span>

### <span data-ttu-id="a35c8-113">-필터</span><span class="sxs-lookup"><span data-stu-id="a35c8-113">-Filter</span></span>
<span data-ttu-id="a35c8-114">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="a35c8-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a35c8-115">-SubscriptionId</span></span>
<span data-ttu-id="a35c8-116">구독 Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="a35c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35c8-117">CommonParameters</span></span>
<span data-ttu-id="a35c8-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a35c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35c8-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35c8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35c8-120">입력</span><span class="sxs-lookup"><span data-stu-id="a35c8-120">INPUTS</span></span>

## <span data-ttu-id="a35c8-121">출력</span><span class="sxs-lookup"><span data-stu-id="a35c8-121">OUTPUTS</span></span>

### <span data-ttu-id="a35c8-122">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="a35c8-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="a35c8-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a35c8-123">NOTES</span></span>

## <span data-ttu-id="a35c8-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a35c8-124">RELATED LINKS</span></span>

