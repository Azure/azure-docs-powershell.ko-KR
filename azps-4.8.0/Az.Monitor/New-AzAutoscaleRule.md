---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214431"
---
# <span data-ttu-id="5b7b0-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="5b7b0-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="5b7b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7b0-103">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="5b7b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b7b0-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b7b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b7b0-105">DESCRIPTION</span></span>
<span data-ttu-id="5b7b0-106">**AzAutoscaleRule** Cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="5b7b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b7b0-107">EXAMPLES</span></span>

### <span data-ttu-id="5b7b0-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5b7b0-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="5b7b0-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-109">This command creates a rule.</span></span>

### <span data-ttu-id="5b7b0-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5b7b0-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="5b7b0-111">첫 번째 명령은 요청 메트릭에 대 한 규칙을 만든 다음이를 $Rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="5b7b0-112">두 번째 명령은 요청 메트릭에 대 한 두 번째 규칙을 만든 다음이를 $Rule 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="5b7b0-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="5b7b0-113">Example 3</span></span>

<span data-ttu-id="5b7b0-114">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="5b7b0-115">생성</span><span class="sxs-lookup"><span data-stu-id="5b7b0-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="5b7b0-116">변수</span><span class="sxs-lookup"><span data-stu-id="5b7b0-116">PARAMETERS</span></span>

### <span data-ttu-id="5b7b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7b0-117">-DefaultProfile</span></span>
<span data-ttu-id="5b7b0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5b7b0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b7b0-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="5b7b0-119">-MetricName</span></span>
<span data-ttu-id="5b7b0-120">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="5b7b0-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7b0-121">-MetricResourceId</span></span>
<span data-ttu-id="5b7b0-122">메트릭 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="5b7b0-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="5b7b0-123">-MetricStatistic</span></span>
<span data-ttu-id="5b7b0-124">메트릭 통계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="5b7b0-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b7b0-126">보통</span><span class="sxs-lookup"><span data-stu-id="5b7b0-126">Average</span></span>
- <span data-ttu-id="5b7b0-127">Occurs</span><span class="sxs-lookup"><span data-stu-id="5b7b0-127">Min</span></span>
- <span data-ttu-id="5b7b0-128">Max</span><span class="sxs-lookup"><span data-stu-id="5b7b0-128">Max</span></span>
- <span data-ttu-id="5b7b0-129">총계</span><span class="sxs-lookup"><span data-stu-id="5b7b0-129">Sum</span></span>

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

### <span data-ttu-id="5b7b0-130">-연산자</span><span class="sxs-lookup"><span data-stu-id="5b7b0-130">-Operator</span></span>
<span data-ttu-id="5b7b0-131">연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-131">Specifies the operator.</span></span>
<span data-ttu-id="5b7b0-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b7b0-133">본인이</span><span class="sxs-lookup"><span data-stu-id="5b7b0-133">Equals</span></span>
- <span data-ttu-id="5b7b0-134">참고 $ Als</span><span class="sxs-lookup"><span data-stu-id="5b7b0-134">NotEquals</span></span>
- <span data-ttu-id="5b7b0-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="5b7b0-135">GreaterThan</span></span>
- <span data-ttu-id="5b7b0-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5b7b0-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="5b7b0-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="5b7b0-137">LessThan</span></span>
- <span data-ttu-id="5b7b0-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="5b7b0-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="5b7b0-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="5b7b0-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="5b7b0-140">자동 크기 조정 작업 쿨 다운 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="5b7b0-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="5b7b0-141">-ScaleActionDirection</span></span>
<span data-ttu-id="5b7b0-142">크기 조정 작업 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="5b7b0-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b7b0-144">않아야</span><span class="sxs-lookup"><span data-stu-id="5b7b0-144">None</span></span>
- <span data-ttu-id="5b7b0-145">늘리거나</span><span class="sxs-lookup"><span data-stu-id="5b7b0-145">Increase</span></span>
- <span data-ttu-id="5b7b0-146">낮출</span><span class="sxs-lookup"><span data-stu-id="5b7b0-146">Decrease</span></span>

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

### <span data-ttu-id="5b7b0-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="5b7b0-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="5b7b0-148">눈금 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-148">Specifies the scale type.</span></span>
<span data-ttu-id="5b7b0-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b7b0-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="5b7b0-150">ChangeSize</span></span>
- <span data-ttu-id="5b7b0-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="5b7b0-151">ChangeCount</span></span>
- <span data-ttu-id="5b7b0-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="5b7b0-152">PercentChangeCount</span></span>
- <span data-ttu-id="5b7b0-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="5b7b0-153">ExactCount</span></span>

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

### <span data-ttu-id="5b7b0-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="5b7b0-154">-ScaleActionValue</span></span>
<span data-ttu-id="5b7b0-155">작업 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="5b7b0-156">-임계값</span><span class="sxs-lookup"><span data-stu-id="5b7b0-156">-Threshold</span></span>
<span data-ttu-id="5b7b0-157">메트릭 값의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="5b7b0-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="5b7b0-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="5b7b0-159">시간 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="5b7b0-160">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b7b0-161">보통</span><span class="sxs-lookup"><span data-stu-id="5b7b0-161">Average</span></span>
- <span data-ttu-id="5b7b0-162">솟</span><span class="sxs-lookup"><span data-stu-id="5b7b0-162">Minimum</span></span>
- <span data-ttu-id="5b7b0-163">까지</span><span class="sxs-lookup"><span data-stu-id="5b7b0-163">Maximum</span></span>
- <span data-ttu-id="5b7b0-164">마지막</span><span class="sxs-lookup"><span data-stu-id="5b7b0-164">Last</span></span>
- <span data-ttu-id="5b7b0-165">총계, 개수</span><span class="sxs-lookup"><span data-stu-id="5b7b0-165">Total, Count</span></span>

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

### <span data-ttu-id="5b7b0-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="5b7b0-166">-TimeGrain</span></span>
<span data-ttu-id="5b7b0-167">시간 세분화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="5b7b0-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="5b7b0-168">-TimeWindow</span></span>
<span data-ttu-id="5b7b0-169">시간 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="5b7b0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7b0-170">CommonParameters</span></span>
<span data-ttu-id="5b7b0-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7b0-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7b0-173">입력</span><span class="sxs-lookup"><span data-stu-id="5b7b0-173">INPUTS</span></span>

### <span data-ttu-id="5b7b0-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b7b0-174">System.String</span></span>

### <span data-ttu-id="5b7b0-175">ComparisonOperationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="5b7b0-176">MetricStatisticType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="5b7b0-177">System. 2</span><span class="sxs-lookup"><span data-stu-id="5b7b0-177">System.Double</span></span>

### <span data-ttu-id="5b7b0-178">TimeAggregationType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="5b7b0-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5b7b0-179">System.TimeSpan</span></span>

### <span data-ttu-id="5b7b0-180">ScaleDirection를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="5b7b0-181">ScaleType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="5b7b0-182">출력</span><span class="sxs-lookup"><span data-stu-id="5b7b0-182">OUTPUTS</span></span>

### <span data-ttu-id="5b7b0-183">ScaleRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="5b7b0-184">상속자</span><span class="sxs-lookup"><span data-stu-id="5b7b0-184">NOTES</span></span>

## <span data-ttu-id="5b7b0-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b7b0-185">RELATED LINKS</span></span>

[<span data-ttu-id="5b7b0-186">추가-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5b7b0-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="5b7b0-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="5b7b0-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="5b7b0-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5b7b0-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="5b7b0-189">새로운 AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="5b7b0-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="5b7b0-190">제거-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5b7b0-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


