---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874912"
---
# <span data-ttu-id="c26c6-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="c26c6-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="c26c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c26c6-103">플랜을 제안에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="c26c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c26c6-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c26c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c26c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c26c6-106">플랜을 제안에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="c26c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c26c6-107">EXAMPLES</span></span>

### <span data-ttu-id="c26c6-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c26c6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="c26c6-109">변수</span><span class="sxs-lookup"><span data-stu-id="c26c6-109">PARAMETERS</span></span>

### <span data-ttu-id="c26c6-110">-Force</span><span class="sxs-lookup"><span data-stu-id="c26c6-110">-Force</span></span>
<span data-ttu-id="c26c6-111">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="c26c6-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="c26c6-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="c26c6-113">구독자 별 최대 획득 수</span><span class="sxs-lookup"><span data-stu-id="c26c6-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26c6-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c26c6-114">-OfferName</span></span>
<span data-ttu-id="c26c6-115">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-115">Name of an offer.</span></span>

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

### <span data-ttu-id="c26c6-116">-계획 Linktype</span><span class="sxs-lookup"><span data-stu-id="c26c6-116">-PlanLinkType</span></span>
<span data-ttu-id="c26c6-117">계획 링크의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="c26c6-118">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="c26c6-118">-PlanName</span></span>
<span data-ttu-id="c26c6-119">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-119">Name of the plan.</span></span>

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

### <span data-ttu-id="c26c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="c26c6-121">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c26c6-122">-확인</span><span class="sxs-lookup"><span data-stu-id="c26c6-122">-Confirm</span></span>
<span data-ttu-id="c26c6-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26c6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26c6-124">-WhatIf</span></span>
<span data-ttu-id="c26c6-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26c6-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26c6-127">CommonParameters</span></span>
<span data-ttu-id="c26c6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26c6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26c6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26c6-130">입력</span><span class="sxs-lookup"><span data-stu-id="c26c6-130">INPUTS</span></span>

## <span data-ttu-id="c26c6-131">출력</span><span class="sxs-lookup"><span data-stu-id="c26c6-131">OUTPUTS</span></span>

## <span data-ttu-id="c26c6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c26c6-132">NOTES</span></span>

## <span data-ttu-id="c26c6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c26c6-133">RELATED LINKS</span></span>

