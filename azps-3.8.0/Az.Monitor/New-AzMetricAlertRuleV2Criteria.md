---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033871"
---
# <span data-ttu-id="0d8ee-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0d8ee-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="0d8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8ee-103">새 메트릭 알림을 만드는 데 사용할 수 있는 로컬 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="0d8ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d8ee-104">SYNTAX</span></span>

### <span data-ttu-id="0d8ee-105">StaticThresholdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d8ee-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d8ee-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8ee-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d8ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0d8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="0d8ee-108">**AzMetricAlertRuleV2Criteria** cmdlet은 새 메트릭 알림 규칙을 만드는 입력 Add-AzMetricAlertRuleV2 cmdlet으로 사용할 로컬 메트릭 기준 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="0d8ee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0d8ee-109">EXAMPLES</span></span>

### <span data-ttu-id="0d8ee-110">예제 1: 간단한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="0d8ee-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="0d8ee-111">이 명령은 메트릭 알림 규칙에 사용할 수 있는 간단한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="0d8ee-112">예제 2: 동적 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="0d8ee-112">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="0d8ee-113">이 명령은 메트릭 알림 규칙에 사용할 수 있는 동적 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="0d8ee-114">예제 3: 더 복잡 한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="0d8ee-114">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="0d8ee-115">이 명령 집합은 차원 선택을 포함 하는 보다 복잡 한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="0d8ee-116">변수</span><span class="sxs-lookup"><span data-stu-id="0d8ee-116">PARAMETERS</span></span>

### <span data-ttu-id="0d8ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8ee-117">-DefaultProfile</span></span>
<span data-ttu-id="0d8ee-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d8ee-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0d8ee-119">-DimensionSelection</span></span>
<span data-ttu-id="0d8ee-120">차원 조건 목록</span><span class="sxs-lookup"><span data-stu-id="0d8ee-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="0d8ee-121">-DynamicThreshold</span></span>
<span data-ttu-id="0d8ee-122">동적 임계값 유형을 사용 하기 위한 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d8ee-122">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="0d8ee-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="0d8ee-124">총 검사 된 지점 수</span><span class="sxs-lookup"><span data-stu-id="0d8ee-124">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="0d8ee-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="0d8ee-126">IgnoreDataBefore 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d8ee-126">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="0d8ee-127">-MetricName</span></span>
<span data-ttu-id="0d8ee-128">규칙에 대 한 메트릭 이름</span><span class="sxs-lookup"><span data-stu-id="0d8ee-128">The metric name for rule</span></span>

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

### <span data-ttu-id="0d8ee-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0d8ee-129">-MetricNamespace</span></span>
<span data-ttu-id="0d8ee-130">메트릭의 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="0d8ee-130">The Namespace of the metric</span></span>

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

### <span data-ttu-id="0d8ee-131">-연산자</span><span class="sxs-lookup"><span data-stu-id="0d8ee-131">-Operator</span></span>
<span data-ttu-id="0d8ee-132">규칙 조건 연산자</span><span class="sxs-lookup"><span data-stu-id="0d8ee-132">The rule condition operator</span></span>

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

### <span data-ttu-id="0d8ee-133">-임계값</span><span class="sxs-lookup"><span data-stu-id="0d8ee-133">-Threshold</span></span>
<span data-ttu-id="0d8ee-134">규칙 조건에 대 한 임계값</span><span class="sxs-lookup"><span data-stu-id="0d8ee-134">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="0d8ee-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="0d8ee-136">규칙 조건에 대 한 민감도</span><span class="sxs-lookup"><span data-stu-id="0d8ee-136">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="0d8ee-137">-TimeAggregation</span></span>
<span data-ttu-id="0d8ee-138">창 간격에서 여러 메트릭 값을 롤 포워드 하는 데 사용 되는 집계 연산</span><span class="sxs-lookup"><span data-stu-id="0d8ee-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="0d8ee-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="0d8ee-139">-ViolationCount</span></span>
<span data-ttu-id="0d8ee-140">경고가 발생 하는 데 필요한 선택한 lookback time 창 내에 필요한 최소 위반 횟수</span><span class="sxs-lookup"><span data-stu-id="0d8ee-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8ee-141">CommonParameters</span></span>
<span data-ttu-id="0d8ee-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8ee-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8ee-144">입력</span><span class="sxs-lookup"><span data-stu-id="0d8ee-144">INPUTS</span></span>

### <span data-ttu-id="0d8ee-145">PSMetricDimension [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0d8ee-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="0d8ee-146">출력</span><span class="sxs-lookup"><span data-stu-id="0d8ee-146">OUTPUTS</span></span>

### <span data-ttu-id="0d8ee-147">IPSMultiMetricCriteria를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d8ee-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="0d8ee-148">상속자</span><span class="sxs-lookup"><span data-stu-id="0d8ee-148">NOTES</span></span>

## <span data-ttu-id="0d8ee-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d8ee-149">RELATED LINKS</span></span>
