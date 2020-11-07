---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874774"
---
# <span data-ttu-id="e4a17-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="e4a17-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="e4a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4a17-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a17-103">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="e4a17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4a17-104">SYNTAX</span></span>

### <span data-ttu-id="e4a17-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4a17-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e4a17-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e4a17-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4a17-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4a17-107">DESCRIPTION</span></span>
<span data-ttu-id="e4a17-108">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="e4a17-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4a17-109">EXAMPLES</span></span>

### <span data-ttu-id="e4a17-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4a17-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="e4a17-111">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="e4a17-112">변수</span><span class="sxs-lookup"><span data-stu-id="e4a17-112">PARAMETERS</span></span>

### <span data-ttu-id="e4a17-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e4a17-113">-OfferName</span></span>
<span data-ttu-id="e4a17-114">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a17-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="e4a17-115">-DelegatedProviderId</span></span>
<span data-ttu-id="e4a17-116">위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-116">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a17-117">-생략</span><span class="sxs-lookup"><span data-stu-id="e4a17-117">-Skip</span></span>
<span data-ttu-id="e4a17-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a17-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e4a17-119">-Top</span></span>
<span data-ttu-id="e4a17-120">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e4a17-121">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a17-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a17-122">CommonParameters</span></span>
<span data-ttu-id="e4a17-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a17-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a17-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a17-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a17-125">입력</span><span class="sxs-lookup"><span data-stu-id="e4a17-125">INPUTS</span></span>

## <span data-ttu-id="e4a17-126">출력</span><span class="sxs-lookup"><span data-stu-id="e4a17-126">OUTPUTS</span></span>

### <span data-ttu-id="e4a17-127">Microsoft AzureStack. 경영진. 제안</span><span class="sxs-lookup"><span data-stu-id="e4a17-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="e4a17-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e4a17-128">NOTES</span></span>

## <span data-ttu-id="e4a17-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4a17-129">RELATED LINKS</span></span>
