---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382670"
---
# <span data-ttu-id="76ebe-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="76ebe-101">Get-AzMetric</span></span>

## <span data-ttu-id="76ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="76ebe-103">리소스의 메트릭 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="76ebe-104">구문</span><span class="sxs-lookup"><span data-stu-id="76ebe-104">SYNTAX</span></span>

### <span data-ttu-id="76ebe-105">GetWithDefaultParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="76ebe-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ebe-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="76ebe-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ebe-107">설명</span><span class="sxs-lookup"><span data-stu-id="76ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="76ebe-108">**Get-AzMetric** cmdlet은 지정된 리소스에 대한 메트릭 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="76ebe-109">예제</span><span class="sxs-lookup"><span data-stu-id="76ebe-109">EXAMPLES</span></span>

### <span data-ttu-id="76ebe-110">예제 1: 요약된 출력이 있는 메트릭을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="76ebe-111">이 명령은 1분의 시간 단위로 website3에 대한 메트릭 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="76ebe-112">예제 2: 자세한 출력이 있는 메트릭을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="76ebe-113">이 명령은 1분의 시간 단위로 website3에 대한 메트릭 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="76ebe-114">출력이 자세히 설명됩니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-114">The output is detailed.</span></span>

### <span data-ttu-id="76ebe-115">예제 3: 지정된 메트릭에 대한 자세한 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="76ebe-116">이 명령은 요청 메트릭에 대한 자세한 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="76ebe-117">예제 4: 지정된 차원 필터를 사용하여 지정된 메트릭에 대한 요약 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="76ebe-118">이 명령은 지정된 차원 필터 및 집계 형식을 사용하여 PageViews 메트릭에 대한 요약된 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="76ebe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76ebe-119">PARAMETERS</span></span>

### <span data-ttu-id="76ebe-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="76ebe-120">-AggregationType</span></span>
<span data-ttu-id="76ebe-121">쿼리의 집계 유형</span><span class="sxs-lookup"><span data-stu-id="76ebe-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ebe-122">-DefaultProfile</span></span>
<span data-ttu-id="76ebe-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ebe-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="76ebe-124">-DetailedOutput</span></span>
<span data-ttu-id="76ebe-125">이 cmdlet이 자세한 출력을 표시하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="76ebe-126">기본적으로 출력은 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="76ebe-127">-EndTime</span></span>
<span data-ttu-id="76ebe-128">로컬 시간으로 쿼리의 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="76ebe-129">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="76ebe-130">-MetricFilter</span></span>
<span data-ttu-id="76ebe-131">메트릭을 쿼리할 메트릭 차원 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="76ebe-132">-MetricName</span></span>
<span data-ttu-id="76ebe-133">메트릭의 이름 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="76ebe-134">-MetricNamespace</span></span>
<span data-ttu-id="76ebe-135">메트릭을 쿼리할 메트릭 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="76ebe-136">-OrderBy</span></span>
<span data-ttu-id="76ebe-137">결과 정렬 및 정렬 방향(예: sum asc)에 사용할 집계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76ebe-138">-ResourceId</span></span>
<span data-ttu-id="76ebe-139">메트릭의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="76ebe-140">-ResultType</span></span>
<span data-ttu-id="76ebe-141">반환할 결과 형식(메타데이터 또는 데이터)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="76ebe-142">-StartTime</span></span>
<span data-ttu-id="76ebe-143">로컬 시간으로 쿼리의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="76ebe-144">기본값은 현재 현지 시간에서 1시간을 -1로 합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="76ebe-145">-TimeGrain</span></span>
<span data-ttu-id="76ebe-146">hh:mm:ss 형식의 **TimeSpan** 개체로 메트릭의 시간 단위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-147">-Top</span><span class="sxs-lookup"><span data-stu-id="76ebe-147">-Top</span></span>
<span data-ttu-id="76ebe-148">검색할 레코드의 최대 수(기본값:10)를 지정하여 $filter.</span><span class="sxs-lookup"><span data-stu-id="76ebe-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ebe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ebe-149">CommonParameters</span></span>
<span data-ttu-id="76ebe-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76ebe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ebe-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76ebe-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ebe-152">입력</span><span class="sxs-lookup"><span data-stu-id="76ebe-152">INPUTS</span></span>

### <span data-ttu-id="76ebe-153">System.String</span><span class="sxs-lookup"><span data-stu-id="76ebe-153">System.String</span></span>

### <span data-ttu-id="76ebe-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="76ebe-154">System.TimeSpan</span></span>

### <span data-ttu-id="76ebe-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="76ebe-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="76ebe-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="76ebe-156">System.DateTime</span></span>

### <span data-ttu-id="76ebe-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="76ebe-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="76ebe-158">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="76ebe-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="76ebe-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="76ebe-159">System.String[]</span></span>

### <span data-ttu-id="76ebe-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76ebe-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76ebe-161">출력</span><span class="sxs-lookup"><span data-stu-id="76ebe-161">OUTPUTS</span></span>

### <span data-ttu-id="76ebe-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="76ebe-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="76ebe-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76ebe-163">NOTES</span></span>

<span data-ttu-id="76ebe-164">지원되는 메트릭에 대한 자세한 내용은 다음에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="76ebe-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="76ebe-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76ebe-165">RELATED LINKS</span></span>

<span data-ttu-id="76ebe-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="76ebe-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>

