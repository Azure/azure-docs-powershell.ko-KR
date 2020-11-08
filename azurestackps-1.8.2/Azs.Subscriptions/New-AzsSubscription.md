---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046947"
---
# <span data-ttu-id="9e665-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9e665-101">New-AzsSubscription</span></span>

## <span data-ttu-id="9e665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e665-102">SYNOPSIS</span></span>
<span data-ttu-id="9e665-103">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-103">Create a subscription.</span></span>

## <span data-ttu-id="9e665-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e665-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e665-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e665-105">DESCRIPTION</span></span>
<span data-ttu-id="9e665-106">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-106">Create a subscription.</span></span>

## <span data-ttu-id="9e665-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e665-107">EXAMPLES</span></span>

### <span data-ttu-id="9e665-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e665-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="9e665-109">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-109">Create a subscription.</span></span>

## <span data-ttu-id="9e665-110">변수</span><span class="sxs-lookup"><span data-stu-id="9e665-110">PARAMETERS</span></span>

### <span data-ttu-id="9e665-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9e665-111">-OfferId</span></span>
<span data-ttu-id="9e665-112">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-112">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e665-113">-DisplayName</span></span>
<span data-ttu-id="9e665-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9e665-115">-TenantId</span></span>
<span data-ttu-id="9e665-116">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-116">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e665-117">-SubscriptionId</span></span>
<span data-ttu-id="9e665-118">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-118">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-119">-상태</span><span class="sxs-lookup"><span data-stu-id="9e665-119">-State</span></span>
<span data-ttu-id="9e665-120">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-120">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-121">-위치</span><span class="sxs-lookup"><span data-stu-id="9e665-121">-Location</span></span>
<span data-ttu-id="9e665-122">리소스가 위치 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e665-123">-WhatIf</span></span>
<span data-ttu-id="9e665-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e665-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9e665-126">-Confirm</span></span>
<span data-ttu-id="9e665-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e665-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e665-128">CommonParameters</span></span>
<span data-ttu-id="9e665-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e665-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e665-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e665-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e665-131">입력</span><span class="sxs-lookup"><span data-stu-id="9e665-131">INPUTS</span></span>

## <span data-ttu-id="9e665-132">출력</span><span class="sxs-lookup"><span data-stu-id="9e665-132">OUTPUTS</span></span>

### <span data-ttu-id="9e665-133">Microsoft AzureStack. 관리. 구독 모델</span><span class="sxs-lookup"><span data-stu-id="9e665-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="9e665-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9e665-134">NOTES</span></span>

## <span data-ttu-id="9e665-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e665-135">RELATED LINKS</span></span>
