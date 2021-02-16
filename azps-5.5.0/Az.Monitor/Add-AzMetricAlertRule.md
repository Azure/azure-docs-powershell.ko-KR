---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180196"
---
# <span data-ttu-id="f3bfc-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f3bfc-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="f3bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bfc-103">메트릭 기반 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="f3bfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3bfc-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3bfc-105">설명</span><span class="sxs-lookup"><span data-stu-id="f3bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="f3bfc-106">**Add-AzMetricAlertRule** cmdlet은 메트릭 기반 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="f3bfc-107">추가된 규칙은 리소스 그룹과 연결하며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="f3bfc-108">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f3bfc-109">예제</span><span class="sxs-lookup"><span data-stu-id="f3bfc-109">EXAMPLES</span></span>

### <span data-ttu-id="f3bfc-110">예제 1: 웹 사이트에 메트릭 경고 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="f3bfc-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="f3bfc-111">이 명령은 웹 사이트에 대한 메트릭 경고 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="f3bfc-112">예제 2: 규칙 사용 안</span><span class="sxs-lookup"><span data-stu-id="f3bfc-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="f3bfc-113">이 명령은 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-113">This command disables a rule.</span></span>
<span data-ttu-id="f3bfc-114">규칙이 없는 경우 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="f3bfc-115">규칙이 있으면 해당 규칙만 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="f3bfc-116">예제 3: 작업이 있는 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="f3bfc-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="f3bfc-117">이 명령은 웹 사이트에 대한 메트릭 경고 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="f3bfc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3bfc-118">PARAMETERS</span></span>

### <span data-ttu-id="f3bfc-119">-Action</span><span class="sxs-lookup"><span data-stu-id="f3bfc-119">-Action</span></span>
<span data-ttu-id="f3bfc-120">콤마로 구분된 작업 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="f3bfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bfc-121">-DefaultProfile</span></span>
<span data-ttu-id="f3bfc-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3bfc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3bfc-123">-Description</span><span class="sxs-lookup"><span data-stu-id="f3bfc-123">-Description</span></span>
<span data-ttu-id="f3bfc-124">규칙에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="f3bfc-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f3bfc-125">-DisableRule</span></span>
<span data-ttu-id="f3bfc-126">규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-126">Disables the rule.</span></span>
<span data-ttu-id="f3bfc-127">이 매개 변수를 지정하지 않으면 규칙이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="f3bfc-128">-Location</span><span class="sxs-lookup"><span data-stu-id="f3bfc-128">-Location</span></span>
<span data-ttu-id="f3bfc-129">규칙이 정의된 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="f3bfc-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="f3bfc-130">-MetricName</span></span>
<span data-ttu-id="f3bfc-131">규칙이 모니터링하는 메트릭의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="f3bfc-132">메트릭 기반 규칙에만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="f3bfc-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f3bfc-133">-Name</span></span>
<span data-ttu-id="f3bfc-134">규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="f3bfc-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="f3bfc-135">-Operator</span></span>
<span data-ttu-id="f3bfc-136">규칙 조건에 대한 관계 연산자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="f3bfc-137">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="f3bfc-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f3bfc-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f3bfc-138">GreaterThan</span></span>
- <span data-ttu-id="f3bfc-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f3bfc-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="f3bfc-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="f3bfc-140">LessThan</span></span>
- <span data-ttu-id="f3bfc-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f3bfc-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="f3bfc-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bfc-142">-ResourceGroupName</span></span>
<span data-ttu-id="f3bfc-143">규칙에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bfc-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f3bfc-144">-TargetResourceId</span></span>
<span data-ttu-id="f3bfc-145">규칙이 모니터링하는 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="f3bfc-146">참고: 이 속성은 기존 경고 규칙에 대해 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="f3bfc-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="f3bfc-147">-Threshold</span></span>
<span data-ttu-id="f3bfc-148">규칙의 임계값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="f3bfc-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="f3bfc-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="f3bfc-150">규칙을 평가할 때 기간에 적용할 집계 연산자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="f3bfc-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="f3bfc-151">-WindowSize</span></span>
<span data-ttu-id="f3bfc-152">해당 데이터를 계산하는 규칙의 기간 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="f3bfc-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3bfc-153">-Confirm</span></span>
<span data-ttu-id="f3bfc-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bfc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bfc-155">-WhatIf</span></span>
<span data-ttu-id="f3bfc-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3bfc-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3bfc-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bfc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bfc-158">CommonParameters</span></span>
<span data-ttu-id="f3bfc-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bfc-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bfc-161">입력</span><span class="sxs-lookup"><span data-stu-id="f3bfc-161">INPUTS</span></span>

### <span data-ttu-id="f3bfc-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f3bfc-162">System.TimeSpan</span></span>

### <span data-ttu-id="f3bfc-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="f3bfc-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="f3bfc-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="f3bfc-164">System.Double</span></span>

### <span data-ttu-id="f3bfc-165">System.String</span><span class="sxs-lookup"><span data-stu-id="f3bfc-165">System.String</span></span>

### <span data-ttu-id="f3bfc-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f3bfc-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f3bfc-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3bfc-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f3bfc-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f3bfc-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f3bfc-169">출력</span><span class="sxs-lookup"><span data-stu-id="f3bfc-169">OUTPUTS</span></span>

### <span data-ttu-id="f3bfc-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f3bfc-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="f3bfc-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3bfc-171">NOTES</span></span>

## <span data-ttu-id="f3bfc-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3bfc-172">RELATED LINKS</span></span>

[<span data-ttu-id="f3bfc-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3bfc-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f3bfc-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f3bfc-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="f3bfc-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f3bfc-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="f3bfc-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="f3bfc-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="f3bfc-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f3bfc-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="f3bfc-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="f3bfc-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="f3bfc-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="f3bfc-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


