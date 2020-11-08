---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047079"
---
# <span data-ttu-id="c2524-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c2524-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="c2524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2524-102">SYNOPSIS</span></span>
<span data-ttu-id="c2524-103">새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-103">Create a new subscription.</span></span>

## <span data-ttu-id="c2524-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2524-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2524-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2524-105">DESCRIPTION</span></span>
<span data-ttu-id="c2524-106">새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-106">Create a new subscription.</span></span>

## <span data-ttu-id="c2524-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c2524-107">EXAMPLES</span></span>

### <span data-ttu-id="c2524-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2524-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="c2524-109">새 사용자 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="c2524-109">Creates a new user subscription</span></span>

## <span data-ttu-id="c2524-110">변수</span><span class="sxs-lookup"><span data-stu-id="c2524-110">PARAMETERS</span></span>

### <span data-ttu-id="c2524-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2524-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="c2524-112">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2524-113">-DisplayName</span></span>
<span data-ttu-id="c2524-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c2524-115">-ExternalReferenceId</span></span>
<span data-ttu-id="c2524-116">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="c2524-117">-OfferId</span></span>
<span data-ttu-id="c2524-118">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-119">-소유자</span><span class="sxs-lookup"><span data-stu-id="c2524-119">-Owner</span></span>
<span data-ttu-id="c2524-120">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-120">Subscription owner.</span></span>

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

### <span data-ttu-id="c2524-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="c2524-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="c2524-122">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-123">-상태</span><span class="sxs-lookup"><span data-stu-id="c2524-123">-State</span></span>
<span data-ttu-id="c2524-124">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2524-125">-SubscriptionId</span></span>
<span data-ttu-id="c2524-126">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2524-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c2524-127">-TenantId</span></span>
<span data-ttu-id="c2524-128">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c2524-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c2524-129">-Confirm</span></span>
<span data-ttu-id="c2524-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2524-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2524-131">-WhatIf</span></span>
<span data-ttu-id="c2524-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2524-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2524-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2524-134">CommonParameters</span></span>
<span data-ttu-id="c2524-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2524-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2524-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2524-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2524-137">입력</span><span class="sxs-lookup"><span data-stu-id="c2524-137">INPUTS</span></span>

## <span data-ttu-id="c2524-138">출력</span><span class="sxs-lookup"><span data-stu-id="c2524-138">OUTPUTS</span></span>

### <span data-ttu-id="c2524-139">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="c2524-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="c2524-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c2524-140">NOTES</span></span>

## <span data-ttu-id="c2524-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2524-141">RELATED LINKS</span></span>

