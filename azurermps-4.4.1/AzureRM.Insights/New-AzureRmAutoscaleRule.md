---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536376"
---
# <span data-ttu-id="934d2-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="934d2-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="934d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="934d2-102">SYNOPSIS</span></span>
<span data-ttu-id="934d2-103">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="934d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="934d2-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="934d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="934d2-105">DESCRIPTION</span></span>
<span data-ttu-id="934d2-106">**AzureRmAutoscaleRule** Cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="934d2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="934d2-107">EXAMPLES</span></span>

### <span data-ttu-id="934d2-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="934d2-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="934d2-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-109">This command creates a rule.</span></span>

### <span data-ttu-id="934d2-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="934d2-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="934d2-111">첫 번째 명령은 요청 메트릭에 대 한 규칙을 만든 다음이를 $Rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="934d2-112">두 번째 명령은 요청 메트릭에 대 한 두 번째 규칙을 만든 다음이를 $Rule 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="934d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="934d2-113">PARAMETERS</span></span>

### <span data-ttu-id="934d2-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="934d2-114">-MetricName</span></span>
<span data-ttu-id="934d2-115">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="934d2-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="934d2-116">-MetricResourceId</span></span>
<span data-ttu-id="934d2-117">메트릭 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="934d2-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="934d2-118">-MetricStatistic</span></span>
<span data-ttu-id="934d2-119">메트릭 통계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="934d2-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="934d2-121">보통</span><span class="sxs-lookup"><span data-stu-id="934d2-121">Average</span></span>
- <span data-ttu-id="934d2-122">Occurs</span><span class="sxs-lookup"><span data-stu-id="934d2-122">Min</span></span>
- <span data-ttu-id="934d2-123">Max</span><span class="sxs-lookup"><span data-stu-id="934d2-123">Max</span></span>
- <span data-ttu-id="934d2-124">총계</span><span class="sxs-lookup"><span data-stu-id="934d2-124">Sum</span></span>

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

### <span data-ttu-id="934d2-125">-연산자</span><span class="sxs-lookup"><span data-stu-id="934d2-125">-Operator</span></span>
<span data-ttu-id="934d2-126">연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-126">Specifies the operator.</span></span>
<span data-ttu-id="934d2-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="934d2-128">본인이</span><span class="sxs-lookup"><span data-stu-id="934d2-128">Equals</span></span>
- <span data-ttu-id="934d2-129">참고 $ Als</span><span class="sxs-lookup"><span data-stu-id="934d2-129">NotEquals</span></span>
- <span data-ttu-id="934d2-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="934d2-130">GreaterThan</span></span>
- <span data-ttu-id="934d2-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="934d2-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="934d2-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="934d2-132">LessThan</span></span>
- <span data-ttu-id="934d2-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="934d2-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="934d2-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="934d2-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="934d2-135">자동 크기 조정 작업 쿨 다운 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="934d2-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="934d2-136">-ScaleActionDirection</span></span>
<span data-ttu-id="934d2-137">크기 조정 작업 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="934d2-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="934d2-139">않아야</span><span class="sxs-lookup"><span data-stu-id="934d2-139">None</span></span>
- <span data-ttu-id="934d2-140">늘리거나</span><span class="sxs-lookup"><span data-stu-id="934d2-140">Increase</span></span>
- <span data-ttu-id="934d2-141">낮출</span><span class="sxs-lookup"><span data-stu-id="934d2-141">Decrease</span></span>

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

### <span data-ttu-id="934d2-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="934d2-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="934d2-143">눈금 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-143">Specifies the scale type.</span></span>
<span data-ttu-id="934d2-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="934d2-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="934d2-145">ChangeSize</span></span>
- <span data-ttu-id="934d2-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="934d2-146">ChangeCount</span></span>
- <span data-ttu-id="934d2-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="934d2-147">PercentChangeCount</span></span>
- <span data-ttu-id="934d2-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="934d2-148">ExactCount</span></span>

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

### <span data-ttu-id="934d2-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="934d2-149">-ScaleActionValue</span></span>
<span data-ttu-id="934d2-150">작업 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="934d2-151">-임계값</span><span class="sxs-lookup"><span data-stu-id="934d2-151">-Threshold</span></span>
<span data-ttu-id="934d2-152">메트릭 값의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="934d2-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="934d2-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="934d2-154">시간 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="934d2-155">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="934d2-156">보통</span><span class="sxs-lookup"><span data-stu-id="934d2-156">Average</span></span>
- <span data-ttu-id="934d2-157">솟</span><span class="sxs-lookup"><span data-stu-id="934d2-157">Minimum</span></span>
- <span data-ttu-id="934d2-158">까지</span><span class="sxs-lookup"><span data-stu-id="934d2-158">Maximum</span></span>
- <span data-ttu-id="934d2-159">마지막</span><span class="sxs-lookup"><span data-stu-id="934d2-159">Last</span></span>
- <span data-ttu-id="934d2-160">총계, 개수</span><span class="sxs-lookup"><span data-stu-id="934d2-160">Total, Count</span></span>

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

### <span data-ttu-id="934d2-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="934d2-161">-TimeGrain</span></span>
<span data-ttu-id="934d2-162">시간 세분화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="934d2-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="934d2-163">-TimeWindow</span></span>
<span data-ttu-id="934d2-164">시간 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="934d2-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934d2-165">-DefaultProfile</span></span>
<span data-ttu-id="934d2-166">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="934d2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934d2-167">CommonParameters</span></span>
<span data-ttu-id="934d2-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934d2-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934d2-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934d2-170">입력</span><span class="sxs-lookup"><span data-stu-id="934d2-170">INPUTS</span></span>

## <span data-ttu-id="934d2-171">출력</span><span class="sxs-lookup"><span data-stu-id="934d2-171">OUTPUTS</span></span>

### <span data-ttu-id="934d2-172">ScaleRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="934d2-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="934d2-173">상속자</span><span class="sxs-lookup"><span data-stu-id="934d2-173">NOTES</span></span>

## <span data-ttu-id="934d2-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="934d2-174">RELATED LINKS</span></span>

[<span data-ttu-id="934d2-175">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="934d2-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="934d2-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="934d2-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="934d2-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="934d2-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="934d2-178">새로운 AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="934d2-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="934d2-179">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="934d2-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


