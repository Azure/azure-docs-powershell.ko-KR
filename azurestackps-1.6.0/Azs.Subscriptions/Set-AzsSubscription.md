---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523867"
---
# <span data-ttu-id="2a3eb-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="2a3eb-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="2a3eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3eb-103">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="2a3eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a3eb-104">SYNTAX</span></span>

### <span data-ttu-id="2a3eb-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a3eb-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a3eb-106">리소스</span><span class="sxs-lookup"><span data-stu-id="2a3eb-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a3eb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a3eb-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a3eb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2a3eb-108">DESCRIPTION</span></span>
<span data-ttu-id="2a3eb-109">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="2a3eb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a3eb-110">EXAMPLES</span></span>

### <span data-ttu-id="2a3eb-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2a3eb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="2a3eb-112">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="2a3eb-113">변수</span><span class="sxs-lookup"><span data-stu-id="2a3eb-113">PARAMETERS</span></span>

### <span data-ttu-id="2a3eb-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a3eb-114">-DisplayName</span></span>
<span data-ttu-id="2a3eb-115">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-115">Subscription name.</span></span>

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

### <span data-ttu-id="2a3eb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a3eb-116">-InputObject</span></span>
<span data-ttu-id="2a3eb-117">Posbbily가 AzsNetworkQuota에서 반환 된 네트워크 할당량을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="2a3eb-118">-위치</span><span class="sxs-lookup"><span data-stu-id="2a3eb-118">-Location</span></span>
<span data-ttu-id="2a3eb-119">리소스가 위치 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="2a3eb-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="2a3eb-120">-OfferId</span></span>
<span data-ttu-id="2a3eb-121">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="2a3eb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a3eb-122">-ResourceId</span></span>
<span data-ttu-id="2a3eb-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-123">The resource ID.</span></span>

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

### <span data-ttu-id="2a3eb-124">-상태</span><span class="sxs-lookup"><span data-stu-id="2a3eb-124">-State</span></span>
<span data-ttu-id="2a3eb-125">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-125">Subscription state.</span></span>

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

### <span data-ttu-id="2a3eb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a3eb-126">-SubscriptionId</span></span>
<span data-ttu-id="2a3eb-127">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="2a3eb-128">태그</span><span class="sxs-lookup"><span data-stu-id="2a3eb-128">-Tags</span></span>
<span data-ttu-id="2a3eb-129">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="2a3eb-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="2a3eb-130">-TenantId</span></span>
<span data-ttu-id="2a3eb-131">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="2a3eb-132">-Type</span><span class="sxs-lookup"><span data-stu-id="2a3eb-132">-Type</span></span>
<span data-ttu-id="2a3eb-133">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-133">Type of resource.</span></span>

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

### <span data-ttu-id="2a3eb-134">-확인</span><span class="sxs-lookup"><span data-stu-id="2a3eb-134">-Confirm</span></span>
<span data-ttu-id="2a3eb-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a3eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a3eb-136">-WhatIf</span></span>
<span data-ttu-id="2a3eb-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a3eb-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a3eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3eb-139">CommonParameters</span></span>
<span data-ttu-id="2a3eb-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a3eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3eb-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a3eb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3eb-142">입력</span><span class="sxs-lookup"><span data-stu-id="2a3eb-142">INPUTS</span></span>

## <span data-ttu-id="2a3eb-143">출력</span><span class="sxs-lookup"><span data-stu-id="2a3eb-143">OUTPUTS</span></span>

### <span data-ttu-id="2a3eb-144">Microsoft AzureStack. 관리. 구독 모델</span><span class="sxs-lookup"><span data-stu-id="2a3eb-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="2a3eb-145">상속자</span><span class="sxs-lookup"><span data-stu-id="2a3eb-145">NOTES</span></span>

## <span data-ttu-id="2a3eb-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a3eb-146">RELATED LINKS</span></span>

