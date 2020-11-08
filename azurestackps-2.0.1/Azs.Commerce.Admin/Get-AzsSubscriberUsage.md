---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045344"
---
# <span data-ttu-id="31211-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="31211-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="31211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31211-102">SYNOPSIS</span></span>
<span data-ttu-id="31211-103">사용자가 UsageAggregates 하는 SubscriberUsageAggregates의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31211-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="31211-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31211-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31211-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31211-105">DESCRIPTION</span></span>
<span data-ttu-id="31211-106">사용자가 UsageAggregates 하는 SubscriberUsageAggregates의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31211-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="31211-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31211-107">EXAMPLES</span></span>

### <span data-ttu-id="31211-108">예제 1: 날짜별로 집계 된 사용 현황 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="31211-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="31211-109">일일으로 집계 된 공급자에서 모든 테 넌 트에 대 한 총 30 년 12 월 2019 (UTC)에 대 한 사용량 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31211-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="31211-110">ReportedStartTime 및 ReportedEndTime는 일별로 반올림 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31211-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="31211-111">서비스 관리자로 호출 하면 모든 테 넌 트에 대 한 모든 사용 데이터가 효율적으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31211-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="31211-112">예제 2: 시간별로 집계 한 사용량 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="31211-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="31211-113">시간을 기준으로 집계 된 2019 년 12 월 30 일 (UTC)의 12am 사이 사용량 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31211-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="31211-114">ReportedStartTime 및 ReportedEndTime는 시간으로 반올림 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31211-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="31211-115">마찬가지로 서비스 관리자로 호출 되 면 모든 테 넌 트에 대 한 모든 사용 데이터가 효율적으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31211-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="31211-116">변수</span><span class="sxs-lookup"><span data-stu-id="31211-116">PARAMETERS</span></span>

### <span data-ttu-id="31211-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="31211-117">-AggregationGranularity</span></span>
<span data-ttu-id="31211-118">집계 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="31211-119">-ContinuationToken</span></span>
<span data-ttu-id="31211-120">연속 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31211-121">-DefaultProfile</span></span>
<span data-ttu-id="31211-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="31211-123">-ReportedEndTime</span></span>
<span data-ttu-id="31211-124">보고 된 종료 시간 (제외)입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="31211-125">-ReportedStartTime</span></span>
<span data-ttu-id="31211-126">보고 된 시작 시간 (포함)입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="31211-127">-SubscriberId</span></span>
<span data-ttu-id="31211-128">테 넌 트 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31211-129">-SubscriptionId</span></span>
<span data-ttu-id="31211-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="31211-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="31211-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31211-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31211-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31211-132">CommonParameters</span></span>
<span data-ttu-id="31211-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31211-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31211-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31211-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31211-135">입력</span><span class="sxs-lookup"><span data-stu-id="31211-135">INPUTS</span></span>

## <span data-ttu-id="31211-136">출력</span><span class="sxs-lookup"><span data-stu-id="31211-136">OUTPUTS</span></span>

### <span data-ttu-id="31211-137">Api20150601Preview. IUsageAggregate에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31211-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="31211-138">상속자</span><span class="sxs-lookup"><span data-stu-id="31211-138">NOTES</span></span>

## <span data-ttu-id="31211-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31211-139">RELATED LINKS</span></span>

