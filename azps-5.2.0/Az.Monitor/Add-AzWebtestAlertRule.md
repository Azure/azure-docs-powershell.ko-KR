---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343449"
---
# <span data-ttu-id="c88fb-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c88fb-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="c88fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c88fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c88fb-103">웹 사이트 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="c88fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="c88fb-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c88fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="c88fb-105">DESCRIPTION</span></span>
<span data-ttu-id="c88fb-106">**Add-AzWebtestAlertRule** cmdlet은 메트릭, 이벤트 또는 webtest 형식의 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="c88fb-107">추가된 규칙은 리소스 그룹에 연결되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="c88fb-108">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c88fb-109">예제</span><span class="sxs-lookup"><span data-stu-id="c88fb-109">EXAMPLES</span></span>

### <span data-ttu-id="c88fb-110">예제 1: 웹 사이트 경고 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="c88fb-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="c88fb-111">이 명령은 웹 사이트 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="c88fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c88fb-112">PARAMETERS</span></span>

### <span data-ttu-id="c88fb-113">-Action</span><span class="sxs-lookup"><span data-stu-id="c88fb-113">-Action</span></span>
<span data-ttu-id="c88fb-114">콤마로 구분된 작업 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="c88fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88fb-115">-DefaultProfile</span></span>
<span data-ttu-id="c88fb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c88fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c88fb-117">-Description</span><span class="sxs-lookup"><span data-stu-id="c88fb-117">-Description</span></span>
<span data-ttu-id="c88fb-118">규칙에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="c88fb-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c88fb-119">-DisableRule</span></span>
<span data-ttu-id="c88fb-120">규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-120">Disables the rule.</span></span>
<span data-ttu-id="c88fb-121">이 매개 변수를 지정하지 않으면 규칙이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="c88fb-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="c88fb-122">-FailedLocationCount</span></span>
<span data-ttu-id="c88fb-123">웹 사이트 규칙에 대해 실패한 위치 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="c88fb-124">다른 유형의 규칙에서 임계값과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88fb-125">-Location</span><span class="sxs-lookup"><span data-stu-id="c88fb-125">-Location</span></span>
<span data-ttu-id="c88fb-126">규칙이 정의된 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="c88fb-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c88fb-127">-MetricName</span></span>
<span data-ttu-id="c88fb-128">메트릭의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="c88fb-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c88fb-129">-MetricNamespace</span></span>
<span data-ttu-id="c88fb-130">규칙에 대한 메트릭 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="c88fb-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c88fb-131">-Name</span></span>
<span data-ttu-id="c88fb-132">규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="c88fb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88fb-133">-ResourceGroupName</span></span>
<span data-ttu-id="c88fb-134">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c88fb-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="c88fb-135">-TargetResourceUri</span></span>
<span data-ttu-id="c88fb-136">웹게스트의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="c88fb-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="c88fb-137">-WindowSize</span></span>
<span data-ttu-id="c88fb-138">해당 데이터를 계산하는 규칙의 기간 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="c88fb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c88fb-139">-Confirm</span></span>
<span data-ttu-id="c88fb-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88fb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88fb-141">-WhatIf</span></span>
<span data-ttu-id="c88fb-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c88fb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c88fb-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88fb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88fb-144">CommonParameters</span></span>
<span data-ttu-id="c88fb-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c88fb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88fb-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c88fb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88fb-147">입력</span><span class="sxs-lookup"><span data-stu-id="c88fb-147">INPUTS</span></span>

### <span data-ttu-id="c88fb-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c88fb-148">System.String</span></span>

### <span data-ttu-id="c88fb-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c88fb-149">System.TimeSpan</span></span>

### <span data-ttu-id="c88fb-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c88fb-150">System.Int32</span></span>

### <span data-ttu-id="c88fb-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c88fb-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c88fb-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c88fb-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c88fb-153">출력</span><span class="sxs-lookup"><span data-stu-id="c88fb-153">OUTPUTS</span></span>

### <span data-ttu-id="c88fb-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c88fb-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="c88fb-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c88fb-155">NOTES</span></span>

## <span data-ttu-id="c88fb-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c88fb-156">RELATED LINKS</span></span>

[<span data-ttu-id="c88fb-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c88fb-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c88fb-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c88fb-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="c88fb-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c88fb-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="c88fb-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c88fb-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


