---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec978cebfaa12f574ce20638347839fd70099df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701752"
---
# <span data-ttu-id="6fe2e-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="6fe2e-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="6fe2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe2e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe2e-103">제공 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-103">Removes the offer delegation</span></span>

## <span data-ttu-id="6fe2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fe2e-104">SYNTAX</span></span>

### <span data-ttu-id="6fe2e-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fe2e-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe2e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="6fe2e-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe2e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6fe2e-107">DESCRIPTION</span></span>
<span data-ttu-id="6fe2e-108">제공 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-108">Removes the offer delegation</span></span>

## <span data-ttu-id="6fe2e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6fe2e-109">EXAMPLES</span></span>

### <span data-ttu-id="6fe2e-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6fe2e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="6fe2e-111">제공 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-111">Removes the offer delegation</span></span>

## <span data-ttu-id="6fe2e-112">변수</span><span class="sxs-lookup"><span data-stu-id="6fe2e-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe2e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6fe2e-113">-Force</span></span>
<span data-ttu-id="6fe2e-114">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="6fe2e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6fe2e-115">-Name</span></span>
<span data-ttu-id="6fe2e-116">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="6fe2e-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6fe2e-117">-OfferName</span></span>
<span data-ttu-id="6fe2e-118">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-118">Name of an offer.</span></span>

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

### <span data-ttu-id="6fe2e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe2e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6fe2e-120">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6fe2e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe2e-121">-ResourceId</span></span>
<span data-ttu-id="6fe2e-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-122">The resource id.</span></span>

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

### <span data-ttu-id="6fe2e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6fe2e-123">-Confirm</span></span>
<span data-ttu-id="6fe2e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe2e-125">-WhatIf</span></span>
<span data-ttu-id="6fe2e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe2e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe2e-128">CommonParameters</span></span>
<span data-ttu-id="6fe2e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe2e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe2e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe2e-131">입력</span><span class="sxs-lookup"><span data-stu-id="6fe2e-131">INPUTS</span></span>

## <span data-ttu-id="6fe2e-132">출력</span><span class="sxs-lookup"><span data-stu-id="6fe2e-132">OUTPUTS</span></span>

## <span data-ttu-id="6fe2e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6fe2e-133">NOTES</span></span>

## <span data-ttu-id="6fe2e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fe2e-134">RELATED LINKS</span></span>

