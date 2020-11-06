---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529815"
---
# <span data-ttu-id="766c2-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="766c2-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="766c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766c2-102">SYNOPSIS</span></span>
<span data-ttu-id="766c2-103">메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="766c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="766c2-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="766c2-105">DESCRIPTION</span></span>
<span data-ttu-id="766c2-106">**Add-AzureRmMetricAlertRule** cmdlet은 메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="766c2-107">추가 된 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="766c2-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="766c2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="766c2-109">EXAMPLES</span></span>

### <span data-ttu-id="766c2-110">예제 1: 웹 사이트에 메트릭 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="766c2-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="766c2-111">이 명령은 웹 사이트에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="766c2-112">예제 2: 규칙 비활성화</span><span class="sxs-lookup"><span data-stu-id="766c2-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="766c2-113">이 명령은 규칙을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-113">This command disables a rule.</span></span>
<span data-ttu-id="766c2-114">규칙이 없는 경우 해당 규칙을 사용할 수 없게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="766c2-115">규칙이 있는 경우 해당 규칙을 사용 하지 않도록 설정 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="766c2-116">예제 3: 작업을 사용 하 여 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="766c2-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="766c2-117">이 명령은 웹 사이트에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="766c2-118">변수</span><span class="sxs-lookup"><span data-stu-id="766c2-118">PARAMETERS</span></span>

### <span data-ttu-id="766c2-119">-작업</span><span class="sxs-lookup"><span data-stu-id="766c2-119">-Action</span></span>
<span data-ttu-id="766c2-120">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766c2-121">-DefaultProfile</span></span>
<span data-ttu-id="766c2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="766c2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="766c2-123">-설명</span><span class="sxs-lookup"><span data-stu-id="766c2-123">-Description</span></span>
<span data-ttu-id="766c2-124">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-124">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="766c2-125">-DisableRule</span></span>
<span data-ttu-id="766c2-126">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-126">Disables the rule.</span></span>
<span data-ttu-id="766c2-127">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-128">-위치</span><span class="sxs-lookup"><span data-stu-id="766c2-128">-Location</span></span>
<span data-ttu-id="766c2-129">규칙이 정의 된 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="766c2-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="766c2-130">-MetricName</span></span>
<span data-ttu-id="766c2-131">규칙이 모니터링 하는 메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="766c2-132">메트릭 기반 규칙에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="766c2-133">-이름</span><span class="sxs-lookup"><span data-stu-id="766c2-133">-Name</span></span>
<span data-ttu-id="766c2-134">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="766c2-135">-연산자</span><span class="sxs-lookup"><span data-stu-id="766c2-135">-Operator</span></span>
<span data-ttu-id="766c2-136">규칙의 조건에 대 한 관계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="766c2-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="766c2-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="766c2-138">GreaterThan</span></span>
- <span data-ttu-id="766c2-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="766c2-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="766c2-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="766c2-140">LessThan</span></span>
- <span data-ttu-id="766c2-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="766c2-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766c2-142">-ResourceGroupName</span></span>
<span data-ttu-id="766c2-143">규칙에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="766c2-144">-TargetResourceId</span></span>
<span data-ttu-id="766c2-145">규칙이 모니터링 하는 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="766c2-146">참고:이 속성은 기존 경고 규칙에 대해 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="766c2-147">-임계값</span><span class="sxs-lookup"><span data-stu-id="766c2-147">-Threshold</span></span>
<span data-ttu-id="766c2-148">규칙의 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="766c2-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="766c2-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="766c2-150">규칙을 평가할 때 시간 창에 적용할 집계 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766c2-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="766c2-151">-WindowSize</span></span>
<span data-ttu-id="766c2-152">해당 데이터를 계산 하는 규칙의 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="766c2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766c2-153">CommonParameters</span></span>
<span data-ttu-id="766c2-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766c2-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="766c2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766c2-156">입력</span><span class="sxs-lookup"><span data-stu-id="766c2-156">INPUTS</span></span>

### <span data-ttu-id="766c2-157">않아야</span><span class="sxs-lookup"><span data-stu-id="766c2-157">None</span></span>
<span data-ttu-id="766c2-158">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="766c2-159">출력</span><span class="sxs-lookup"><span data-stu-id="766c2-159">OUTPUTS</span></span>

### <span data-ttu-id="766c2-160">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="766c2-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="766c2-161">상속자</span><span class="sxs-lookup"><span data-stu-id="766c2-161">NOTES</span></span>

## <span data-ttu-id="766c2-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="766c2-162">RELATED LINKS</span></span>

[<span data-ttu-id="766c2-163">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="766c2-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="766c2-164">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="766c2-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="766c2-165">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="766c2-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="766c2-166">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="766c2-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="766c2-167">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="766c2-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="766c2-168">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="766c2-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="766c2-169">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="766c2-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


