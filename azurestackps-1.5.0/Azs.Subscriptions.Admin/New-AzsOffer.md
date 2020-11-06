---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523264"
---
# <span data-ttu-id="90272-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="90272-101">New-AzsOffer</span></span>

## <span data-ttu-id="90272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90272-102">SYNOPSIS</span></span>
<span data-ttu-id="90272-103">새 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90272-103">Creates a new offer.</span></span>

## <span data-ttu-id="90272-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90272-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90272-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90272-105">DESCRIPTION</span></span>
<span data-ttu-id="90272-106">제안을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="90272-106">Create or update the offer.</span></span>

## <span data-ttu-id="90272-107">예제의</span><span class="sxs-lookup"><span data-stu-id="90272-107">EXAMPLES</span></span>

### <span data-ttu-id="90272-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90272-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="90272-109">새 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90272-109">Creates a new offer.</span></span>

## <span data-ttu-id="90272-110">변수</span><span class="sxs-lookup"><span data-stu-id="90272-110">PARAMETERS</span></span>

### <span data-ttu-id="90272-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="90272-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="90272-112">테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-113">-Base계획 Id</span><span class="sxs-lookup"><span data-stu-id="90272-113">-BasePlanIds</span></span>
<span data-ttu-id="90272-114">테 넌 트가 제안에 구독 하는 즉시 테 넌 트에 사용할 수 있는 기본 계획의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-115">-설명</span><span class="sxs-lookup"><span data-stu-id="90272-115">-Description</span></span>
<span data-ttu-id="90272-116">제안에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-116">Description of offer.</span></span>

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

### <span data-ttu-id="90272-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="90272-117">-DisplayName</span></span>
<span data-ttu-id="90272-118">제공의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-118">Display name of offer.</span></span>

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

### <span data-ttu-id="90272-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="90272-119">-ExternalReferenceId</span></span>
<span data-ttu-id="90272-120">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-121">-위치</span><span class="sxs-lookup"><span data-stu-id="90272-121">-Location</span></span>
<span data-ttu-id="90272-122">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="90272-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="90272-124">계정 당 최대 구독 수.</span><span class="sxs-lookup"><span data-stu-id="90272-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-125">-이름</span><span class="sxs-lookup"><span data-stu-id="90272-125">-Name</span></span>
<span data-ttu-id="90272-126">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-126">Name of an offer.</span></span>

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

### <span data-ttu-id="90272-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90272-127">-ResourceGroupName</span></span>
<span data-ttu-id="90272-128">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-129">-상태</span><span class="sxs-lookup"><span data-stu-id="90272-129">-State</span></span>
<span data-ttu-id="90272-130">접근성 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90272-130">Offer accessibility state.</span></span>
<span data-ttu-id="90272-131">기본 값은 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-131">Default value is Private.</span></span>
<span data-ttu-id="90272-132">이 매개 변수는 이후 릴리스에서 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90272-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-133">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="90272-133">-SubscriptionCount</span></span>
<span data-ttu-id="90272-134">현재 구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="90272-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90272-135">-확인</span><span class="sxs-lookup"><span data-stu-id="90272-135">-Confirm</span></span>
<span data-ttu-id="90272-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90272-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90272-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90272-137">-WhatIf</span></span>
<span data-ttu-id="90272-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90272-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90272-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90272-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90272-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90272-140">CommonParameters</span></span>
<span data-ttu-id="90272-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90272-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90272-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90272-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90272-143">입력</span><span class="sxs-lookup"><span data-stu-id="90272-143">INPUTS</span></span>

## <span data-ttu-id="90272-144">출력</span><span class="sxs-lookup"><span data-stu-id="90272-144">OUTPUTS</span></span>

### <span data-ttu-id="90272-145">Microsoft AzureStack. 관리. 관리자. 제공</span><span class="sxs-lookup"><span data-stu-id="90272-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="90272-146">상속자</span><span class="sxs-lookup"><span data-stu-id="90272-146">NOTES</span></span>

## <span data-ttu-id="90272-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90272-147">RELATED LINKS</span></span>

