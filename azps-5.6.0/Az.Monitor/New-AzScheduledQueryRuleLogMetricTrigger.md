---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978427"
---
# <span data-ttu-id="e343a-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e343a-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="e343a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e343a-102">SYNOPSIS</span></span>
<span data-ttu-id="e343a-103">Log Metric Trigger 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="e343a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e343a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e343a-105">설명</span><span class="sxs-lookup"><span data-stu-id="e343a-105">DESCRIPTION</span></span>
<span data-ttu-id="e343a-106">Log Metric Trigger 형식의 개체를 만들고 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="e343a-107">메트릭 측정 유형 경고를 상태해야 할 때 사용할 메트릭 쿼리 규칙의 트리거 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="e343a-108">예제</span><span class="sxs-lookup"><span data-stu-id="e343a-108">EXAMPLES</span></span>

### <span data-ttu-id="e343a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e343a-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="e343a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e343a-110">PARAMETERS</span></span>

### <span data-ttu-id="e343a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e343a-111">-DefaultProfile</span></span>
<span data-ttu-id="e343a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e343a-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="e343a-113">-MetricColumn</span></span>
<span data-ttu-id="e343a-114">메트릭 값이 집계되는 열입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="e343a-115">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-115">The input is not validated.</span></span> <span data-ttu-id="e343a-116">먼저 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e343a-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="e343a-117">-MetricTriggerType</span></span>
<span data-ttu-id="e343a-118">메트릭 트리거 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-118">The metric trigger type.</span></span>
<span data-ttu-id="e343a-119">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-119">The input is not validated.</span></span> <span data-ttu-id="e343a-120">먼저 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e343a-121">-임계값</span><span class="sxs-lookup"><span data-stu-id="e343a-121">-Threshold</span></span>
<span data-ttu-id="e343a-122">메트릭 임계값: 연속, 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="e343a-123">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-123">The input is not validated.</span></span> <span data-ttu-id="e343a-124">먼저 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e343a-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="e343a-125">-ThresholdOperator</span></span>
<span data-ttu-id="e343a-126">메트릭 임계값 연산자: GreaterThan, LessThan, Equal입니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="e343a-127">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-127">The input is not validated.</span></span> <span data-ttu-id="e343a-128">먼저 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e343a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e343a-129">CommonParameters</span></span>
<span data-ttu-id="e343a-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e343a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e343a-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e343a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e343a-132">입력</span><span class="sxs-lookup"><span data-stu-id="e343a-132">INPUTS</span></span>

### <span data-ttu-id="e343a-133">없음</span><span class="sxs-lookup"><span data-stu-id="e343a-133">None</span></span>

## <span data-ttu-id="e343a-134">출력</span><span class="sxs-lookup"><span data-stu-id="e343a-134">OUTPUTS</span></span>

### <span data-ttu-id="e343a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e343a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="e343a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e343a-136">NOTES</span></span>

## <span data-ttu-id="e343a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e343a-137">RELATED LINKS</span></span>
