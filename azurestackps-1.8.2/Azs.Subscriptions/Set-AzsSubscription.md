---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046946"
---
# <span data-ttu-id="dce8c-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="dce8c-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="dce8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dce8c-103">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="dce8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dce8c-104">SYNTAX</span></span>

### <span data-ttu-id="dce8c-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="dce8c-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dce8c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="dce8c-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce8c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8c-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce8c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dce8c-108">DESCRIPTION</span></span>
<span data-ttu-id="dce8c-109">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="dce8c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dce8c-110">EXAMPLES</span></span>

### <span data-ttu-id="dce8c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dce8c-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="dce8c-112">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="dce8c-113">변수</span><span class="sxs-lookup"><span data-stu-id="dce8c-113">PARAMETERS</span></span>

### <span data-ttu-id="dce8c-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dce8c-114">-OfferId</span></span>
<span data-ttu-id="dce8c-115">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="dce8c-116">-Type</span><span class="sxs-lookup"><span data-stu-id="dce8c-116">-Type</span></span>
<span data-ttu-id="dce8c-117">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-117">Type of resource.</span></span>

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

### <span data-ttu-id="dce8c-118">태그</span><span class="sxs-lookup"><span data-stu-id="dce8c-118">-Tags</span></span>
<span data-ttu-id="dce8c-119">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce8c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dce8c-120">-SubscriptionId</span></span>
<span data-ttu-id="dce8c-121">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce8c-122">-상태</span><span class="sxs-lookup"><span data-stu-id="dce8c-122">-State</span></span>
<span data-ttu-id="dce8c-123">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-123">Subscription state.</span></span>

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

### <span data-ttu-id="dce8c-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="dce8c-124">-TenantId</span></span>
<span data-ttu-id="dce8c-125">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="dce8c-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dce8c-126">-DisplayName</span></span>
<span data-ttu-id="dce8c-127">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-127">Subscription name.</span></span>

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

### <span data-ttu-id="dce8c-128">-위치</span><span class="sxs-lookup"><span data-stu-id="dce8c-128">-Location</span></span>
<span data-ttu-id="dce8c-129">리소스가 위치 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="dce8c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dce8c-130">-ResourceId</span></span>
<span data-ttu-id="dce8c-131">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-131">The resource ID.</span></span>

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

### <span data-ttu-id="dce8c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8c-132">-InputObject</span></span>
<span data-ttu-id="dce8c-133">Posbbily가 AzsNetworkQuota에서 반환 된 네트워크 할당량을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce8c-134">-WhatIf</span></span>
<span data-ttu-id="dce8c-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce8c-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce8c-137">-확인</span><span class="sxs-lookup"><span data-stu-id="dce8c-137">-Confirm</span></span>
<span data-ttu-id="dce8c-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce8c-139">CommonParameters</span></span>
<span data-ttu-id="dce8c-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce8c-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce8c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce8c-142">입력</span><span class="sxs-lookup"><span data-stu-id="dce8c-142">INPUTS</span></span>

## <span data-ttu-id="dce8c-143">출력</span><span class="sxs-lookup"><span data-stu-id="dce8c-143">OUTPUTS</span></span>

### <span data-ttu-id="dce8c-144">Microsoft AzureStack. 관리. 구독 모델</span><span class="sxs-lookup"><span data-stu-id="dce8c-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="dce8c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="dce8c-145">NOTES</span></span>

## <span data-ttu-id="dce8c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dce8c-146">RELATED LINKS</span></span>
