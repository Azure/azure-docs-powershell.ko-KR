---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
ms.openlocfilehash: 785424560ebd0af3ce7035265e9fb64b22713049
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881561"
---
# <span data-ttu-id="9d8e9-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9d8e9-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="9d8e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d8e9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8e9-103">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d8e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d8e9-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d8e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d8e9-105">DESCRIPTION</span></span>
<span data-ttu-id="9d8e9-106">**AzureRmAutoscaleRule** Cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="9d8e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9d8e9-107">EXAMPLES</span></span>

### <span data-ttu-id="9d8e9-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="9d8e9-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9d8e9-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-109">This command creates a rule.</span></span>

### <span data-ttu-id="9d8e9-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="9d8e9-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9d8e9-111">첫 번째 명령은 요청 메트릭에 대 한 규칙을 만든 다음이를 $Rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="9d8e9-112">두 번째 명령은 요청 메트릭에 대 한 두 번째 규칙을 만든 다음이를 $Rule 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="9d8e9-113">변수</span><span class="sxs-lookup"><span data-stu-id="9d8e9-113">PARAMETERS</span></span>

### <span data-ttu-id="9d8e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8e9-114">-DefaultProfile</span></span>
<span data-ttu-id="9d8e9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d8e9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8e9-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9d8e9-116">-MetricName</span></span>
<span data-ttu-id="9d8e9-117">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="9d8e9-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="9d8e9-118">-MetricResourceId</span></span>
<span data-ttu-id="9d8e9-119">메트릭 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="9d8e9-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="9d8e9-120">-MetricStatistic</span></span>
<span data-ttu-id="9d8e9-121">메트릭 통계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="9d8e9-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8e9-123">보통</span><span class="sxs-lookup"><span data-stu-id="9d8e9-123">Average</span></span>
- <span data-ttu-id="9d8e9-124">Occurs</span><span class="sxs-lookup"><span data-stu-id="9d8e9-124">Min</span></span>
- <span data-ttu-id="9d8e9-125">Max</span><span class="sxs-lookup"><span data-stu-id="9d8e9-125">Max</span></span>
- <span data-ttu-id="9d8e9-126">총계</span><span class="sxs-lookup"><span data-stu-id="9d8e9-126">Sum</span></span>

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

### <span data-ttu-id="9d8e9-127">-연산자</span><span class="sxs-lookup"><span data-stu-id="9d8e9-127">-Operator</span></span>
<span data-ttu-id="9d8e9-128">연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-128">Specifies the operator.</span></span>
<span data-ttu-id="9d8e9-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8e9-130">본인이</span><span class="sxs-lookup"><span data-stu-id="9d8e9-130">Equals</span></span>
- <span data-ttu-id="9d8e9-131">참고 $ Als</span><span class="sxs-lookup"><span data-stu-id="9d8e9-131">NotEquals</span></span>
- <span data-ttu-id="9d8e9-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="9d8e9-132">GreaterThan</span></span>
- <span data-ttu-id="9d8e9-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9d8e9-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="9d8e9-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="9d8e9-134">LessThan</span></span>
- <span data-ttu-id="9d8e9-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9d8e9-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="9d8e9-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="9d8e9-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="9d8e9-137">자동 크기 조정 작업 쿨 다운 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="9d8e9-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="9d8e9-138">-ScaleActionDirection</span></span>
<span data-ttu-id="9d8e9-139">크기 조정 작업 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="9d8e9-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8e9-141">않아야</span><span class="sxs-lookup"><span data-stu-id="9d8e9-141">None</span></span>
- <span data-ttu-id="9d8e9-142">늘리거나</span><span class="sxs-lookup"><span data-stu-id="9d8e9-142">Increase</span></span>
- <span data-ttu-id="9d8e9-143">낮출</span><span class="sxs-lookup"><span data-stu-id="9d8e9-143">Decrease</span></span>

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

### <span data-ttu-id="9d8e9-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="9d8e9-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="9d8e9-145">눈금 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-145">Specifies the scale type.</span></span>
<span data-ttu-id="9d8e9-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8e9-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="9d8e9-147">ChangeSize</span></span>
- <span data-ttu-id="9d8e9-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="9d8e9-148">ChangeCount</span></span>
- <span data-ttu-id="9d8e9-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="9d8e9-149">PercentChangeCount</span></span>
- <span data-ttu-id="9d8e9-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="9d8e9-150">ExactCount</span></span>

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

### <span data-ttu-id="9d8e9-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="9d8e9-151">-ScaleActionValue</span></span>
<span data-ttu-id="9d8e9-152">작업 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="9d8e9-153">-임계값</span><span class="sxs-lookup"><span data-stu-id="9d8e9-153">-Threshold</span></span>
<span data-ttu-id="9d8e9-154">메트릭 값의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="9d8e9-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="9d8e9-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="9d8e9-156">시간 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="9d8e9-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d8e9-158">보통</span><span class="sxs-lookup"><span data-stu-id="9d8e9-158">Average</span></span>
- <span data-ttu-id="9d8e9-159">솟</span><span class="sxs-lookup"><span data-stu-id="9d8e9-159">Minimum</span></span>
- <span data-ttu-id="9d8e9-160">까지</span><span class="sxs-lookup"><span data-stu-id="9d8e9-160">Maximum</span></span>
- <span data-ttu-id="9d8e9-161">마지막</span><span class="sxs-lookup"><span data-stu-id="9d8e9-161">Last</span></span>
- <span data-ttu-id="9d8e9-162">총계, 개수</span><span class="sxs-lookup"><span data-stu-id="9d8e9-162">Total, Count</span></span>

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

### <span data-ttu-id="9d8e9-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="9d8e9-163">-TimeGrain</span></span>
<span data-ttu-id="9d8e9-164">시간 세분화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="9d8e9-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="9d8e9-165">-TimeWindow</span></span>
<span data-ttu-id="9d8e9-166">시간 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="9d8e9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8e9-167">CommonParameters</span></span>
<span data-ttu-id="9d8e9-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8e9-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8e9-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8e9-170">입력</span><span class="sxs-lookup"><span data-stu-id="9d8e9-170">INPUTS</span></span>

### <span data-ttu-id="9d8e9-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9d8e9-171">System.String</span></span>

### <span data-ttu-id="9d8e9-172">ComparisonOperationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="9d8e9-173">MetricStatisticType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="9d8e9-174">System. 2</span><span class="sxs-lookup"><span data-stu-id="9d8e9-174">System.Double</span></span>

### <span data-ttu-id="9d8e9-175">TimeAggregationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="9d8e9-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9d8e9-176">System.TimeSpan</span></span>

### <span data-ttu-id="9d8e9-177">ScaleDirection를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="9d8e9-178">ScaleType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="9d8e9-179">출력</span><span class="sxs-lookup"><span data-stu-id="9d8e9-179">OUTPUTS</span></span>

### <span data-ttu-id="9d8e9-180">ScaleRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8e9-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="9d8e9-181">상속자</span><span class="sxs-lookup"><span data-stu-id="9d8e9-181">NOTES</span></span>

## <span data-ttu-id="9d8e9-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d8e9-182">RELATED LINKS</span></span>

[<span data-ttu-id="9d8e9-183">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d8e9-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9d8e9-184">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="9d8e9-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="9d8e9-185">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d8e9-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9d8e9-186">새로운 AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9d8e9-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="9d8e9-187">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d8e9-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


