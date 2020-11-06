---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522923"
---
# <span data-ttu-id="b3472-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="b3472-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="b3472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3472-102">SYNOPSIS</span></span>
<span data-ttu-id="b3472-103">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-103">Get the offer metrics.</span></span>

## <span data-ttu-id="b3472-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3472-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="b3472-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3472-105">DESCRIPTION</span></span>
<span data-ttu-id="b3472-106">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-106">Get the offer metrics.</span></span>

## <span data-ttu-id="b3472-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3472-107">EXAMPLES</span></span>

### <span data-ttu-id="b3472-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3472-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="b3472-109">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-109">Get the offer metrics.</span></span>

## <span data-ttu-id="b3472-110">변수</span><span class="sxs-lookup"><span data-stu-id="b3472-110">PARAMETERS</span></span>

### <span data-ttu-id="b3472-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="b3472-111">-OfferName</span></span>
<span data-ttu-id="b3472-112">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-112">Name of an offer.</span></span>

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

### <span data-ttu-id="b3472-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3472-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3472-114">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b3472-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3472-115">CommonParameters</span></span>
<span data-ttu-id="b3472-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3472-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3472-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3472-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3472-118">입력</span><span class="sxs-lookup"><span data-stu-id="b3472-118">INPUTS</span></span>

## <span data-ttu-id="b3472-119">출력</span><span class="sxs-lookup"><span data-stu-id="b3472-119">OUTPUTS</span></span>

### <span data-ttu-id="b3472-120">Microsoft AzureStack. 관리. 미터법</span><span class="sxs-lookup"><span data-stu-id="b3472-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="b3472-121">상속자</span><span class="sxs-lookup"><span data-stu-id="b3472-121">NOTES</span></span>

## <span data-ttu-id="b3472-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3472-122">RELATED LINKS</span></span>

