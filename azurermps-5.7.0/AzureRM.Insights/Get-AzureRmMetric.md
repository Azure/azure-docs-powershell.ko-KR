---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702264"
---
# <span data-ttu-id="b9d23-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="b9d23-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="b9d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9d23-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d23-103">리소스의 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9d23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9d23-104">SYNTAX</span></span>

### <span data-ttu-id="b9d23-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="b9d23-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9d23-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="b9d23-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9d23-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9d23-107">DESCRIPTION</span></span>
<span data-ttu-id="b9d23-108">**AzureRmMetric** cmdlet은 지정 된 리소스에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="b9d23-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b9d23-109">EXAMPLES</span></span>

### <span data-ttu-id="b9d23-110">예제 1: 요약 된 출력이 있는 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9d23-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="b9d23-111">이 명령은 시간 그레인이 1 분인 website3에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="b9d23-112">예제 2: 자세한 출력을 사용 하 여 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9d23-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="b9d23-113">이 명령은 시간 그레인이 1 분인 website3에 대 한 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="b9d23-114">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-114">The output is detailed.</span></span>

### <span data-ttu-id="b9d23-115">예제 3: 지정 된 메트릭에 대 한 자세한 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9d23-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="b9d23-116">이 명령은 요청 메트릭의 자세한 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="b9d23-117">변수</span><span class="sxs-lookup"><span data-stu-id="b9d23-117">PARAMETERS</span></span>

### <span data-ttu-id="b9d23-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="b9d23-118">-AggregationType</span></span>
<span data-ttu-id="b9d23-119">쿼리의 집계 유형</span><span class="sxs-lookup"><span data-stu-id="b9d23-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d23-120">-DefaultProfile</span></span>
<span data-ttu-id="b9d23-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b9d23-122">-DetailedOutput</span></span>
<span data-ttu-id="b9d23-123">이 cmdlet에 자세한 출력이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="b9d23-124">기본적으로 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b9d23-125">-EndTime</span></span>
<span data-ttu-id="b9d23-126">현지 시간으로 쿼리의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="b9d23-127">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b9d23-128">-MetricName</span></span>
<span data-ttu-id="b9d23-129">메트릭의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9d23-130">-ResourceId</span></span>
<span data-ttu-id="b9d23-131">메트릭의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b9d23-132">-StartTime</span></span>
<span data-ttu-id="b9d23-133">현지 시간으로 쿼리의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="b9d23-134">기본값은 현재 현지 시간이 1 시간을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="b9d23-135">-TimeGrain</span></span>
<span data-ttu-id="b9d23-136">메트릭의 시간 그레인을 hh: mm: ss 형식의 **TimeSpan** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d23-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d23-137">CommonParameters</span></span>
<span data-ttu-id="b9d23-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d23-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9d23-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d23-140">입력</span><span class="sxs-lookup"><span data-stu-id="b9d23-140">INPUTS</span></span>

### <span data-ttu-id="b9d23-141">않아야</span><span class="sxs-lookup"><span data-stu-id="b9d23-141">None</span></span>
<span data-ttu-id="b9d23-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9d23-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9d23-143">출력</span><span class="sxs-lookup"><span data-stu-id="b9d23-143">OUTPUTS</span></span>

### <span data-ttu-id="b9d23-144">PSMetric [] (으)로</span><span class="sxs-lookup"><span data-stu-id="b9d23-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="b9d23-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b9d23-145">NOTES</span></span>

## <span data-ttu-id="b9d23-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9d23-146">RELATED LINKS</span></span>

[<span data-ttu-id="b9d23-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b9d23-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


