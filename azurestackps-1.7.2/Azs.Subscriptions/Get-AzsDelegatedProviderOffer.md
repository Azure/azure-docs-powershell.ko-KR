---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874284"
---
# <span data-ttu-id="27813-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="27813-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="27813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27813-102">SYNOPSIS</span></span>
<span data-ttu-id="27813-103">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27813-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="27813-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27813-104">SYNTAX</span></span>

### <span data-ttu-id="27813-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="27813-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="27813-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="27813-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="27813-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27813-107">DESCRIPTION</span></span>
<span data-ttu-id="27813-108">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27813-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="27813-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27813-109">EXAMPLES</span></span>

### <span data-ttu-id="27813-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27813-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="27813-111">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27813-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="27813-112">변수</span><span class="sxs-lookup"><span data-stu-id="27813-112">PARAMETERS</span></span>

### <span data-ttu-id="27813-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="27813-113">-DelegatedProviderId</span></span>
<span data-ttu-id="27813-114">위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="27813-114">Id of the delegated provider.</span></span>

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

### <span data-ttu-id="27813-115">-이름</span><span class="sxs-lookup"><span data-stu-id="27813-115">-Name</span></span>
<span data-ttu-id="27813-116">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27813-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27813-117">-생략</span><span class="sxs-lookup"><span data-stu-id="27813-117">-Skip</span></span>
<span data-ttu-id="27813-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="27813-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="27813-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="27813-119">-Top</span></span>
<span data-ttu-id="27813-120">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27813-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="27813-121">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27813-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="27813-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27813-122">CommonParameters</span></span>
<span data-ttu-id="27813-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27813-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27813-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27813-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27813-125">입력</span><span class="sxs-lookup"><span data-stu-id="27813-125">INPUTS</span></span>

## <span data-ttu-id="27813-126">출력</span><span class="sxs-lookup"><span data-stu-id="27813-126">OUTPUTS</span></span>

### <span data-ttu-id="27813-127">Microsoft AzureStack. 경영진. 제안</span><span class="sxs-lookup"><span data-stu-id="27813-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="27813-128">상속자</span><span class="sxs-lookup"><span data-stu-id="27813-128">NOTES</span></span>

## <span data-ttu-id="27813-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27813-129">RELATED LINKS</span></span>

