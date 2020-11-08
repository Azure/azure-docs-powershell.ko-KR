---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218858"
---
# <span data-ttu-id="c2493-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c2493-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="c2493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2493-102">SYNOPSIS</span></span>
<span data-ttu-id="c2493-103">새 메트릭 알림을 만드는 데 사용할 수 있는 로컬 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="c2493-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2493-104">SYNTAX</span></span>

### <span data-ttu-id="c2493-105">StaticThresholdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2493-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2493-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2493-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2493-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2493-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2493-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2493-108">DESCRIPTION</span></span>
<span data-ttu-id="c2493-109">**AzMetricAlertRuleV2Criteria** cmdlet은 새 메트릭 알림 규칙을 만드는 입력 [추가/AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet으로 사용할 로컬 메트릭 기준 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="c2493-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2493-110">EXAMPLES</span></span>

### <span data-ttu-id="c2493-111">예제 1: 간단한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="c2493-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="c2493-112">이 명령은 메트릭 알림 규칙에 사용할 수 있는 간단한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="c2493-113">예제 2: 동적 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="c2493-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="c2493-114">이 명령은 메트릭 알림 규칙에 사용할 수 있는 동적 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="c2493-115">예제 3: 더 복잡 한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="c2493-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="c2493-116">이 명령 집합은 차원 선택을 포함 하는 보다 복잡 한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="c2493-117">예제 4: webtest 사용 가능 기준 만들기</span><span class="sxs-lookup"><span data-stu-id="c2493-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="c2493-118">이 명령은 메트릭 알림 규칙에 사용할 수 있는 webtest 사용 가능 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="c2493-119">변수</span><span class="sxs-lookup"><span data-stu-id="c2493-119">PARAMETERS</span></span>

### <span data-ttu-id="c2493-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="c2493-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="c2493-121">Application Insights 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2493-122">-DefaultProfile</span></span>
<span data-ttu-id="c2493-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2493-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c2493-124">-DimensionSelection</span></span>
<span data-ttu-id="c2493-125">차원 조건 목록</span><span class="sxs-lookup"><span data-stu-id="c2493-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="c2493-126">-DynamicThreshold</span></span>
<span data-ttu-id="c2493-127">동적 임계값 유형을 사용 하기 위한 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2493-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="c2493-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="c2493-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="c2493-129">총 검사 된 지점 수</span><span class="sxs-lookup"><span data-stu-id="c2493-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="c2493-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="c2493-130">-FailedLocationCount</span></span>
<span data-ttu-id="c2493-131">경고를 발생 시킬 최소 실패 한 위치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="c2493-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="c2493-133">IgnoreDataBefore 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2493-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="c2493-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c2493-134">-MetricName</span></span>
<span data-ttu-id="c2493-135">규칙에 대 한 메트릭 이름</span><span class="sxs-lookup"><span data-stu-id="c2493-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c2493-136">-MetricNamespace</span></span>
<span data-ttu-id="c2493-137">메트릭의 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c2493-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-138">-연산자</span><span class="sxs-lookup"><span data-stu-id="c2493-138">-Operator</span></span>
<span data-ttu-id="c2493-139">규칙 조건 연산자</span><span class="sxs-lookup"><span data-stu-id="c2493-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="c2493-140">-SkipMetricValidation</span></span>
<span data-ttu-id="c2493-141">메트릭 유효성 검사를 건너뛰도록 하 여 아직 내보내지 않은 사용자 지정 메트릭에 대해 알림 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-142">-임계값</span><span class="sxs-lookup"><span data-stu-id="c2493-142">-Threshold</span></span>
<span data-ttu-id="c2493-143">규칙 조건에 대 한 임계값</span><span class="sxs-lookup"><span data-stu-id="c2493-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="c2493-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="c2493-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="c2493-145">규칙 조건에 대 한 민감도</span><span class="sxs-lookup"><span data-stu-id="c2493-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="c2493-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="c2493-146">-TimeAggregation</span></span>
<span data-ttu-id="c2493-147">창 간격에서 여러 메트릭 값을 롤 포워드 하는 데 사용 되는 집계 연산</span><span class="sxs-lookup"><span data-stu-id="c2493-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="c2493-148">-ViolationCount</span></span>
<span data-ttu-id="c2493-149">경고가 발생 하는 데 필요한 선택한 lookback time 창 내에 필요한 최소 위반 횟수</span><span class="sxs-lookup"><span data-stu-id="c2493-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="c2493-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="c2493-150">-WebTest</span></span>
<span data-ttu-id="c2493-151">가용성 조건 유형을 사용 하기 위한 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2493-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="c2493-152">-WebTestId</span></span>
<span data-ttu-id="c2493-153">Application Insights 웹 테스트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2493-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2493-154">CommonParameters</span></span>
<span data-ttu-id="c2493-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2493-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2493-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2493-157">입력</span><span class="sxs-lookup"><span data-stu-id="c2493-157">INPUTS</span></span>

### <span data-ttu-id="c2493-158">PSMetricDimension [] (으)로</span><span class="sxs-lookup"><span data-stu-id="c2493-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="c2493-159">출력</span><span class="sxs-lookup"><span data-stu-id="c2493-159">OUTPUTS</span></span>

### <span data-ttu-id="c2493-160">IPSMultiMetricCriteria를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2493-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="c2493-161">상속자</span><span class="sxs-lookup"><span data-stu-id="c2493-161">NOTES</span></span>

## <span data-ttu-id="c2493-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2493-162">RELATED LINKS</span></span>
