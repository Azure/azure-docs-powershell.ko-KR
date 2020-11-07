---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874594"
---
# <span data-ttu-id="b5f52-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="b5f52-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="b5f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f52-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f52-103">지정 된 timespan 동안 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="b5f52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5f52-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b5f52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5f52-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f52-106">지정 된 timespan 동안 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="b5f52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5f52-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5f52-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="b5f52-109">지난 24 시간에서 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="b5f52-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5f52-110">PARAMETERS</span></span>

### <span data-ttu-id="b5f52-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="b5f52-111">-SubscriberId</span></span>
<span data-ttu-id="b5f52-112">테 넌 트 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="b5f52-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="b5f52-113">-ReportedStartTime</span></span>
<span data-ttu-id="b5f52-114">보고 된 시작 시간 (포함)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-114">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f52-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="b5f52-115">-AggregationGranularity</span></span>
<span data-ttu-id="b5f52-116">집계 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="b5f52-117">-생략</span><span class="sxs-lookup"><span data-stu-id="b5f52-117">-Skip</span></span>
<span data-ttu-id="b5f52-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f52-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="b5f52-119">-ReportedEndTime</span></span>
<span data-ttu-id="b5f52-120">보고 된 종료 시간 (제외)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-120">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f52-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b5f52-121">-ContinuationToken</span></span>
<span data-ttu-id="b5f52-122">연속 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-122">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f52-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="b5f52-123">-Top</span></span>
<span data-ttu-id="b5f52-124">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b5f52-125">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f52-126">CommonParameters</span></span>
<span data-ttu-id="b5f52-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f52-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f52-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f52-129">입력</span><span class="sxs-lookup"><span data-stu-id="b5f52-129">INPUTS</span></span>

## <span data-ttu-id="b5f52-130">출력</span><span class="sxs-lookup"><span data-stu-id="b5f52-130">OUTPUTS</span></span>

### <span data-ttu-id="b5f52-131">UsageAggregate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="b5f52-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="b5f52-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b5f52-132">NOTES</span></span>

## <span data-ttu-id="b5f52-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5f52-133">RELATED LINKS</span></span>
