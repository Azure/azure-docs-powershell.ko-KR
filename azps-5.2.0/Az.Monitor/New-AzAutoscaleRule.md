---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350882"
---
# <span data-ttu-id="c871d-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c871d-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="c871d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c871d-102">SYNOPSIS</span></span>
<span data-ttu-id="c871d-103">자동 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="c871d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c871d-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c871d-105">설명</span><span class="sxs-lookup"><span data-stu-id="c871d-105">DESCRIPTION</span></span>
<span data-ttu-id="c871d-106">**New-AzAutoscaleRule** cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="c871d-107">예제</span><span class="sxs-lookup"><span data-stu-id="c871d-107">EXAMPLES</span></span>

### <span data-ttu-id="c871d-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="c871d-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c871d-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-109">This command creates a rule.</span></span>

### <span data-ttu-id="c871d-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="c871d-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c871d-111">첫 번째 명령은 Requests 메트릭에 대한 규칙을 만든 다음 $Rule 1 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="c871d-112">두 번째 명령은 요청 메트릭에 대한 두 번째 규칙을 만든 다음 $Rule 2 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="c871d-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="c871d-113">Example 3</span></span>

<span data-ttu-id="c871d-114">자동 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="c871d-115">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="c871d-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="c871d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c871d-116">PARAMETERS</span></span>

### <span data-ttu-id="c871d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c871d-117">-DefaultProfile</span></span>
<span data-ttu-id="c871d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c871d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c871d-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c871d-119">-MetricName</span></span>
<span data-ttu-id="c871d-120">메트릭의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-120">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="c871d-121">-MetricResourceId</span></span>
<span data-ttu-id="c871d-122">메트릭 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-122">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="c871d-123">-MetricStatistic</span></span>
<span data-ttu-id="c871d-124">메트릭 통계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="c871d-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c871d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c871d-126">평균</span><span class="sxs-lookup"><span data-stu-id="c871d-126">Average</span></span>
- <span data-ttu-id="c871d-127">최소</span><span class="sxs-lookup"><span data-stu-id="c871d-127">Min</span></span>
- <span data-ttu-id="c871d-128">최대</span><span class="sxs-lookup"><span data-stu-id="c871d-128">Max</span></span>
- <span data-ttu-id="c871d-129">합계</span><span class="sxs-lookup"><span data-stu-id="c871d-129">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="c871d-130">-Operator</span></span>
<span data-ttu-id="c871d-131">연산자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-131">Specifies the operator.</span></span>
<span data-ttu-id="c871d-132">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c871d-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c871d-133">같음</span><span class="sxs-lookup"><span data-stu-id="c871d-133">Equals</span></span>
- <span data-ttu-id="c871d-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="c871d-134">NotEquals</span></span>
- <span data-ttu-id="c871d-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="c871d-135">GreaterThan</span></span>
- <span data-ttu-id="c871d-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c871d-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="c871d-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="c871d-137">LessThan</span></span>
- <span data-ttu-id="c871d-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c871d-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="c871d-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="c871d-140">자동 조정 작업 대기 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-140">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="c871d-141">-ScaleActionDirection</span></span>
<span data-ttu-id="c871d-142">크기 조정 작업 방향을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="c871d-143">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c871d-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c871d-144">없음</span><span class="sxs-lookup"><span data-stu-id="c871d-144">None</span></span>
- <span data-ttu-id="c871d-145">증가</span><span class="sxs-lookup"><span data-stu-id="c871d-145">Increase</span></span>
- <span data-ttu-id="c871d-146">감소</span><span class="sxs-lookup"><span data-stu-id="c871d-146">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="c871d-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="c871d-148">크기 조정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-148">Specifies the scale type.</span></span>
<span data-ttu-id="c871d-149">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c871d-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c871d-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="c871d-150">ChangeSize</span></span>
- <span data-ttu-id="c871d-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="c871d-151">ChangeCount</span></span>
- <span data-ttu-id="c871d-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="c871d-152">PercentChangeCount</span></span>
- <span data-ttu-id="c871d-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="c871d-153">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="c871d-154">-ScaleActionValue</span></span>
<span data-ttu-id="c871d-155">작업 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-155">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-156">-Threshold</span><span class="sxs-lookup"><span data-stu-id="c871d-156">-Threshold</span></span>
<span data-ttu-id="c871d-157">메트릭 값의 임계값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-157">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="c871d-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="c871d-159">시간 집계 연산자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="c871d-160">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c871d-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c871d-161">평균</span><span class="sxs-lookup"><span data-stu-id="c871d-161">Average</span></span>
- <span data-ttu-id="c871d-162">최소</span><span class="sxs-lookup"><span data-stu-id="c871d-162">Minimum</span></span>
- <span data-ttu-id="c871d-163">최대</span><span class="sxs-lookup"><span data-stu-id="c871d-163">Maximum</span></span>
- <span data-ttu-id="c871d-164">Last</span><span class="sxs-lookup"><span data-stu-id="c871d-164">Last</span></span>
- <span data-ttu-id="c871d-165">합계, 개수</span><span class="sxs-lookup"><span data-stu-id="c871d-165">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c871d-166">-TimeGrain</span></span>
<span data-ttu-id="c871d-167">시간 그레인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-167">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="c871d-168">-TimeWindow</span></span>
<span data-ttu-id="c871d-169">기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-169">Specifies the time window.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c871d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c871d-170">CommonParameters</span></span>
<span data-ttu-id="c871d-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c871d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c871d-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c871d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c871d-173">입력</span><span class="sxs-lookup"><span data-stu-id="c871d-173">INPUTS</span></span>

### <span data-ttu-id="c871d-174">System.String</span><span class="sxs-lookup"><span data-stu-id="c871d-174">System.String</span></span>

### <span data-ttu-id="c871d-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="c871d-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="c871d-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="c871d-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="c871d-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="c871d-177">System.Double</span></span>

### <span data-ttu-id="c871d-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="c871d-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="c871d-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c871d-179">System.TimeSpan</span></span>

### <span data-ttu-id="c871d-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="c871d-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="c871d-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="c871d-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="c871d-182">출력</span><span class="sxs-lookup"><span data-stu-id="c871d-182">OUTPUTS</span></span>

### <span data-ttu-id="c871d-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="c871d-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="c871d-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c871d-184">NOTES</span></span>

## <span data-ttu-id="c871d-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c871d-185">RELATED LINKS</span></span>

[<span data-ttu-id="c871d-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c871d-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="c871d-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="c871d-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="c871d-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c871d-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="c871d-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c871d-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="c871d-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c871d-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


