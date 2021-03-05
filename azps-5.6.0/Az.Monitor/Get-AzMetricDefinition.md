---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 3e1038fc44acc1e3834ee10a1fd08bb49c35cd82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979936"
---
# <span data-ttu-id="5d3f5-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5d3f5-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="5d3f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3f5-103">메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-103">Gets metric definitions.</span></span>

## <span data-ttu-id="5d3f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d3f5-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d3f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="5d3f5-105">DESCRIPTION</span></span>
<span data-ttu-id="5d3f5-106">**Get-AzMetricDefinition** cmdlet은 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="5d3f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="5d3f5-107">EXAMPLES</span></span>

### <span data-ttu-id="5d3f5-108">예제 1: 리소스에 대한 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="5d3f5-109">이 명령은 지정된 리소스에 대한 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="5d3f5-110">예제 2: 자세한 출력을 사용하여 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="5d3f5-111">이 명령은 website2에 대한 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="5d3f5-112">출력이 자세히 설명됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-112">The output is detailed.</span></span>

### <span data-ttu-id="5d3f5-113">예제 3: 이름에 따라 메트릭 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="5d3f5-114">이 명령은 BytesSent 및 CpuTime 메트릭에 대한 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="5d3f5-115">출력이 자세히 설명됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-115">The output is detailed.</span></span>

## <span data-ttu-id="5d3f5-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d3f5-116">PARAMETERS</span></span>

### <span data-ttu-id="5d3f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f5-117">-DefaultProfile</span></span>
<span data-ttu-id="5d3f5-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d3f5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d3f5-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5d3f5-119">-DetailedOutput</span></span>
<span data-ttu-id="5d3f5-120">이 작업에 자세한 출력이 포함되어 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="5d3f5-121">이 매개 변수를 지정하지 않으면 출력이 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3f5-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="5d3f5-122">-MetricName</span></span>
<span data-ttu-id="5d3f5-123">메트릭의 이름 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3f5-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="5d3f5-124">-MetricNamespace</span></span>
<span data-ttu-id="5d3f5-125">메트릭 정의를 쿼리하기 위해 메트릭 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3f5-126">-ResourceId</span></span>
<span data-ttu-id="5d3f5-127">리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="5d3f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3f5-128">CommonParameters</span></span>
<span data-ttu-id="5d3f5-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3f5-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d3f5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3f5-131">입력</span><span class="sxs-lookup"><span data-stu-id="5d3f5-131">INPUTS</span></span>

### <span data-ttu-id="5d3f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5d3f5-132">System.String</span></span>

### <span data-ttu-id="5d3f5-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5d3f5-133">System.String[]</span></span>

## <span data-ttu-id="5d3f5-134">출력</span><span class="sxs-lookup"><span data-stu-id="5d3f5-134">OUTPUTS</span></span>

### <span data-ttu-id="5d3f5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5d3f5-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="5d3f5-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f5-136">NOTES</span></span>

<span data-ttu-id="5d3f5-137">지원되는 메트릭에 대한 자세한 내용은 다음에서 찾을 수 있습니다. https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="5d3f5-137">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="5d3f5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d3f5-138">RELATED LINKS</span></span>

<span data-ttu-id="5d3f5-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="5d3f5-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


