---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869518"
---
# <span data-ttu-id="93d2e-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="93d2e-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="93d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="93d2e-103">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="93d2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93d2e-104">SYNTAX</span></span>

### <span data-ttu-id="93d2e-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="93d2e-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93d2e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="93d2e-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d2e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="93d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="93d2e-108">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="93d2e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="93d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="93d2e-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="93d2e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="93d2e-111">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="93d2e-112">변수</span><span class="sxs-lookup"><span data-stu-id="93d2e-112">PARAMETERS</span></span>

### <span data-ttu-id="93d2e-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="93d2e-113">-AcquisitionId</span></span>
<span data-ttu-id="93d2e-114">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="93d2e-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="93d2e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93d2e-115">-Force</span></span>
<span data-ttu-id="93d2e-116">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="93d2e-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93d2e-117">-ResourceId</span></span>
<span data-ttu-id="93d2e-118">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-118">The resource id.</span></span>

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

### <span data-ttu-id="93d2e-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93d2e-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="93d2e-120">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="93d2e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="93d2e-121">-Confirm</span></span>
<span data-ttu-id="93d2e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d2e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d2e-123">-WhatIf</span></span>
<span data-ttu-id="93d2e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93d2e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d2e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d2e-126">CommonParameters</span></span>
<span data-ttu-id="93d2e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d2e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d2e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d2e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d2e-129">입력</span><span class="sxs-lookup"><span data-stu-id="93d2e-129">INPUTS</span></span>

## <span data-ttu-id="93d2e-130">출력</span><span class="sxs-lookup"><span data-stu-id="93d2e-130">OUTPUTS</span></span>

## <span data-ttu-id="93d2e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="93d2e-131">NOTES</span></span>

## <span data-ttu-id="93d2e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93d2e-132">RELATED LINKS</span></span>

