---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874368"
---
# <span data-ttu-id="1234b-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1234b-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="1234b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1234b-102">SYNOPSIS</span></span>
<span data-ttu-id="1234b-103">제안 위임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="1234b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1234b-104">SYNTAX</span></span>

### <span data-ttu-id="1234b-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1234b-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1234b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1234b-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1234b-107">리소스</span><span class="sxs-lookup"><span data-stu-id="1234b-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1234b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1234b-108">DESCRIPTION</span></span>
<span data-ttu-id="1234b-109">제안 위임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="1234b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1234b-110">EXAMPLES</span></span>

### <span data-ttu-id="1234b-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1234b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="1234b-112">제안 위임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="1234b-113">변수</span><span class="sxs-lookup"><span data-stu-id="1234b-113">PARAMETERS</span></span>

### <span data-ttu-id="1234b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1234b-114">-InputObject</span></span>
<span data-ttu-id="1234b-115">OfferDelegation에 대 한 입력 개체 (.. 관리자.</span><span class="sxs-lookup"><span data-stu-id="1234b-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1234b-116">-위치</span><span class="sxs-lookup"><span data-stu-id="1234b-116">-Location</span></span>
<span data-ttu-id="1234b-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1234b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="1234b-118">-Name</span></span>
<span data-ttu-id="1234b-119">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="1234b-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="1234b-120">-OfferName</span></span>
<span data-ttu-id="1234b-121">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-121">Name of an offer.</span></span>

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

### <span data-ttu-id="1234b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1234b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1234b-123">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1234b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1234b-124">-ResourceId</span></span>
<span data-ttu-id="1234b-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-125">The resource id.</span></span>

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

### <span data-ttu-id="1234b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1234b-126">-SubscriptionId</span></span>
<span data-ttu-id="1234b-127">위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1234b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1234b-128">-Confirm</span></span>
<span data-ttu-id="1234b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1234b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1234b-130">-WhatIf</span></span>
<span data-ttu-id="1234b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1234b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1234b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1234b-133">CommonParameters</span></span>
<span data-ttu-id="1234b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1234b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1234b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1234b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1234b-136">입력</span><span class="sxs-lookup"><span data-stu-id="1234b-136">INPUTS</span></span>

## <span data-ttu-id="1234b-137">출력</span><span class="sxs-lookup"><span data-stu-id="1234b-137">OUTPUTS</span></span>

### <span data-ttu-id="1234b-138">OfferDelegation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="1234b-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="1234b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1234b-139">NOTES</span></span>

## <span data-ttu-id="1234b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1234b-140">RELATED LINKS</span></span>

