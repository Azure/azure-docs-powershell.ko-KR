---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689090"
---
# <span data-ttu-id="dfb4c-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="dfb4c-101">Get-AzsOffer</span></span>

## <span data-ttu-id="dfb4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb4c-103">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-103">Get the list of public offers.</span></span>

## <span data-ttu-id="dfb4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfb4c-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dfb4c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb4c-106">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-106">Get the list of public offers.</span></span>

## <span data-ttu-id="dfb4c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb4c-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dfb4c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="dfb4c-109">공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-109">Get the list of public offers.</span></span>

## <span data-ttu-id="dfb4c-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfb4c-110">PARAMETERS</span></span>

### <span data-ttu-id="dfb4c-111">-생략</span><span class="sxs-lookup"><span data-stu-id="dfb4c-111">-Skip</span></span>
<span data-ttu-id="dfb4c-112">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dfb4c-113">-위쪽</span><span class="sxs-lookup"><span data-stu-id="dfb4c-113">-Top</span></span>
<span data-ttu-id="dfb4c-114">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dfb4c-115">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dfb4c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb4c-116">CommonParameters</span></span>
<span data-ttu-id="dfb4c-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb4c-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb4c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb4c-119">입력</span><span class="sxs-lookup"><span data-stu-id="dfb4c-119">INPUTS</span></span>

## <span data-ttu-id="dfb4c-120">출력</span><span class="sxs-lookup"><span data-stu-id="dfb4c-120">OUTPUTS</span></span>

### <span data-ttu-id="dfb4c-121">Microsoft AzureStack. 경영진. 제안</span><span class="sxs-lookup"><span data-stu-id="dfb4c-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="dfb4c-122">상속자</span><span class="sxs-lookup"><span data-stu-id="dfb4c-122">NOTES</span></span>

## <span data-ttu-id="dfb4c-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfb4c-123">RELATED LINKS</span></span>

