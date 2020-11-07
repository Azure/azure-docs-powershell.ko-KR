---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875183"
---
# <span data-ttu-id="39e1f-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="39e1f-101">New-AzsPlan</span></span>

## <span data-ttu-id="39e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="39e1f-103">새 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="39e1f-103">Creates a new plan</span></span>

## <span data-ttu-id="39e1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39e1f-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39e1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="39e1f-106">새 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="39e1f-106">Creates a new plan</span></span>

## <span data-ttu-id="39e1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="39e1f-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39e1f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="39e1f-109">새 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="39e1f-109">Creates a new plan</span></span>

## <span data-ttu-id="39e1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="39e1f-110">PARAMETERS</span></span>

### <span data-ttu-id="39e1f-111">-설명</span><span class="sxs-lookup"><span data-stu-id="39e1f-111">-Description</span></span>
<span data-ttu-id="39e1f-112">계획에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-112">Description of the plan.</span></span>

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

### <span data-ttu-id="39e1f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="39e1f-113">-DisplayName</span></span>
<span data-ttu-id="39e1f-114">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-114">Display name.</span></span>

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

### <span data-ttu-id="39e1f-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="39e1f-115">-ExternalReferenceId</span></span>
<span data-ttu-id="39e1f-116">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-116">External reference identifier.</span></span>

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

### <span data-ttu-id="39e1f-117">-위치</span><span class="sxs-lookup"><span data-stu-id="39e1f-117">-Location</span></span>
<span data-ttu-id="39e1f-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="39e1f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="39e1f-119">-Name</span></span>
<span data-ttu-id="39e1f-120">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-120">Name of the plan.</span></span>

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

### <span data-ttu-id="39e1f-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="39e1f-121">-QuotaIds</span></span>
<span data-ttu-id="39e1f-122">계획 아래에 할당량 식별자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e1f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e1f-123">-ResourceGroupName</span></span>
<span data-ttu-id="39e1f-124">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="39e1f-125">-(\) Uid</span><span class="sxs-lookup"><span data-stu-id="39e1f-125">-SkuIds</span></span>
<span data-ttu-id="39e1f-126">SKU 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e1f-127">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="39e1f-127">-SubscriptionCount</span></span>
<span data-ttu-id="39e1f-128">구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-128">Subscription count.</span></span>

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

### <span data-ttu-id="39e1f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="39e1f-129">-Confirm</span></span>
<span data-ttu-id="39e1f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e1f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e1f-131">-WhatIf</span></span>
<span data-ttu-id="39e1f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39e1f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e1f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e1f-134">CommonParameters</span></span>
<span data-ttu-id="39e1f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e1f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e1f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e1f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e1f-137">입력</span><span class="sxs-lookup"><span data-stu-id="39e1f-137">INPUTS</span></span>

## <span data-ttu-id="39e1f-138">출력</span><span class="sxs-lookup"><span data-stu-id="39e1f-138">OUTPUTS</span></span>

### <span data-ttu-id="39e1f-139">Microsoft AzureStack. 관리자. 관리. 계획</span><span class="sxs-lookup"><span data-stu-id="39e1f-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="39e1f-140">상속자</span><span class="sxs-lookup"><span data-stu-id="39e1f-140">NOTES</span></span>

## <span data-ttu-id="39e1f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39e1f-141">RELATED LINKS</span></span>

