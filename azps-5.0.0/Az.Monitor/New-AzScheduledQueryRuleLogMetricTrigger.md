---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217290"
---
# <span data-ttu-id="b7167-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b7167-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="b7167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7167-102">SYNOPSIS</span></span>
<span data-ttu-id="b7167-103">Log 메트릭 트리거의 형식 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="b7167-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7167-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7167-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7167-105">DESCRIPTION</span></span>
<span data-ttu-id="b7167-106">Log 메트릭 트리거의 형식 개체를 만들며, 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="b7167-107">메트릭 쿼리 규칙에 대 한 트리거 조건으로, 미터법 측정 유형의 경고가 필요한 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="b7167-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b7167-108">EXAMPLES</span></span>

### <span data-ttu-id="b7167-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7167-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="b7167-110">변수</span><span class="sxs-lookup"><span data-stu-id="b7167-110">PARAMETERS</span></span>

### <span data-ttu-id="b7167-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7167-111">-DefaultProfile</span></span>
<span data-ttu-id="b7167-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7167-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="b7167-113">-MetricColumn</span></span>
<span data-ttu-id="b7167-114">메트릭 값이 집계 되는 열입니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="b7167-115">입력의 유효성이 확인 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-115">The input is not validated.</span></span> <span data-ttu-id="b7167-116">New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="b7167-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="b7167-117">-MetricTriggerType</span></span>
<span data-ttu-id="b7167-118">메트릭 트리거 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-118">The metric trigger type.</span></span>
<span data-ttu-id="b7167-119">입력의 유효성이 확인 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-119">The input is not validated.</span></span> <span data-ttu-id="b7167-120">New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="b7167-121">-임계값</span><span class="sxs-lookup"><span data-stu-id="b7167-121">-Threshold</span></span>
<span data-ttu-id="b7167-122">메트릭 임계값 (연속, 합계)입니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="b7167-123">입력의 유효성이 확인 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-123">The input is not validated.</span></span> <span data-ttu-id="b7167-124">New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="b7167-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="b7167-125">-ThresholdOperator</span></span>
<span data-ttu-id="b7167-126">메트릭 임계값 연산자: GreaterThan, LessThan, 같음.</span><span class="sxs-lookup"><span data-stu-id="b7167-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="b7167-127">입력의 유효성이 확인 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-127">The input is not validated.</span></span> <span data-ttu-id="b7167-128">New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="b7167-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7167-129">CommonParameters</span></span>
<span data-ttu-id="b7167-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7167-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7167-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7167-132">입력</span><span class="sxs-lookup"><span data-stu-id="b7167-132">INPUTS</span></span>

### <span data-ttu-id="b7167-133">않아야</span><span class="sxs-lookup"><span data-stu-id="b7167-133">None</span></span>

## <span data-ttu-id="b7167-134">출력</span><span class="sxs-lookup"><span data-stu-id="b7167-134">OUTPUTS</span></span>

### <span data-ttu-id="b7167-135">PSScheduledQueryRuleLogMetricTrigger를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7167-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="b7167-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b7167-136">NOTES</span></span>

## <span data-ttu-id="b7167-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7167-137">RELATED LINKS</span></span>
