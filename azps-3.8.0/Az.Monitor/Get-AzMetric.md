---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879766"
---
# <span data-ttu-id="eea7c-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="eea7c-101">Get-AzMetric</span></span>

## <span data-ttu-id="eea7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea7c-102">SYNOPSIS</span></span>
<span data-ttu-id="eea7c-103">리소스의 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="eea7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eea7c-104">SYNTAX</span></span>

### <span data-ttu-id="eea7c-105">GetWithDefaultParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="eea7c-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea7c-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="eea7c-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eea7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eea7c-107">DESCRIPTION</span></span>
<span data-ttu-id="eea7c-108">**AzMetric** cmdlet은 지정 된 리소스에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="eea7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eea7c-109">EXAMPLES</span></span>

### <span data-ttu-id="eea7c-110">예제 1: 요약 된 출력이 있는 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="eea7c-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="eea7c-111">이 명령은 시간 그레인이 1 분인 website3에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="eea7c-112">예제 2: 자세한 출력을 사용 하 여 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="eea7c-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="eea7c-113">이 명령은 시간 그레인이 1 분인 website3에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="eea7c-114">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-114">The output is detailed.</span></span>

### <span data-ttu-id="eea7c-115">예제 3: 지정 된 메트릭에 대 한 자세한 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="eea7c-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="eea7c-116">이 명령은 요청 메트릭의 자세한 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="eea7c-117">예제 4: 지정 된 차원 필터를 사용 하 여 지정 된 메트릭의 요약 된 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="eea7c-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
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

<span data-ttu-id="eea7c-118">이 명령은 지정 된 차원 필터 및 집계 유형을 사용 하 여 PageViews 메트릭의 요약 된 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="eea7c-119">변수</span><span class="sxs-lookup"><span data-stu-id="eea7c-119">PARAMETERS</span></span>

### <span data-ttu-id="eea7c-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="eea7c-120">-AggregationType</span></span>
<span data-ttu-id="eea7c-121">쿼리의 집계 유형</span><span class="sxs-lookup"><span data-stu-id="eea7c-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="eea7c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea7c-122">-DefaultProfile</span></span>
<span data-ttu-id="eea7c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea7c-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="eea7c-124">-DetailedOutput</span></span>
<span data-ttu-id="eea7c-125">이 cmdlet에 자세한 출력이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="eea7c-126">기본적으로 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="eea7c-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="eea7c-127">-EndTime</span></span>
<span data-ttu-id="eea7c-128">현지 시간으로 쿼리의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="eea7c-129">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-129">The default is the current time.</span></span>

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

### <span data-ttu-id="eea7c-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="eea7c-130">-MetricFilter</span></span>
<span data-ttu-id="eea7c-131">메트릭을 쿼리할 메트릭 차원 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="eea7c-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="eea7c-132">-MetricName</span></span>
<span data-ttu-id="eea7c-133">메트릭의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="eea7c-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="eea7c-134">-MetricNamespace</span></span>
<span data-ttu-id="eea7c-135">메트릭을 쿼리할 메트릭 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="eea7c-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="eea7c-136">-OrderBy</span></span>
<span data-ttu-id="eea7c-137">결과 정렬에 사용할 집계 및 정렬 방향 (예: sum asc)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="eea7c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea7c-138">-ResourceId</span></span>
<span data-ttu-id="eea7c-139">메트릭의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="eea7c-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="eea7c-140">-ResultType</span></span>
<span data-ttu-id="eea7c-141">반환 될 결과 형식 (메타 데이터 또는 데이터)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="eea7c-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eea7c-142">-StartTime</span></span>
<span data-ttu-id="eea7c-143">현지 시간으로 쿼리의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="eea7c-144">기본값은 현재 현지 시간이 1 시간을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="eea7c-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="eea7c-145">-TimeGrain</span></span>
<span data-ttu-id="eea7c-146">메트릭의 시간 그레인을 hh: mm: ss 형식의 **TimeSpan** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="eea7c-147">-위쪽</span><span class="sxs-lookup"><span data-stu-id="eea7c-147">-Top</span></span>
<span data-ttu-id="eea7c-148">검색할 최대 레코드 수 (기본값: 10)를 지정 하 여 $filter에 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="eea7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea7c-149">CommonParameters</span></span>
<span data-ttu-id="eea7c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea7c-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea7c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea7c-152">입력</span><span class="sxs-lookup"><span data-stu-id="eea7c-152">INPUTS</span></span>

### <span data-ttu-id="eea7c-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eea7c-153">System.String</span></span>

### <span data-ttu-id="eea7c-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="eea7c-154">System.TimeSpan</span></span>

### <span data-ttu-id="eea7c-155">시스템 Null 허용 ' 1 [[AggregationType, Microsoft azure. 0.21.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eea7c-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eea7c-156">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="eea7c-156">System.DateTime</span></span>

### <span data-ttu-id="eea7c-157">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="eea7c-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eea7c-158">시스템 Null 허용 ' 1 [[0.21.0.0]-[[Microsoft. t e.].-., Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eea7c-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eea7c-159">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="eea7c-159">System.String[]</span></span>

### <span data-ttu-id="eea7c-160">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="eea7c-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eea7c-161">출력</span><span class="sxs-lookup"><span data-stu-id="eea7c-161">OUTPUTS</span></span>

### <span data-ttu-id="eea7c-162">PSMetric를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea7c-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="eea7c-163">상속자</span><span class="sxs-lookup"><span data-stu-id="eea7c-163">NOTES</span></span>

<span data-ttu-id="eea7c-164">지원 되는 메트릭에 대 한 자세한 내용은 다음에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="eea7c-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="eea7c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eea7c-165">RELATED LINKS</span></span>

<span data-ttu-id="eea7c-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [새로운 AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="eea7c-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


