---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874917"
---
# <span data-ttu-id="036a1-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="036a1-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="036a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="036a1-102">SYNOPSIS</span></span>
<span data-ttu-id="036a1-103">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="036a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="036a1-104">SYNTAX</span></span>

### <span data-ttu-id="036a1-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="036a1-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="036a1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="036a1-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036a1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="036a1-107">DESCRIPTION</span></span>
<span data-ttu-id="036a1-108">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="036a1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="036a1-109">EXAMPLES</span></span>

### <span data-ttu-id="036a1-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="036a1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="036a1-111">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="036a1-112">변수</span><span class="sxs-lookup"><span data-stu-id="036a1-112">PARAMETERS</span></span>

### <span data-ttu-id="036a1-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="036a1-113">-AcquisitionId</span></span>
<span data-ttu-id="036a1-114">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="036a1-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036a1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="036a1-115">-Force</span></span>
<span data-ttu-id="036a1-116">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-116">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036a1-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="036a1-117">-ResourceId</span></span>
<span data-ttu-id="036a1-118">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-118">The resource id.</span></span>

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

### <span data-ttu-id="036a1-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="036a1-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="036a1-120">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="036a1-121">-확인</span><span class="sxs-lookup"><span data-stu-id="036a1-121">-Confirm</span></span>
<span data-ttu-id="036a1-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036a1-123">-WhatIf</span></span>
<span data-ttu-id="036a1-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036a1-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036a1-126">CommonParameters</span></span>
<span data-ttu-id="036a1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="036a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036a1-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036a1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036a1-129">입력</span><span class="sxs-lookup"><span data-stu-id="036a1-129">INPUTS</span></span>

## <span data-ttu-id="036a1-130">출력</span><span class="sxs-lookup"><span data-stu-id="036a1-130">OUTPUTS</span></span>

## <span data-ttu-id="036a1-131">상속자</span><span class="sxs-lookup"><span data-stu-id="036a1-131">NOTES</span></span>

## <span data-ttu-id="036a1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="036a1-132">RELATED LINKS</span></span>

