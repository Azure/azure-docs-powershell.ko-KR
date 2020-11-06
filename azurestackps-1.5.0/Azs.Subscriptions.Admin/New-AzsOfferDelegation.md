---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523260"
---
# <span data-ttu-id="2d2b6-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="2d2b6-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="2d2b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2b6-103">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="2d2b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d2b6-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d2b6-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2b6-106">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="2d2b6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d2b6-107">EXAMPLES</span></span>

### <span data-ttu-id="2d2b6-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d2b6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="2d2b6-109">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="2d2b6-110">변수</span><span class="sxs-lookup"><span data-stu-id="2d2b6-110">PARAMETERS</span></span>

### <span data-ttu-id="2d2b6-111">-위치</span><span class="sxs-lookup"><span data-stu-id="2d2b6-111">-Location</span></span>
<span data-ttu-id="2d2b6-112">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-112">Location of the resource.</span></span>

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

### <span data-ttu-id="2d2b6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2d2b6-113">-Name</span></span>
<span data-ttu-id="2d2b6-114">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="2d2b6-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="2d2b6-115">-OfferName</span></span>
<span data-ttu-id="2d2b6-116">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-116">Name of an offer.</span></span>

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

### <span data-ttu-id="2d2b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d2b6-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2b6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d2b6-119">-SubscriptionId</span></span>
<span data-ttu-id="2d2b6-120">위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="2d2b6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="2d2b6-121">-Confirm</span></span>
<span data-ttu-id="2d2b6-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2b6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2b6-123">-WhatIf</span></span>
<span data-ttu-id="2d2b6-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d2b6-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2b6-126">CommonParameters</span></span>
<span data-ttu-id="2d2b6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2b6-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2b6-129">입력</span><span class="sxs-lookup"><span data-stu-id="2d2b6-129">INPUTS</span></span>

## <span data-ttu-id="2d2b6-130">출력</span><span class="sxs-lookup"><span data-stu-id="2d2b6-130">OUTPUTS</span></span>

### <span data-ttu-id="2d2b6-131">OfferDelegation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="2d2b6-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="2d2b6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2d2b6-132">NOTES</span></span>

## <span data-ttu-id="2d2b6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d2b6-133">RELATED LINKS</span></span>

