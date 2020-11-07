---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874815"
---
# <span data-ttu-id="85d1d-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="85d1d-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="85d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="85d1d-103">위임 된 행사 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="85d1d-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="85d1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85d1d-104">SYNTAX</span></span>

### <span data-ttu-id="85d1d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="85d1d-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="85d1d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="85d1d-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="85d1d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="85d1d-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="85d1d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="85d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="85d1d-109">위임 된 행사 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="85d1d-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="85d1d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="85d1d-110">EXAMPLES</span></span>

### <span data-ttu-id="85d1d-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85d1d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="85d1d-112">위임 된 행사 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="85d1d-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="85d1d-113">변수</span><span class="sxs-lookup"><span data-stu-id="85d1d-113">PARAMETERS</span></span>

### <span data-ttu-id="85d1d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="85d1d-114">-Name</span></span>
<span data-ttu-id="85d1d-115">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="85d1d-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="85d1d-116">-OfferName</span></span>
<span data-ttu-id="85d1d-117">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d1d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d1d-118">-ResourceGroupName</span></span>
<span data-ttu-id="85d1d-119">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d1d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85d1d-120">-ResourceId</span></span>
<span data-ttu-id="85d1d-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d1d-122">-생략</span><span class="sxs-lookup"><span data-stu-id="85d1d-122">-Skip</span></span>
<span data-ttu-id="85d1d-123">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d1d-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="85d1d-124">-Top</span></span>
<span data-ttu-id="85d1d-125">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="85d1d-126">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d1d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d1d-127">CommonParameters</span></span>
<span data-ttu-id="85d1d-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85d1d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d1d-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85d1d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d1d-130">입력</span><span class="sxs-lookup"><span data-stu-id="85d1d-130">INPUTS</span></span>

## <span data-ttu-id="85d1d-131">출력</span><span class="sxs-lookup"><span data-stu-id="85d1d-131">OUTPUTS</span></span>

### <span data-ttu-id="85d1d-132">OfferDelegation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="85d1d-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="85d1d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="85d1d-133">NOTES</span></span>

## <span data-ttu-id="85d1d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85d1d-134">RELATED LINKS</span></span>

