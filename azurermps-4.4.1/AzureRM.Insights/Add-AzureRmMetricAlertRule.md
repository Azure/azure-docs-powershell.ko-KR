---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711549"
---
# <span data-ttu-id="51a50-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="51a50-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="51a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a50-102">SYNOPSIS</span></span>
<span data-ttu-id="51a50-103">메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51a50-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51a50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="51a50-105">DESCRIPTION</span></span>
<span data-ttu-id="51a50-106">**Add-AzureRmMetricAlertRule** cmdlet은 메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="51a50-107">추가 된 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="51a50-108">예제의</span><span class="sxs-lookup"><span data-stu-id="51a50-108">EXAMPLES</span></span>

### <span data-ttu-id="51a50-109">예제 1: 웹 사이트에 메트릭 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="51a50-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="51a50-110">이 명령은 웹 사이트에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="51a50-111">예제 2: 규칙 비활성화</span><span class="sxs-lookup"><span data-stu-id="51a50-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="51a50-112">이 명령은 규칙을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-112">This command disables a rule.</span></span>
<span data-ttu-id="51a50-113">규칙이 없는 경우 해당 규칙을 사용할 수 없게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="51a50-114">규칙이 있는 경우 해당 규칙을 사용 하지 않도록 설정 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="51a50-115">예제 3: 작업을 사용 하 여 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="51a50-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="51a50-116">이 명령은 웹 사이트에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="51a50-117">변수</span><span class="sxs-lookup"><span data-stu-id="51a50-117">PARAMETERS</span></span>

### <span data-ttu-id="51a50-118">-작업</span><span class="sxs-lookup"><span data-stu-id="51a50-118">-Actions</span></span>
<span data-ttu-id="51a50-119">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-119">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a50-120">-설명</span><span class="sxs-lookup"><span data-stu-id="51a50-120">-Description</span></span>
<span data-ttu-id="51a50-121">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-121">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a50-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="51a50-122">-DisableRule</span></span>
<span data-ttu-id="51a50-123">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-123">Disables the rule.</span></span>
<span data-ttu-id="51a50-124">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-124">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a50-125">-위치</span><span class="sxs-lookup"><span data-stu-id="51a50-125">-Location</span></span>
<span data-ttu-id="51a50-126">규칙이 정의 된 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="51a50-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="51a50-127">-MetricName</span></span>
<span data-ttu-id="51a50-128">규칙이 모니터링 하는 메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="51a50-129">메트릭 기반 규칙에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="51a50-130">-이름</span><span class="sxs-lookup"><span data-stu-id="51a50-130">-Name</span></span>
<span data-ttu-id="51a50-131">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="51a50-132">-연산자</span><span class="sxs-lookup"><span data-stu-id="51a50-132">-Operator</span></span>
<span data-ttu-id="51a50-133">규칙의 조건에 대 한 관계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="51a50-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51a50-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="51a50-135">GreaterThan</span></span>
- <span data-ttu-id="51a50-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="51a50-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="51a50-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="51a50-137">LessThan</span></span>
- <span data-ttu-id="51a50-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="51a50-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a50-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51a50-139">-ResourceGroup</span></span>
<span data-ttu-id="51a50-140">규칙에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="51a50-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="51a50-141">-TargetResourceId</span></span>
<span data-ttu-id="51a50-142">규칙이 모니터링 하는 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="51a50-143">참고:이 속성은 기존 경고 규칙에 대해 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="51a50-144">-임계값</span><span class="sxs-lookup"><span data-stu-id="51a50-144">-Threshold</span></span>
<span data-ttu-id="51a50-145">규칙의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="51a50-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="51a50-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="51a50-147">규칙을 평가할 때 시간 창에 적용할 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a50-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="51a50-148">-WindowSize</span></span>
<span data-ttu-id="51a50-149">해당 데이터를 계산 하는 규칙의 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="51a50-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a50-150">-DefaultProfile</span></span>
<span data-ttu-id="51a50-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51a50-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a50-152">CommonParameters</span></span>
<span data-ttu-id="51a50-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a50-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a50-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a50-155">입력</span><span class="sxs-lookup"><span data-stu-id="51a50-155">INPUTS</span></span>

## <span data-ttu-id="51a50-156">출력</span><span class="sxs-lookup"><span data-stu-id="51a50-156">OUTPUTS</span></span>

### <span data-ttu-id="51a50-157">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="51a50-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="51a50-158">상속자</span><span class="sxs-lookup"><span data-stu-id="51a50-158">NOTES</span></span>

## <span data-ttu-id="51a50-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51a50-159">RELATED LINKS</span></span>

[<span data-ttu-id="51a50-160">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="51a50-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="51a50-161">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="51a50-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="51a50-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="51a50-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="51a50-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="51a50-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="51a50-164">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="51a50-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="51a50-165">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="51a50-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="51a50-166">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="51a50-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


