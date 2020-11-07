---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703277"
---
# <span data-ttu-id="213c0-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="213c0-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="213c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213c0-102">SYNOPSIS</span></span>
<span data-ttu-id="213c0-103">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="213c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="213c0-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="213c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="213c0-105">DESCRIPTION</span></span>
<span data-ttu-id="213c0-106">**AzureRmAutoscaleRule** Cmdlet은 자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="213c0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="213c0-107">EXAMPLES</span></span>

### <span data-ttu-id="213c0-108">예제 1: 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="213c0-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="213c0-109">이 명령은 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-109">This command creates a rule.</span></span>

### <span data-ttu-id="213c0-110">예제 2: 두 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="213c0-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="213c0-111">첫 번째 명령은 요청 메트릭에 대 한 규칙을 만든 다음이를 $Rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="213c0-112">두 번째 명령은 요청 메트릭에 대 한 두 번째 규칙을 만든 다음이를 $Rule 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="213c0-113">변수</span><span class="sxs-lookup"><span data-stu-id="213c0-113">PARAMETERS</span></span>

### <span data-ttu-id="213c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213c0-114">-DefaultProfile</span></span>
<span data-ttu-id="213c0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="213c0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="213c0-116">-MetricName</span></span>
<span data-ttu-id="213c0-117">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="213c0-118">-MetricResourceId</span></span>
<span data-ttu-id="213c0-119">메트릭 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="213c0-120">-MetricStatistic</span></span>
<span data-ttu-id="213c0-121">메트릭 통계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="213c0-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c0-123">보통</span><span class="sxs-lookup"><span data-stu-id="213c0-123">Average</span></span>
- <span data-ttu-id="213c0-124">Occurs</span><span class="sxs-lookup"><span data-stu-id="213c0-124">Min</span></span>
- <span data-ttu-id="213c0-125">Max</span><span class="sxs-lookup"><span data-stu-id="213c0-125">Max</span></span>
- <span data-ttu-id="213c0-126">총계</span><span class="sxs-lookup"><span data-stu-id="213c0-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-127">-연산자</span><span class="sxs-lookup"><span data-stu-id="213c0-127">-Operator</span></span>
<span data-ttu-id="213c0-128">연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-128">Specifies the operator.</span></span>
<span data-ttu-id="213c0-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c0-130">본인이</span><span class="sxs-lookup"><span data-stu-id="213c0-130">Equals</span></span>
- <span data-ttu-id="213c0-131">참고 $ Als</span><span class="sxs-lookup"><span data-stu-id="213c0-131">NotEquals</span></span>
- <span data-ttu-id="213c0-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="213c0-132">GreaterThan</span></span>
- <span data-ttu-id="213c0-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="213c0-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="213c0-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="213c0-134">LessThan</span></span>
- <span data-ttu-id="213c0-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="213c0-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="213c0-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="213c0-137">자동 크기 조정 작업 쿨 다운 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="213c0-138">-ScaleActionDirection</span></span>
<span data-ttu-id="213c0-139">크기 조정 작업 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="213c0-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c0-141">않아야</span><span class="sxs-lookup"><span data-stu-id="213c0-141">None</span></span>
- <span data-ttu-id="213c0-142">늘리거나</span><span class="sxs-lookup"><span data-stu-id="213c0-142">Increase</span></span>
- <span data-ttu-id="213c0-143">낮출</span><span class="sxs-lookup"><span data-stu-id="213c0-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="213c0-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="213c0-145">눈금 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-145">Specifies the scale type.</span></span>
<span data-ttu-id="213c0-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c0-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="213c0-147">ChangeSize</span></span>
- <span data-ttu-id="213c0-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="213c0-148">ChangeCount</span></span>
- <span data-ttu-id="213c0-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="213c0-149">PercentChangeCount</span></span>
- <span data-ttu-id="213c0-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="213c0-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="213c0-151">-ScaleActionValue</span></span>
<span data-ttu-id="213c0-152">작업 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-153">-임계값</span><span class="sxs-lookup"><span data-stu-id="213c0-153">-Threshold</span></span>
<span data-ttu-id="213c0-154">메트릭 값의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="213c0-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="213c0-156">시간 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="213c0-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="213c0-158">보통</span><span class="sxs-lookup"><span data-stu-id="213c0-158">Average</span></span>
- <span data-ttu-id="213c0-159">솟</span><span class="sxs-lookup"><span data-stu-id="213c0-159">Minimum</span></span>
- <span data-ttu-id="213c0-160">까지</span><span class="sxs-lookup"><span data-stu-id="213c0-160">Maximum</span></span>
- <span data-ttu-id="213c0-161">마지막</span><span class="sxs-lookup"><span data-stu-id="213c0-161">Last</span></span>
- <span data-ttu-id="213c0-162">총계, 개수</span><span class="sxs-lookup"><span data-stu-id="213c0-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="213c0-163">-TimeGrain</span></span>
<span data-ttu-id="213c0-164">시간 세분화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="213c0-165">-TimeWindow</span></span>
<span data-ttu-id="213c0-166">시간 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213c0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213c0-167">CommonParameters</span></span>
<span data-ttu-id="213c0-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213c0-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213c0-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213c0-170">입력</span><span class="sxs-lookup"><span data-stu-id="213c0-170">INPUTS</span></span>

### <span data-ttu-id="213c0-171">않아야</span><span class="sxs-lookup"><span data-stu-id="213c0-171">None</span></span>
<span data-ttu-id="213c0-172">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="213c0-173">출력</span><span class="sxs-lookup"><span data-stu-id="213c0-173">OUTPUTS</span></span>

### <span data-ttu-id="213c0-174">ScaleRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="213c0-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="213c0-175">상속자</span><span class="sxs-lookup"><span data-stu-id="213c0-175">NOTES</span></span>

## <span data-ttu-id="213c0-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="213c0-176">RELATED LINKS</span></span>

[<span data-ttu-id="213c0-177">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="213c0-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="213c0-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="213c0-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="213c0-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="213c0-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="213c0-180">새로운 AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="213c0-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="213c0-181">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="213c0-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


