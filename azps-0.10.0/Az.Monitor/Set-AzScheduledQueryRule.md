---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 5a1ae00f13494c73c6e27aa6aeeeda391d17a512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875710"
---
# <span data-ttu-id="1478e-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1478e-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="1478e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1478e-102">SYNOPSIS</span></span>
<span data-ttu-id="1478e-103">로그 알림 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="1478e-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="1478e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1478e-104">SYNTAX</span></span>

### <span data-ttu-id="1478e-105">ByRuleName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1478e-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1478e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1478e-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1478e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1478e-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1478e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1478e-108">DESCRIPTION</span></span>
<span data-ttu-id="1478e-109">의미를 포함 하 여 로그 알림 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="1478e-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="1478e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1478e-110">EXAMPLES</span></span>

### <span data-ttu-id="1478e-111">예제 1-규칙 이름별로 설정</span><span class="sxs-lookup"><span data-stu-id="1478e-111">Example 1 - Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="1478e-112">예제 2-입력 개체에 의해 설정</span><span class="sxs-lookup"><span data-stu-id="1478e-112">Example 2 - Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="1478e-113">예제 3-리소스 Id로 설정</span><span class="sxs-lookup"><span data-stu-id="1478e-113">Example 3 - Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="1478e-114">변수</span><span class="sxs-lookup"><span data-stu-id="1478e-114">PARAMETERS</span></span>

### <span data-ttu-id="1478e-115">-작업</span><span class="sxs-lookup"><span data-stu-id="1478e-115">-Action</span></span>
<span data-ttu-id="1478e-116">예약 된 쿼리 규칙 경고 동작</span><span class="sxs-lookup"><span data-stu-id="1478e-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1478e-117">-AsJob</span></span>
<span data-ttu-id="1478e-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1478e-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1478e-119">-DefaultProfile</span></span>
<span data-ttu-id="1478e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1478e-121">-설명</span><span class="sxs-lookup"><span data-stu-id="1478e-121">-Description</span></span>
<span data-ttu-id="1478e-122">이 경고에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="1478e-122">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-123">-사용</span><span class="sxs-lookup"><span data-stu-id="1478e-123">-Enabled</span></span>
<span data-ttu-id="1478e-124">Azure alert state-유효한 값-$true, $false</span><span class="sxs-lookup"><span data-stu-id="1478e-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1478e-125">-InputObject</span></span>
<span data-ttu-id="1478e-126">예약 된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="1478e-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-127">-위치</span><span class="sxs-lookup"><span data-stu-id="1478e-127">-Location</span></span>
<span data-ttu-id="1478e-128">이 알림의 위치</span><span class="sxs-lookup"><span data-stu-id="1478e-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-129">-이름</span><span class="sxs-lookup"><span data-stu-id="1478e-129">-Name</span></span>
<span data-ttu-id="1478e-130">알림 이름</span><span class="sxs-lookup"><span data-stu-id="1478e-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1478e-131">-ResourceGroupName</span></span>
<span data-ttu-id="1478e-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1478e-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1478e-133">-ResourceId</span></span>
<span data-ttu-id="1478e-134">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="1478e-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-135">-일정</span><span class="sxs-lookup"><span data-stu-id="1478e-135">-Schedule</span></span>
<span data-ttu-id="1478e-136">예약 된 쿼리 규칙 일정</span><span class="sxs-lookup"><span data-stu-id="1478e-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-137">-원본</span><span class="sxs-lookup"><span data-stu-id="1478e-137">-Source</span></span>
<span data-ttu-id="1478e-138">예약 된 쿼리 규칙 원본</span><span class="sxs-lookup"><span data-stu-id="1478e-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-139">태그</span><span class="sxs-lookup"><span data-stu-id="1478e-139">-Tag</span></span>
<span data-ttu-id="1478e-140">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="1478e-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1478e-141">-확인</span><span class="sxs-lookup"><span data-stu-id="1478e-141">-Confirm</span></span>
<span data-ttu-id="1478e-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1478e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1478e-143">-WhatIf</span></span>
<span data-ttu-id="1478e-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1478e-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1478e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1478e-146">CommonParameters</span></span>
<span data-ttu-id="1478e-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1478e-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1478e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1478e-149">입력</span><span class="sxs-lookup"><span data-stu-id="1478e-149">INPUTS</span></span>

### <span data-ttu-id="1478e-150">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="1478e-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1478e-151">System.String</span></span>

### <span data-ttu-id="1478e-152">PSScheduledQueryRuleSource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="1478e-153">PSScheduledQueryRuleSchedule를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="1478e-154">PSScheduledQueryRuleAlertingAction를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="1478e-155">출력</span><span class="sxs-lookup"><span data-stu-id="1478e-155">OUTPUTS</span></span>

### <span data-ttu-id="1478e-156">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1478e-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="1478e-157">상속자</span><span class="sxs-lookup"><span data-stu-id="1478e-157">NOTES</span></span>

## <span data-ttu-id="1478e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1478e-158">RELATED LINKS</span></span>
