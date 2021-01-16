---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331533"
---
# <span data-ttu-id="d2772-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d2772-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="d2772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2772-102">SYNOPSIS</span></span>
<span data-ttu-id="d2772-103">로그 메트릭 트리거 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="d2772-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2772-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2772-105">설명</span><span class="sxs-lookup"><span data-stu-id="d2772-105">DESCRIPTION</span></span>
<span data-ttu-id="d2772-106">로그 메트릭 트리거 형식의 개체를 만들고 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="d2772-107">경고의 메트릭 측정 유형을 상태 표시해야 할 때 사용할 메트릭 쿼리 규칙에 대한 트리거 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="d2772-108">예제</span><span class="sxs-lookup"><span data-stu-id="d2772-108">EXAMPLES</span></span>

### <span data-ttu-id="d2772-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2772-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="d2772-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2772-110">PARAMETERS</span></span>

### <span data-ttu-id="d2772-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2772-111">-DefaultProfile</span></span>
<span data-ttu-id="d2772-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2772-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="d2772-113">-MetricColumn</span></span>
<span data-ttu-id="d2772-114">메트릭 값이 집계되는 열입니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="d2772-115">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-115">The input is not validated.</span></span> <span data-ttu-id="d2772-116">최종적으로 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d2772-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="d2772-117">-MetricTriggerType</span></span>
<span data-ttu-id="d2772-118">메트릭 트리거 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-118">The metric trigger type.</span></span>
<span data-ttu-id="d2772-119">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-119">The input is not validated.</span></span> <span data-ttu-id="d2772-120">최종적으로 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d2772-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="d2772-121">-Threshold</span></span>
<span data-ttu-id="d2772-122">메트릭 임계값: 연속, 합계.</span><span class="sxs-lookup"><span data-stu-id="d2772-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="d2772-123">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-123">The input is not validated.</span></span> <span data-ttu-id="d2772-124">최종적으로 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d2772-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="d2772-125">-ThresholdOperator</span></span>
<span data-ttu-id="d2772-126">메트릭 임계값 연산자: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="d2772-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="d2772-127">입력의 유효성이 검사되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-127">The input is not validated.</span></span> <span data-ttu-id="d2772-128">최종적으로 호출될 때 New-AzScheduledQueryRule 유효성이 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="d2772-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2772-129">CommonParameters</span></span>
<span data-ttu-id="d2772-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2772-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2772-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2772-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2772-132">입력</span><span class="sxs-lookup"><span data-stu-id="d2772-132">INPUTS</span></span>

### <span data-ttu-id="d2772-133">없음</span><span class="sxs-lookup"><span data-stu-id="d2772-133">None</span></span>

## <span data-ttu-id="d2772-134">출력</span><span class="sxs-lookup"><span data-stu-id="d2772-134">OUTPUTS</span></span>

### <span data-ttu-id="d2772-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d2772-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="d2772-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2772-136">NOTES</span></span>

## <span data-ttu-id="d2772-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2772-137">RELATED LINKS</span></span>
