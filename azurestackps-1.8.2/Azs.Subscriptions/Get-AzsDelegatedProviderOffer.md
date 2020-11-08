---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047010"
---
# <span data-ttu-id="3c273-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="3c273-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="3c273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c273-102">SYNOPSIS</span></span>
<span data-ttu-id="3c273-103">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="3c273-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c273-104">SYNTAX</span></span>

### <span data-ttu-id="3c273-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c273-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3c273-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3c273-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c273-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3c273-107">DESCRIPTION</span></span>
<span data-ttu-id="3c273-108">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="3c273-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3c273-109">EXAMPLES</span></span>

### <span data-ttu-id="3c273-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c273-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="3c273-111">지정 된 위임 공급자에 대 한 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="3c273-112">변수</span><span class="sxs-lookup"><span data-stu-id="3c273-112">PARAMETERS</span></span>

### <span data-ttu-id="3c273-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="3c273-113">-OfferName</span></span>
<span data-ttu-id="3c273-114">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-114">Name of the offer.</span></span>

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

### <span data-ttu-id="3c273-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="3c273-115">-DelegatedProviderId</span></span>
<span data-ttu-id="3c273-116">위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-116">Id of the delegated provider.</span></span>

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

### <span data-ttu-id="3c273-117">-생략</span><span class="sxs-lookup"><span data-stu-id="3c273-117">-Skip</span></span>
<span data-ttu-id="3c273-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3c273-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="3c273-119">-Top</span></span>
<span data-ttu-id="3c273-120">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3c273-121">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3c273-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c273-122">CommonParameters</span></span>
<span data-ttu-id="3c273-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c273-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c273-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c273-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c273-125">입력</span><span class="sxs-lookup"><span data-stu-id="3c273-125">INPUTS</span></span>

## <span data-ttu-id="3c273-126">출력</span><span class="sxs-lookup"><span data-stu-id="3c273-126">OUTPUTS</span></span>

### <span data-ttu-id="3c273-127">Microsoft AzureStack. 경영진. 제안</span><span class="sxs-lookup"><span data-stu-id="3c273-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="3c273-128">상속자</span><span class="sxs-lookup"><span data-stu-id="3c273-128">NOTES</span></span>

## <span data-ttu-id="3c273-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c273-129">RELATED LINKS</span></span>
