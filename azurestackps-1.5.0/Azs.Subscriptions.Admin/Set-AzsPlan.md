---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523584"
---
# <span data-ttu-id="ca8a2-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="ca8a2-101">Set-AzsPlan</span></span>

## <span data-ttu-id="ca8a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8a2-103">지정 된 요금제 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca8a2-103">Updates the specified plan</span></span>

## <span data-ttu-id="ca8a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca8a2-104">SYNTAX</span></span>

### <span data-ttu-id="ca8a2-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ca8a2-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8a2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ca8a2-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8a2-107">리소스</span><span class="sxs-lookup"><span data-stu-id="ca8a2-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ca8a2-108">DESCRIPTION</span></span>
<span data-ttu-id="ca8a2-109">지정 된 요금제 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca8a2-109">Updates the specified plan</span></span>

## <span data-ttu-id="ca8a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ca8a2-110">EXAMPLES</span></span>

### <span data-ttu-id="ca8a2-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ca8a2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="ca8a2-112">지정 된 요금제 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca8a2-112">Updates the specified plan</span></span>

## <span data-ttu-id="ca8a2-113">변수</span><span class="sxs-lookup"><span data-stu-id="ca8a2-113">PARAMETERS</span></span>

### <span data-ttu-id="ca8a2-114">-설명</span><span class="sxs-lookup"><span data-stu-id="ca8a2-114">-Description</span></span>
<span data-ttu-id="ca8a2-115">계획에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca8a2-116">-DisplayName</span></span>
<span data-ttu-id="ca8a2-117">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="ca8a2-118">-ExternalReferenceId</span></span>
<span data-ttu-id="ca8a2-119">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca8a2-120">-InputObject</span></span>
<span data-ttu-id="ca8a2-121">' AzureStack. 관리. 플랜. ' 관리자의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-122">-위치</span><span class="sxs-lookup"><span data-stu-id="ca8a2-122">-Location</span></span>
<span data-ttu-id="ca8a2-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="ca8a2-124">-Name</span></span>
<span data-ttu-id="ca8a2-125">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="ca8a2-126">-QuotaIds</span></span>
<span data-ttu-id="ca8a2-127">계획 아래에 할당량 식별자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8a2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ca8a2-129">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8a2-130">-ResourceId</span></span>
<span data-ttu-id="ca8a2-131">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-132">-(\) Uid</span><span class="sxs-lookup"><span data-stu-id="ca8a2-132">-SkuIds</span></span>
<span data-ttu-id="ca8a2-133">SKU 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-134">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="ca8a2-134">-SubscriptionCount</span></span>
<span data-ttu-id="ca8a2-135">구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8a2-136">-확인</span><span class="sxs-lookup"><span data-stu-id="ca8a2-136">-Confirm</span></span>
<span data-ttu-id="ca8a2-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8a2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8a2-138">-WhatIf</span></span>
<span data-ttu-id="ca8a2-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8a2-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8a2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8a2-141">CommonParameters</span></span>
<span data-ttu-id="ca8a2-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8a2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8a2-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8a2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8a2-144">입력</span><span class="sxs-lookup"><span data-stu-id="ca8a2-144">INPUTS</span></span>

## <span data-ttu-id="ca8a2-145">출력</span><span class="sxs-lookup"><span data-stu-id="ca8a2-145">OUTPUTS</span></span>

### <span data-ttu-id="ca8a2-146">Microsoft AzureStack. 관리자. 관리. 계획</span><span class="sxs-lookup"><span data-stu-id="ca8a2-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="ca8a2-147">상속자</span><span class="sxs-lookup"><span data-stu-id="ca8a2-147">NOTES</span></span>

## <span data-ttu-id="ca8a2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca8a2-148">RELATED LINKS</span></span>

