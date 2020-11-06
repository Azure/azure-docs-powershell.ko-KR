---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523103"
---
# <span data-ttu-id="9604f-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="9604f-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="9604f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9604f-102">SYNOPSIS</span></span>
<span data-ttu-id="9604f-103">제공 업체에서 연결 하거나 링크 해제할 수 있는 계획의 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="9604f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9604f-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="9604f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9604f-105">DESCRIPTION</span></span>
<span data-ttu-id="9604f-106">제공 업체에서 연결 하거나 링크 해제할 수 있는 계획의 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="9604f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9604f-107">EXAMPLES</span></span>

### <span data-ttu-id="9604f-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9604f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="9604f-109">획득 제한인 500를 사용 하 여 지정 된 계획에 대 한 새 계획 정의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="9604f-110">변수</span><span class="sxs-lookup"><span data-stu-id="9604f-110">PARAMETERS</span></span>

### <span data-ttu-id="9604f-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="9604f-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="9604f-112">단일 구독으로 얻을 수 있는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="9604f-113">지정 하지 않으면 가정 값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9604f-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="9604f-114">-PlanId</span></span>
<span data-ttu-id="9604f-115">계획 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9604f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9604f-116">CommonParameters</span></span>
<span data-ttu-id="9604f-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9604f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9604f-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9604f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9604f-119">입력</span><span class="sxs-lookup"><span data-stu-id="9604f-119">INPUTS</span></span>

## <span data-ttu-id="9604f-120">출력</span><span class="sxs-lookup"><span data-stu-id="9604f-120">OUTPUTS</span></span>

## <span data-ttu-id="9604f-121">상속자</span><span class="sxs-lookup"><span data-stu-id="9604f-121">NOTES</span></span>

## <span data-ttu-id="9604f-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9604f-122">RELATED LINKS</span></span>

