---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874607"
---
# <span data-ttu-id="31816-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="31816-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="31816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31816-102">SYNOPSIS</span></span>
<span data-ttu-id="31816-103">지정 된 사용자 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="31816-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="31816-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31816-104">SYNTAX</span></span>

### <span data-ttu-id="31816-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="31816-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31816-106">리소스</span><span class="sxs-lookup"><span data-stu-id="31816-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31816-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="31816-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31816-108">설명은</span><span class="sxs-lookup"><span data-stu-id="31816-108">DESCRIPTION</span></span>
<span data-ttu-id="31816-109">지정 된 사용자 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="31816-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="31816-110">예제의</span><span class="sxs-lookup"><span data-stu-id="31816-110">EXAMPLES</span></span>

### <span data-ttu-id="31816-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="31816-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="31816-112">구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="31816-112">Updates a subscription</span></span>

## <span data-ttu-id="31816-113">변수</span><span class="sxs-lookup"><span data-stu-id="31816-113">PARAMETERS</span></span>

### <span data-ttu-id="31816-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31816-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="31816-115">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="31816-116">-DisplayName</span></span>
<span data-ttu-id="31816-117">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="31816-118">-ExternalReferenceId</span></span>
<span data-ttu-id="31816-119">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31816-120">-InputObject</span></span>
<span data-ttu-id="31816-121">. 관리자. i a m. i a..</span><span class="sxs-lookup"><span data-stu-id="31816-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31816-122">-위치</span><span class="sxs-lookup"><span data-stu-id="31816-122">-Location</span></span>
<span data-ttu-id="31816-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="31816-124">-OfferId</span></span>
<span data-ttu-id="31816-125">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-126">-소유자</span><span class="sxs-lookup"><span data-stu-id="31816-126">-Owner</span></span>
<span data-ttu-id="31816-127">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31816-128">-ResourceId</span></span>
<span data-ttu-id="31816-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-129">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31816-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="31816-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="31816-131">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-132">-상태</span><span class="sxs-lookup"><span data-stu-id="31816-132">-State</span></span>
<span data-ttu-id="31816-133">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31816-134">-SubscriptionId</span></span>
<span data-ttu-id="31816-135">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="31816-136">-TenantId</span></span>
<span data-ttu-id="31816-137">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31816-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-138">-확인</span><span class="sxs-lookup"><span data-stu-id="31816-138">-Confirm</span></span>
<span data-ttu-id="31816-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31816-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31816-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31816-140">-WhatIf</span></span>
<span data-ttu-id="31816-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31816-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31816-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31816-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31816-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31816-143">CommonParameters</span></span>
<span data-ttu-id="31816-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31816-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31816-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31816-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31816-146">입력</span><span class="sxs-lookup"><span data-stu-id="31816-146">INPUTS</span></span>

## <span data-ttu-id="31816-147">출력</span><span class="sxs-lookup"><span data-stu-id="31816-147">OUTPUTS</span></span>

### <span data-ttu-id="31816-148">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="31816-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="31816-149">상속자</span><span class="sxs-lookup"><span data-stu-id="31816-149">NOTES</span></span>

## <span data-ttu-id="31816-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31816-150">RELATED LINKS</span></span>

