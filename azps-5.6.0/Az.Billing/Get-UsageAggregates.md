---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988493"
---
# <span data-ttu-id="56b68-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="56b68-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="56b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b68-102">SYNOPSIS</span></span>
<span data-ttu-id="56b68-103">보고된 Azure 구독 사용 현황 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="56b68-104">구문</span><span class="sxs-lookup"><span data-stu-id="56b68-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b68-105">설명</span><span class="sxs-lookup"><span data-stu-id="56b68-105">DESCRIPTION</span></span>
<span data-ttu-id="56b68-106">**Get-UsageAggregates** cmdlet은 다음 속성에 의해 집계된 Azure 구독 사용 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="56b68-107">사용량이 보고된 시작 및 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="56b68-108">집계 정밀도(매일 또는 시간당).</span><span class="sxs-lookup"><span data-stu-id="56b68-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="56b68-109">동일한 리소스의 여러 인스턴스에 대한 인스턴스 수준 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="56b68-110">일관된 결과를 위해 반환된 데이터는 Azure 리소스에서 사용량 세부 정보를 보고한 때를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="56b68-111">자세한 내용은 Azure Billing REST API 참조(Microsoft Developer Network https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) 라이브러리를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="56b68-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="56b68-112">예제</span><span class="sxs-lookup"><span data-stu-id="56b68-112">EXAMPLES</span></span>

### <span data-ttu-id="56b68-113">예제 1: 구독 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="56b68-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="56b68-114">이 명령은 2015년 5월 2일과 2015년 5월 5일 사이에 구독에 대한 보고된 사용 현황 데이터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="56b68-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56b68-115">PARAMETERS</span></span>

### <span data-ttu-id="56b68-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="56b68-116">-AggregationGranularity</span></span>
<span data-ttu-id="56b68-117">데이터의 집계 정밀도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="56b68-118">유효한 값은 일별 및 시간별 값입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="56b68-119">기본값은 Daily입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b68-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="56b68-120">-ContinuationToken</span></span>
<span data-ttu-id="56b68-121">이전 호출의 응답 본문에서 검색된 연속 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="56b68-122">큰 결과 집합의 경우 연속 토큰을 사용하여 응답을 페이지화합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="56b68-123">연속 토큰은 진행률에 대한 책갈피 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="56b68-124">이 매개 변수를 지정하지 않으면 *ReportedStartTime에* 지정된 날짜 또는 시간의 시작부터 데이터가 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="56b68-125">데이터지만 페이지에 대한 응답의 다음 링크를 따르는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="56b68-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b68-126">-DefaultProfile</span></span>
<span data-ttu-id="56b68-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b68-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="56b68-128">-ReportedEndTime</span></span>
<span data-ttu-id="56b68-129">Azure 청구 시스템에 리소스 사용량이 기록된 경우 보고된 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="56b68-130">Azure는 전 세계 여러 데이터 센터를 아우르는 분산 시스템입니다. 따라서 리소스가 실제로 사용된 시기, 리소스 사용 시간, 사용량 이벤트가 청구 시스템에 도달한 시기 사이의 지연이 있습니다. 이는 리소스 사용량 보고 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="56b68-131">일정 기간 동안 보고되는 구독에 대한 모든 사용 이벤트를 얻기 위해 보고된 시간으로 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="56b68-132">보고된 시간으로 쿼리하는 경우에도 cmdlet은 리소스 사용 시간별로 응답 데이터를 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="56b68-133">리소스 사용 데이터는 데이터를 분석하는 데 유용한 피벗입니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="56b68-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="56b68-134">-ReportedStartTime</span></span>
<span data-ttu-id="56b68-135">Azure 청구 시스템에 리소스 사용량이 기록된 시기에 대한 보고된 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="56b68-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="56b68-136">-ShowDetails</span></span>
<span data-ttu-id="56b68-137">이 cmdlet이 사용량 데이터와 함께 인스턴스 수준 세부 정보를 반환하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="56b68-138">기본값은 $True.</span><span class="sxs-lookup"><span data-stu-id="56b68-138">The default value is $True.</span></span>
<span data-ttu-id="56b68-139">$False 경우 서비스는 서버 쪽에서 결과를 집계하므로 집계 그룹 수가 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="56b68-140">예를 들어 세 개의 웹 사이트를 실행하는 경우 기본적으로 웹 사이트 사용량에 대한 세 개의 광고 항목이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="56b68-141">그러나 값이 $False 경우 동일한 **구독Id,** **meterId,** **usageStartTime** 및 **usageEndTime에** 대한 모든 데이터가 단일 줄 항목으로 축소됩니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b68-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b68-142">CommonParameters</span></span>
<span data-ttu-id="56b68-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56b68-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b68-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="56b68-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b68-145">입력</span><span class="sxs-lookup"><span data-stu-id="56b68-145">INPUTS</span></span>

### <span data-ttu-id="56b68-146">없음</span><span class="sxs-lookup"><span data-stu-id="56b68-146">None</span></span>

## <span data-ttu-id="56b68-147">출력</span><span class="sxs-lookup"><span data-stu-id="56b68-147">OUTPUTS</span></span>

### <span data-ttu-id="56b68-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="56b68-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="56b68-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56b68-149">NOTES</span></span>

## <span data-ttu-id="56b68-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56b68-150">RELATED LINKS</span></span>
