---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: ed69dc291b230dc634fe9eeaf19e783c0fb8fbe6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034285"
---
# <span data-ttu-id="2208c-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="2208c-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="2208c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2208c-102">SYNOPSIS</span></span>
<span data-ttu-id="2208c-103">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="2208c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2208c-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2208c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2208c-105">DESCRIPTION</span></span>
<span data-ttu-id="2208c-106">**AzAutoscaleRule** Cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="2208c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2208c-107">EXAMPLES</span></span>

### <span data-ttu-id="2208c-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2208c-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="2208c-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-109">This command creates a rule.</span></span>

### <span data-ttu-id="2208c-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2208c-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="2208c-111">첫 번째 명령은 요청 메트릭에 대 한 규칙을 만든 다음이를 $Rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="2208c-112">두 번째 명령은 요청 메트릭에 대 한 두 번째 규칙을 만든 다음이를 $Rule 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="2208c-113">변수</span><span class="sxs-lookup"><span data-stu-id="2208c-113">PARAMETERS</span></span>

### <span data-ttu-id="2208c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2208c-114">-DefaultProfile</span></span>
<span data-ttu-id="2208c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2208c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2208c-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2208c-116">-MetricName</span></span>
<span data-ttu-id="2208c-117">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="2208c-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="2208c-118">-MetricResourceId</span></span>
<span data-ttu-id="2208c-119">메트릭 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="2208c-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="2208c-120">-MetricStatistic</span></span>
<span data-ttu-id="2208c-121">메트릭 통계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="2208c-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2208c-123">보통</span><span class="sxs-lookup"><span data-stu-id="2208c-123">Average</span></span>
- <span data-ttu-id="2208c-124">Occurs</span><span class="sxs-lookup"><span data-stu-id="2208c-124">Min</span></span>
- <span data-ttu-id="2208c-125">Max</span><span class="sxs-lookup"><span data-stu-id="2208c-125">Max</span></span>
- <span data-ttu-id="2208c-126">총계</span><span class="sxs-lookup"><span data-stu-id="2208c-126">Sum</span></span>

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

### <span data-ttu-id="2208c-127">-연산자</span><span class="sxs-lookup"><span data-stu-id="2208c-127">-Operator</span></span>
<span data-ttu-id="2208c-128">연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-128">Specifies the operator.</span></span>
<span data-ttu-id="2208c-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2208c-130">본인이</span><span class="sxs-lookup"><span data-stu-id="2208c-130">Equals</span></span>
- <span data-ttu-id="2208c-131">참고 $ Als</span><span class="sxs-lookup"><span data-stu-id="2208c-131">NotEquals</span></span>
- <span data-ttu-id="2208c-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2208c-132">GreaterThan</span></span>
- <span data-ttu-id="2208c-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2208c-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="2208c-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="2208c-134">LessThan</span></span>
- <span data-ttu-id="2208c-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2208c-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="2208c-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="2208c-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="2208c-137">자동 크기 조정 작업 쿨 다운 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="2208c-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="2208c-138">-ScaleActionDirection</span></span>
<span data-ttu-id="2208c-139">크기 조정 작업 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="2208c-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2208c-141">않아야</span><span class="sxs-lookup"><span data-stu-id="2208c-141">None</span></span>
- <span data-ttu-id="2208c-142">늘리거나</span><span class="sxs-lookup"><span data-stu-id="2208c-142">Increase</span></span>
- <span data-ttu-id="2208c-143">낮출</span><span class="sxs-lookup"><span data-stu-id="2208c-143">Decrease</span></span>

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

### <span data-ttu-id="2208c-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="2208c-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="2208c-145">눈금 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-145">Specifies the scale type.</span></span>
<span data-ttu-id="2208c-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2208c-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="2208c-147">ChangeSize</span></span>
- <span data-ttu-id="2208c-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="2208c-148">ChangeCount</span></span>
- <span data-ttu-id="2208c-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="2208c-149">PercentChangeCount</span></span>
- <span data-ttu-id="2208c-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="2208c-150">ExactCount</span></span>

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

### <span data-ttu-id="2208c-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="2208c-151">-ScaleActionValue</span></span>
<span data-ttu-id="2208c-152">작업 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="2208c-153">-임계값</span><span class="sxs-lookup"><span data-stu-id="2208c-153">-Threshold</span></span>
<span data-ttu-id="2208c-154">메트릭 값의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="2208c-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="2208c-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="2208c-156">시간 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="2208c-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2208c-158">보통</span><span class="sxs-lookup"><span data-stu-id="2208c-158">Average</span></span>
- <span data-ttu-id="2208c-159">솟</span><span class="sxs-lookup"><span data-stu-id="2208c-159">Minimum</span></span>
- <span data-ttu-id="2208c-160">까지</span><span class="sxs-lookup"><span data-stu-id="2208c-160">Maximum</span></span>
- <span data-ttu-id="2208c-161">마지막</span><span class="sxs-lookup"><span data-stu-id="2208c-161">Last</span></span>
- <span data-ttu-id="2208c-162">총계, 개수</span><span class="sxs-lookup"><span data-stu-id="2208c-162">Total, Count</span></span>

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

### <span data-ttu-id="2208c-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2208c-163">-TimeGrain</span></span>
<span data-ttu-id="2208c-164">시간 세분화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="2208c-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="2208c-165">-TimeWindow</span></span>
<span data-ttu-id="2208c-166">시간 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="2208c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2208c-167">CommonParameters</span></span>
<span data-ttu-id="2208c-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2208c-169">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2208c-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2208c-170">입력</span><span class="sxs-lookup"><span data-stu-id="2208c-170">INPUTS</span></span>

### <span data-ttu-id="2208c-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2208c-171">System.String</span></span>

### <span data-ttu-id="2208c-172">ComparisonOperationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="2208c-173">MetricStatisticType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="2208c-174">System. 2</span><span class="sxs-lookup"><span data-stu-id="2208c-174">System.Double</span></span>

### <span data-ttu-id="2208c-175">TimeAggregationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="2208c-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="2208c-176">System.TimeSpan</span></span>

### <span data-ttu-id="2208c-177">ScaleDirection를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="2208c-178">ScaleType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="2208c-179">출력</span><span class="sxs-lookup"><span data-stu-id="2208c-179">OUTPUTS</span></span>

### <span data-ttu-id="2208c-180">ScaleRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2208c-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="2208c-181">상속자</span><span class="sxs-lookup"><span data-stu-id="2208c-181">NOTES</span></span>

## <span data-ttu-id="2208c-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2208c-182">RELATED LINKS</span></span>

[<span data-ttu-id="2208c-183">추가-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2208c-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="2208c-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="2208c-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="2208c-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2208c-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="2208c-186">새로운 AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="2208c-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="2208c-187">제거-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2208c-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


