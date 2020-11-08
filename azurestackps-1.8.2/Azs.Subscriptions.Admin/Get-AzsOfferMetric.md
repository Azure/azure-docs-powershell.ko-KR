---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046853"
---
# <span data-ttu-id="5b507-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="5b507-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="5b507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b507-102">SYNOPSIS</span></span>
<span data-ttu-id="5b507-103">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-103">Get the offer metrics.</span></span>

## <span data-ttu-id="5b507-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b507-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="5b507-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b507-105">DESCRIPTION</span></span>
<span data-ttu-id="5b507-106">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-106">Get the offer metrics.</span></span>

## <span data-ttu-id="5b507-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b507-107">EXAMPLES</span></span>

### <span data-ttu-id="5b507-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5b507-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="5b507-109">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-109">Get the offer metrics.</span></span>

## <span data-ttu-id="5b507-110">변수</span><span class="sxs-lookup"><span data-stu-id="5b507-110">PARAMETERS</span></span>

### <span data-ttu-id="5b507-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="5b507-111">-OfferName</span></span>
<span data-ttu-id="5b507-112">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-112">Name of an offer.</span></span>

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

### <span data-ttu-id="5b507-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b507-113">-ResourceGroupName</span></span>
<span data-ttu-id="5b507-114">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5b507-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b507-115">CommonParameters</span></span>
<span data-ttu-id="5b507-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b507-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b507-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b507-118">입력</span><span class="sxs-lookup"><span data-stu-id="5b507-118">INPUTS</span></span>

## <span data-ttu-id="5b507-119">출력</span><span class="sxs-lookup"><span data-stu-id="5b507-119">OUTPUTS</span></span>

### <span data-ttu-id="5b507-120">Microsoft AzureStack. 관리. 미터법</span><span class="sxs-lookup"><span data-stu-id="5b507-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="5b507-121">상속자</span><span class="sxs-lookup"><span data-stu-id="5b507-121">NOTES</span></span>

## <span data-ttu-id="5b507-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b507-122">RELATED LINKS</span></span>

