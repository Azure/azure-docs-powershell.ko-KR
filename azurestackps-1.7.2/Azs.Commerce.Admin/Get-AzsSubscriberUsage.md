---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873779"
---
# <span data-ttu-id="2fb24-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="2fb24-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="2fb24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fb24-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb24-103">지정 된 timespan 동안 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="2fb24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fb24-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2fb24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2fb24-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb24-106">지정 된 timespan 동안 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="2fb24-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2fb24-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb24-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2fb24-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="2fb24-109">지난 24 시간에서 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="2fb24-110">변수</span><span class="sxs-lookup"><span data-stu-id="2fb24-110">PARAMETERS</span></span>

### <span data-ttu-id="2fb24-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="2fb24-111">-AggregationGranularity</span></span>
<span data-ttu-id="2fb24-112">집계 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-112">The aggregation granularity.</span></span>

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

### <span data-ttu-id="2fb24-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2fb24-113">-ContinuationToken</span></span>
<span data-ttu-id="2fb24-114">연속 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-114">The continuation token.</span></span>

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

### <span data-ttu-id="2fb24-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="2fb24-115">-ReportedEndTime</span></span>
<span data-ttu-id="2fb24-116">보고 된 종료 시간 (제외)입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-116">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="2fb24-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="2fb24-117">-ReportedStartTime</span></span>
<span data-ttu-id="2fb24-118">보고 된 시작 시간 (포함)입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-118">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="2fb24-119">-생략</span><span class="sxs-lookup"><span data-stu-id="2fb24-119">-Skip</span></span>
<span data-ttu-id="2fb24-120">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-120">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2fb24-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="2fb24-121">-SubscriberId</span></span>
<span data-ttu-id="2fb24-122">테 넌 트 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-122">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="2fb24-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="2fb24-123">-Top</span></span>
<span data-ttu-id="2fb24-124">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2fb24-125">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2fb24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb24-126">CommonParameters</span></span>
<span data-ttu-id="2fb24-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb24-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb24-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb24-129">입력</span><span class="sxs-lookup"><span data-stu-id="2fb24-129">INPUTS</span></span>

## <span data-ttu-id="2fb24-130">출력</span><span class="sxs-lookup"><span data-stu-id="2fb24-130">OUTPUTS</span></span>

### <span data-ttu-id="2fb24-131">UsageAggregate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="2fb24-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="2fb24-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2fb24-132">NOTES</span></span>

## <span data-ttu-id="2fb24-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fb24-133">RELATED LINKS</span></span>

