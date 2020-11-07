---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874953"
---
# <span data-ttu-id="bbb2f-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="bbb2f-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="bbb2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb2f-103">구독 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="bbb2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bbb2f-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bbb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb2f-106">구독 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="bbb2f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bbb2f-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb2f-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bbb2f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="bbb2f-109">구독 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-109">Create an subscription plan.</span></span>

## <span data-ttu-id="bbb2f-110">변수</span><span class="sxs-lookup"><span data-stu-id="bbb2f-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb2f-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="bbb2f-111">-AcquisitionId</span></span>
<span data-ttu-id="bbb2f-112">취득 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb2f-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="bbb2f-113">-PlanId</span></span>
<span data-ttu-id="bbb2f-114">테 넌 트 구독 컨텍스트에서 id를 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="bbb2f-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbb2f-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="bbb2f-116">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb2f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="bbb2f-117">-Confirm</span></span>
<span data-ttu-id="bbb2f-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb2f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb2f-119">-WhatIf</span></span>
<span data-ttu-id="bbb2f-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb2f-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb2f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb2f-122">CommonParameters</span></span>
<span data-ttu-id="bbb2f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb2f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb2f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb2f-125">입력</span><span class="sxs-lookup"><span data-stu-id="bbb2f-125">INPUTS</span></span>

## <span data-ttu-id="bbb2f-126">출력</span><span class="sxs-lookup"><span data-stu-id="bbb2f-126">OUTPUTS</span></span>

### <span data-ttu-id="bbb2f-127">Microsoft AzureStack. 경영진. 관리. 모델 취득</span><span class="sxs-lookup"><span data-stu-id="bbb2f-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="bbb2f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bbb2f-128">NOTES</span></span>

## <span data-ttu-id="bbb2f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbb2f-129">RELATED LINKS</span></span>

