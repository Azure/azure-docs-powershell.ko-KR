---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871029"
---
# <span data-ttu-id="53ee0-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="53ee0-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="53ee0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="53ee0-103">Log 메트릭 트리거 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="53ee0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53ee0-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53ee0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="53ee0-106">Log 메트릭 트리거의 형식 개체를 만들며, 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="53ee0-107">메트릭 쿼리 규칙에 대 한 트리거 조건으로, 미터법 측정 유형의 경고가 필요한 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="53ee0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="53ee0-108">EXAMPLES</span></span>

### <span data-ttu-id="53ee0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="53ee0-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="53ee0-110">변수</span><span class="sxs-lookup"><span data-stu-id="53ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="53ee0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ee0-111">-DefaultProfile</span></span>
<span data-ttu-id="53ee0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53ee0-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="53ee0-113">-MetricColumn</span></span>
<span data-ttu-id="53ee0-114">메트릭 값이 집계 되는 열</span><span class="sxs-lookup"><span data-stu-id="53ee0-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="53ee0-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="53ee0-115">-MetricTriggerType</span></span>
<span data-ttu-id="53ee0-116">메트릭 트리거 유형</span><span class="sxs-lookup"><span data-stu-id="53ee0-116">The metric trigger type</span></span>

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

### <span data-ttu-id="53ee0-117">-임계값</span><span class="sxs-lookup"><span data-stu-id="53ee0-117">-Threshold</span></span>
<span data-ttu-id="53ee0-118">메트릭 임계값</span><span class="sxs-lookup"><span data-stu-id="53ee0-118">The metric threshold value</span></span>

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

### <span data-ttu-id="53ee0-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="53ee0-119">-ThresholdOperator</span></span>
<span data-ttu-id="53ee0-120">메트릭 임계값 연산자: GreaterThan, LessThan, 같음</span><span class="sxs-lookup"><span data-stu-id="53ee0-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="53ee0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ee0-121">CommonParameters</span></span>
<span data-ttu-id="53ee0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ee0-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53ee0-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ee0-124">입력</span><span class="sxs-lookup"><span data-stu-id="53ee0-124">INPUTS</span></span>

### <span data-ttu-id="53ee0-125">않아야</span><span class="sxs-lookup"><span data-stu-id="53ee0-125">None</span></span>

## <span data-ttu-id="53ee0-126">출력</span><span class="sxs-lookup"><span data-stu-id="53ee0-126">OUTPUTS</span></span>

### <span data-ttu-id="53ee0-127">PSScheduledQueryRuleLogMetricTrigger를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53ee0-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="53ee0-128">상속자</span><span class="sxs-lookup"><span data-stu-id="53ee0-128">NOTES</span></span>

## <span data-ttu-id="53ee0-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53ee0-129">RELATED LINKS</span></span>
