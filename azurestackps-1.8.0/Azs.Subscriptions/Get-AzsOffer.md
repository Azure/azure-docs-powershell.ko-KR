---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874773"
---
# <span data-ttu-id="0a7af-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0a7af-101">Get-AzsOffer</span></span>

## <span data-ttu-id="0a7af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a7af-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7af-103">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-103">Get the list of public offers.</span></span>

## <span data-ttu-id="0a7af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a7af-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a7af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a7af-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7af-106">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-106">Get the list of public offers.</span></span>

## <span data-ttu-id="0a7af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0a7af-107">EXAMPLES</span></span>

### <span data-ttu-id="0a7af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a7af-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="0a7af-109">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-109">Get the list of public offers.</span></span>

## <span data-ttu-id="0a7af-110">변수</span><span class="sxs-lookup"><span data-stu-id="0a7af-110">PARAMETERS</span></span>

### <span data-ttu-id="0a7af-111">-생략</span><span class="sxs-lookup"><span data-stu-id="0a7af-111">-Skip</span></span>
<span data-ttu-id="0a7af-112">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7af-113">-위쪽</span><span class="sxs-lookup"><span data-stu-id="0a7af-113">-Top</span></span>
<span data-ttu-id="0a7af-114">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0a7af-115">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7af-116">-공급자</span><span class="sxs-lookup"><span data-stu-id="0a7af-116">-Provider</span></span>
<span data-ttu-id="0a7af-117">위임 된 공급자 이름을 지정 하는 선택적 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="0a7af-118">이 매개 변수는 사용 되지 않으며 향후에 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7af-119">CommonParameters</span></span>
<span data-ttu-id="0a7af-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a7af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7af-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a7af-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7af-122">입력</span><span class="sxs-lookup"><span data-stu-id="0a7af-122">INPUTS</span></span>

## <span data-ttu-id="0a7af-123">출력</span><span class="sxs-lookup"><span data-stu-id="0a7af-123">OUTPUTS</span></span>

### <span data-ttu-id="0a7af-124">Microsoft AzureStack. 경영진. 제안</span><span class="sxs-lookup"><span data-stu-id="0a7af-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="0a7af-125">상속자</span><span class="sxs-lookup"><span data-stu-id="0a7af-125">NOTES</span></span>

## <span data-ttu-id="0a7af-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a7af-126">RELATED LINKS</span></span>
