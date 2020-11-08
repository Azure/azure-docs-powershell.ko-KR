---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047003"
---
# <span data-ttu-id="51141-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="51141-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="51141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51141-102">SYNOPSIS</span></span>
<span data-ttu-id="51141-103">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51141-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="51141-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51141-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51141-105">설명은</span><span class="sxs-lookup"><span data-stu-id="51141-105">DESCRIPTION</span></span>
<span data-ttu-id="51141-106">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51141-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="51141-107">예제의</span><span class="sxs-lookup"><span data-stu-id="51141-107">EXAMPLES</span></span>

### <span data-ttu-id="51141-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="51141-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="51141-109">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51141-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="51141-110">변수</span><span class="sxs-lookup"><span data-stu-id="51141-110">PARAMETERS</span></span>

### <span data-ttu-id="51141-111">-위치</span><span class="sxs-lookup"><span data-stu-id="51141-111">-Location</span></span>
<span data-ttu-id="51141-112">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="51141-112">Location of the resource.</span></span>

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

### <span data-ttu-id="51141-113">-이름</span><span class="sxs-lookup"><span data-stu-id="51141-113">-Name</span></span>
<span data-ttu-id="51141-114">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51141-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="51141-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="51141-115">-OfferName</span></span>
<span data-ttu-id="51141-116">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51141-116">Name of an offer.</span></span>

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

### <span data-ttu-id="51141-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51141-117">-ResourceGroupName</span></span>
<span data-ttu-id="51141-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="51141-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="51141-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51141-119">-SubscriptionId</span></span>
<span data-ttu-id="51141-120">위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51141-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="51141-121">-확인</span><span class="sxs-lookup"><span data-stu-id="51141-121">-Confirm</span></span>
<span data-ttu-id="51141-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51141-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51141-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51141-123">-WhatIf</span></span>
<span data-ttu-id="51141-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51141-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51141-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51141-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51141-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51141-126">CommonParameters</span></span>
<span data-ttu-id="51141-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51141-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51141-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51141-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51141-129">입력</span><span class="sxs-lookup"><span data-stu-id="51141-129">INPUTS</span></span>

## <span data-ttu-id="51141-130">출력</span><span class="sxs-lookup"><span data-stu-id="51141-130">OUTPUTS</span></span>

### <span data-ttu-id="51141-131">OfferDelegation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="51141-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="51141-132">상속자</span><span class="sxs-lookup"><span data-stu-id="51141-132">NOTES</span></span>

## <span data-ttu-id="51141-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51141-133">RELATED LINKS</span></span>

