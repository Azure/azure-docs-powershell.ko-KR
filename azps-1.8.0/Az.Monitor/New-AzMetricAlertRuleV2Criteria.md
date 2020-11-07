---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867262"
---
# <span data-ttu-id="b1ea2-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b1ea2-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="b1ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ea2-103">새 메트릭 알림을 만드는 데 사용할 수 있는 로컬 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="b1ea2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1ea2-104">SYNTAX</span></span>

### <span data-ttu-id="b1ea2-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1ea2-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1ea2-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1ea2-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1ea2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b1ea2-107">DESCRIPTION</span></span>
<span data-ttu-id="b1ea2-108">**AzMetricAlertRuleV2Criteria** cmdlet은 새 메트릭 알림 규칙을 만드는 입력 Add-AzMetricAlertRuleV2 cmdlet으로 사용할 로컬 메트릭 기준 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="b1ea2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b1ea2-109">EXAMPLES</span></span>

### <span data-ttu-id="b1ea2-110">예제 1: 간단한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="b1ea2-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="b1ea2-111">이 명령은 메트릭 알림 규칙에 사용할 수 있는 간단한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="b1ea2-112">예제 2: 더 복잡 한 메트릭 알림 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="b1ea2-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="b1ea2-113">이 명령 집합은 차원 선택을 포함 하는 보다 복잡 한 메트릭 알림 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="b1ea2-114">변수</span><span class="sxs-lookup"><span data-stu-id="b1ea2-114">PARAMETERS</span></span>

### <span data-ttu-id="b1ea2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ea2-115">-DefaultProfile</span></span>
<span data-ttu-id="b1ea2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b1ea2-117">-DimensionSelection</span></span>
<span data-ttu-id="b1ea2-118">차원 조건 목록</span><span class="sxs-lookup"><span data-stu-id="b1ea2-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="b1ea2-119">-DynamicThreshold</span></span>
<span data-ttu-id="b1ea2-120">규칙 조건에 대 한 동적 임계값</span><span class="sxs-lookup"><span data-stu-id="b1ea2-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="b1ea2-121">-FailingPeriod</span></span>
<span data-ttu-id="b1ea2-122">규칙 조건에 대 한 실패 기간</span><span class="sxs-lookup"><span data-stu-id="b1ea2-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="b1ea2-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="b1ea2-124">IgnoreDataBefore 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b1ea2-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b1ea2-125">-MetricName</span></span>
<span data-ttu-id="b1ea2-126">규칙에 대 한 메트릭 이름</span><span class="sxs-lookup"><span data-stu-id="b1ea2-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="b1ea2-127">-MetricNamespace</span></span>
<span data-ttu-id="b1ea2-128">메트릭의 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="b1ea2-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-129">-연산자</span><span class="sxs-lookup"><span data-stu-id="b1ea2-129">-Operator</span></span>
<span data-ttu-id="b1ea2-130">규칙 조건 연산자</span><span class="sxs-lookup"><span data-stu-id="b1ea2-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-131">민감도</span><span class="sxs-lookup"><span data-stu-id="b1ea2-131">-Sensitivity</span></span>
<span data-ttu-id="b1ea2-132">규칙 조건에 대 한 민감도</span><span class="sxs-lookup"><span data-stu-id="b1ea2-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-133">-임계값</span><span class="sxs-lookup"><span data-stu-id="b1ea2-133">-Threshold</span></span>
<span data-ttu-id="b1ea2-134">규칙 조건에 대 한 임계값</span><span class="sxs-lookup"><span data-stu-id="b1ea2-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="b1ea2-135">-TimeAggregation</span></span>
<span data-ttu-id="b1ea2-136">창 간격에서 여러 메트릭 값을 롤 포워드 하는 데 사용 되는 집계 연산</span><span class="sxs-lookup"><span data-stu-id="b1ea2-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="b1ea2-137">-TotalPeriod</span></span>
<span data-ttu-id="b1ea2-138">규칙 조건에 대 한 총 기간</span><span class="sxs-lookup"><span data-stu-id="b1ea2-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ea2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ea2-139">CommonParameters</span></span>
<span data-ttu-id="b1ea2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1ea2-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1ea2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ea2-142">입력</span><span class="sxs-lookup"><span data-stu-id="b1ea2-142">INPUTS</span></span>

### <span data-ttu-id="b1ea2-143">PSMetricDimension [] (으)로</span><span class="sxs-lookup"><span data-stu-id="b1ea2-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="b1ea2-144">출력</span><span class="sxs-lookup"><span data-stu-id="b1ea2-144">OUTPUTS</span></span>

### <span data-ttu-id="b1ea2-145">PSMetricCriteria를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ea2-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="b1ea2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b1ea2-146">NOTES</span></span>

## <span data-ttu-id="b1ea2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1ea2-147">RELATED LINKS</span></span>
