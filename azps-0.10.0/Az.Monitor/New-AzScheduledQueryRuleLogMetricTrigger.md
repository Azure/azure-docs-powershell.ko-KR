---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875744"
---
# <span data-ttu-id="0f514-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0f514-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="0f514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f514-102">SYNOPSIS</span></span>
<span data-ttu-id="0f514-103">Log 메트릭 트리거 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="0f514-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f514-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f514-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f514-105">DESCRIPTION</span></span>
<span data-ttu-id="0f514-106">Log 메트릭 트리거의 형식 개체를 만들며, 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="0f514-107">메트릭 쿼리 규칙에 대 한 트리거 조건으로, 미터법 측정 유형의 경고가 필요한 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="0f514-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0f514-108">EXAMPLES</span></span>

### <span data-ttu-id="0f514-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f514-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="0f514-110">변수</span><span class="sxs-lookup"><span data-stu-id="0f514-110">PARAMETERS</span></span>

### <span data-ttu-id="0f514-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f514-111">-DefaultProfile</span></span>
<span data-ttu-id="0f514-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f514-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="0f514-113">-MetricColumn</span></span>
<span data-ttu-id="0f514-114">메트릭 값이 집계 되는 열</span><span class="sxs-lookup"><span data-stu-id="0f514-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="0f514-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="0f514-115">-MetricTriggerType</span></span>
<span data-ttu-id="0f514-116">메트릭 트리거 유형</span><span class="sxs-lookup"><span data-stu-id="0f514-116">The metric trigger type</span></span>

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

### <span data-ttu-id="0f514-117">-임계값</span><span class="sxs-lookup"><span data-stu-id="0f514-117">-Threshold</span></span>
<span data-ttu-id="0f514-118">메트릭 임계값</span><span class="sxs-lookup"><span data-stu-id="0f514-118">The metric threshold value</span></span>

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

### <span data-ttu-id="0f514-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="0f514-119">-ThresholdOperator</span></span>
<span data-ttu-id="0f514-120">메트릭 임계값 연산자: GreaterThan, LessThan, 같음</span><span class="sxs-lookup"><span data-stu-id="0f514-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="0f514-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f514-121">CommonParameters</span></span>
<span data-ttu-id="0f514-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f514-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f514-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f514-124">입력</span><span class="sxs-lookup"><span data-stu-id="0f514-124">INPUTS</span></span>

### <span data-ttu-id="0f514-125">않아야</span><span class="sxs-lookup"><span data-stu-id="0f514-125">None</span></span>

## <span data-ttu-id="0f514-126">출력</span><span class="sxs-lookup"><span data-stu-id="0f514-126">OUTPUTS</span></span>

### <span data-ttu-id="0f514-127">PSScheduledQueryRuleLogMetricTrigger를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f514-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="0f514-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0f514-128">NOTES</span></span>

## <span data-ttu-id="0f514-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f514-129">RELATED LINKS</span></span>
