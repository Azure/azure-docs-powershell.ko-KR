---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874370"
---
# <span data-ttu-id="98de2-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="98de2-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="98de2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98de2-102">SYNOPSIS</span></span>
<span data-ttu-id="98de2-103">지정 된 테 넌 트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="98de2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98de2-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98de2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="98de2-105">DESCRIPTION</span></span>
<span data-ttu-id="98de2-106">지정 된 테 넌 트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="98de2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="98de2-107">EXAMPLES</span></span>

### <span data-ttu-id="98de2-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98de2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="98de2-109">지정 된 테 넌 트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="98de2-110">변수</span><span class="sxs-lookup"><span data-stu-id="98de2-110">PARAMETERS</span></span>

### <span data-ttu-id="98de2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="98de2-111">-Force</span></span>
<span data-ttu-id="98de2-112">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="98de2-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98de2-113">-SubscriptionId</span></span>
<span data-ttu-id="98de2-114">구독 Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98de2-115">-확인</span><span class="sxs-lookup"><span data-stu-id="98de2-115">-Confirm</span></span>
<span data-ttu-id="98de2-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98de2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98de2-117">-WhatIf</span></span>
<span data-ttu-id="98de2-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98de2-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98de2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98de2-120">CommonParameters</span></span>
<span data-ttu-id="98de2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98de2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98de2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98de2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98de2-123">입력</span><span class="sxs-lookup"><span data-stu-id="98de2-123">INPUTS</span></span>

## <span data-ttu-id="98de2-124">출력</span><span class="sxs-lookup"><span data-stu-id="98de2-124">OUTPUTS</span></span>

## <span data-ttu-id="98de2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="98de2-125">NOTES</span></span>

## <span data-ttu-id="98de2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98de2-126">RELATED LINKS</span></span>

