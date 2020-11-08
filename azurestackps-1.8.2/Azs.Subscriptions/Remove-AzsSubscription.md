---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046945"
---
# <span data-ttu-id="1d8b7-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="1d8b7-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="1d8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8b7-103">지정한 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1d8b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d8b7-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8b7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="1d8b7-106">지정한 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1d8b7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d8b7-107">EXAMPLES</span></span>

### <span data-ttu-id="1d8b7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d8b7-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="1d8b7-109">지정한 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="1d8b7-110">변수</span><span class="sxs-lookup"><span data-stu-id="1d8b7-110">PARAMETERS</span></span>

### <span data-ttu-id="1d8b7-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d8b7-111">-SubscriptionId</span></span>
<span data-ttu-id="1d8b7-112">구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="1d8b7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1d8b7-113">-Force</span></span>
<span data-ttu-id="1d8b7-114">메시지를 표시 하지 않고 구독 제거</span><span class="sxs-lookup"><span data-stu-id="1d8b7-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="1d8b7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8b7-115">-WhatIf</span></span>
<span data-ttu-id="1d8b7-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8b7-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8b7-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1d8b7-118">-Confirm</span></span>
<span data-ttu-id="1d8b7-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8b7-120">CommonParameters</span></span>
<span data-ttu-id="1d8b7-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d8b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8b7-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8b7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8b7-123">입력</span><span class="sxs-lookup"><span data-stu-id="1d8b7-123">INPUTS</span></span>

## <span data-ttu-id="1d8b7-124">출력</span><span class="sxs-lookup"><span data-stu-id="1d8b7-124">OUTPUTS</span></span>

## <span data-ttu-id="1d8b7-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1d8b7-125">NOTES</span></span>

## <span data-ttu-id="1d8b7-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d8b7-126">RELATED LINKS</span></span>
