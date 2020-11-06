---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523099"
---
# <span data-ttu-id="f3f37-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="f3f37-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="f3f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f37-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f37-103">새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-103">Create a new subscription.</span></span>

## <span data-ttu-id="f3f37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3f37-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3f37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3f37-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f37-106">새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-106">Create a new subscription.</span></span>

## <span data-ttu-id="f3f37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3f37-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f37-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3f37-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="f3f37-109">새 사용자 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="f3f37-109">Creates a new user subscription</span></span>

## <span data-ttu-id="f3f37-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3f37-110">PARAMETERS</span></span>

### <span data-ttu-id="f3f37-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3f37-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="f3f37-112">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="f3f37-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3f37-113">-DisplayName</span></span>
<span data-ttu-id="f3f37-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-114">Subscription name.</span></span>

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

### <span data-ttu-id="f3f37-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f3f37-115">-ExternalReferenceId</span></span>
<span data-ttu-id="f3f37-116">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-116">External reference identifier.</span></span>

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

### <span data-ttu-id="f3f37-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="f3f37-117">-OfferId</span></span>
<span data-ttu-id="f3f37-118">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="f3f37-119">-소유자</span><span class="sxs-lookup"><span data-stu-id="f3f37-119">-Owner</span></span>
<span data-ttu-id="f3f37-120">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-120">Subscription owner.</span></span>

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

### <span data-ttu-id="f3f37-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="f3f37-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="f3f37-122">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-122">Routing resource manager type.</span></span>

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

### <span data-ttu-id="f3f37-123">-상태</span><span class="sxs-lookup"><span data-stu-id="f3f37-123">-State</span></span>
<span data-ttu-id="f3f37-124">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-124">Subscription state.</span></span>

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

### <span data-ttu-id="f3f37-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3f37-125">-SubscriptionId</span></span>
<span data-ttu-id="f3f37-126">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-126">Subscription identifier.</span></span>

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

### <span data-ttu-id="f3f37-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f3f37-127">-TenantId</span></span>
<span data-ttu-id="f3f37-128">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="f3f37-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f3f37-129">-Confirm</span></span>
<span data-ttu-id="f3f37-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f37-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f37-131">-WhatIf</span></span>
<span data-ttu-id="f3f37-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f37-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f37-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f37-134">CommonParameters</span></span>
<span data-ttu-id="f3f37-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f37-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f37-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f37-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f37-137">입력</span><span class="sxs-lookup"><span data-stu-id="f3f37-137">INPUTS</span></span>

## <span data-ttu-id="f3f37-138">출력</span><span class="sxs-lookup"><span data-stu-id="f3f37-138">OUTPUTS</span></span>

### <span data-ttu-id="f3f37-139">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="f3f37-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="f3f37-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f3f37-140">NOTES</span></span>

## <span data-ttu-id="f3f37-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3f37-141">RELATED LINKS</span></span>

