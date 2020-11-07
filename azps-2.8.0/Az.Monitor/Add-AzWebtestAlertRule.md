---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: e67fa6bd5f69a727493805fa21f4cbfa776af436
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689332"
---
# <span data-ttu-id="cfbb7-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cfbb7-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="cfbb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbb7-103">Webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="cfbb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cfbb7-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfbb7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cfbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="cfbb7-106">**AzWebtestAlertRule** cmdlet은 메트릭, 이벤트 또는 webtest 유형의 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="cfbb7-107">추가한 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="cfbb7-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cfbb7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cfbb7-109">EXAMPLES</span></span>

### <span data-ttu-id="cfbb7-110">예제 1: webtest 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="cfbb7-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="cfbb7-111">이 명령은 webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="cfbb7-112">변수</span><span class="sxs-lookup"><span data-stu-id="cfbb7-112">PARAMETERS</span></span>

### <span data-ttu-id="cfbb7-113">-작업</span><span class="sxs-lookup"><span data-stu-id="cfbb7-113">-Action</span></span>
<span data-ttu-id="cfbb7-114">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="cfbb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbb7-115">-DefaultProfile</span></span>
<span data-ttu-id="cfbb7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cfbb7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfbb7-117">-설명</span><span class="sxs-lookup"><span data-stu-id="cfbb7-117">-Description</span></span>
<span data-ttu-id="cfbb7-118">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="cfbb7-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="cfbb7-119">-DisableRule</span></span>
<span data-ttu-id="cfbb7-120">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-120">Disables the rule.</span></span>
<span data-ttu-id="cfbb7-121">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="cfbb7-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="cfbb7-122">-FailedLocationCount</span></span>
<span data-ttu-id="cfbb7-123">Webtest 규칙의 실패 한 위치 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="cfbb7-124">이는 다른 유형의 규칙에 있는 임계값과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="cfbb7-125">-위치</span><span class="sxs-lookup"><span data-stu-id="cfbb7-125">-Location</span></span>
<span data-ttu-id="cfbb7-126">규칙이 정의 된 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="cfbb7-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="cfbb7-127">-MetricName</span></span>
<span data-ttu-id="cfbb7-128">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="cfbb7-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="cfbb7-129">-MetricNamespace</span></span>
<span data-ttu-id="cfbb7-130">규칙에 대 한 메트릭 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="cfbb7-131">-이름</span><span class="sxs-lookup"><span data-stu-id="cfbb7-131">-Name</span></span>
<span data-ttu-id="cfbb7-132">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="cfbb7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfbb7-133">-ResourceGroupName</span></span>
<span data-ttu-id="cfbb7-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cfbb7-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="cfbb7-135">-TargetResourceUri</span></span>
<span data-ttu-id="cfbb7-136">Webtest의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="cfbb7-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="cfbb7-137">-WindowSize</span></span>
<span data-ttu-id="cfbb7-138">해당 데이터를 계산 하는 규칙의 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="cfbb7-139">-확인</span><span class="sxs-lookup"><span data-stu-id="cfbb7-139">-Confirm</span></span>
<span data-ttu-id="cfbb7-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfbb7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfbb7-141">-WhatIf</span></span>
<span data-ttu-id="cfbb7-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfbb7-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfbb7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbb7-144">CommonParameters</span></span>
<span data-ttu-id="cfbb7-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbb7-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbb7-147">입력</span><span class="sxs-lookup"><span data-stu-id="cfbb7-147">INPUTS</span></span>

### <span data-ttu-id="cfbb7-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cfbb7-148">System.String</span></span>

### <span data-ttu-id="cfbb7-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="cfbb7-149">System.TimeSpan</span></span>

### <span data-ttu-id="cfbb7-150">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-150">System.Int32</span></span>

### <span data-ttu-id="cfbb7-151">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cfbb7-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cfbb7-152">System.webserver. List ' 1 [[Microsoft. t e;. \*. \*. \*. \*. \*. \*. \*. e 1.. i t = 1.0.0.0, Culture = 중립, PublicKeyToken = null])</span><span class="sxs-lookup"><span data-stu-id="cfbb7-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cfbb7-153">출력</span><span class="sxs-lookup"><span data-stu-id="cfbb7-153">OUTPUTS</span></span>

### <span data-ttu-id="cfbb7-154">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbb7-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="cfbb7-155">상속자</span><span class="sxs-lookup"><span data-stu-id="cfbb7-155">NOTES</span></span>

## <span data-ttu-id="cfbb7-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfbb7-156">RELATED LINKS</span></span>

[<span data-ttu-id="cfbb7-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cfbb7-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="cfbb7-158">추가-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cfbb7-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="cfbb7-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cfbb7-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="cfbb7-160">새로운 AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="cfbb7-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


