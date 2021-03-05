---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: eefcebbcf1544205fd37201574ed0c3394123bcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960432"
---
# <span data-ttu-id="71ea9-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71ea9-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="71ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="71ea9-103">로그 경고 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="71ea9-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="71ea9-104">구문</span><span class="sxs-lookup"><span data-stu-id="71ea9-104">SYNTAX</span></span>

### <span data-ttu-id="71ea9-105">ByRuleName(기본값)</span><span class="sxs-lookup"><span data-stu-id="71ea9-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ea9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71ea9-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ea9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71ea9-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ea9-108">설명</span><span class="sxs-lookup"><span data-stu-id="71ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="71ea9-109">PUT 시맨틱에 따라 로그 경고 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="71ea9-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="71ea9-110">예제</span><span class="sxs-lookup"><span data-stu-id="71ea9-110">EXAMPLES</span></span>

### <span data-ttu-id="71ea9-111">예제 1: 규칙 이름으로 설정</span><span class="sxs-lookup"><span data-stu-id="71ea9-111">Example 1: Set by rule name</span></span>
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

### <span data-ttu-id="71ea9-112">예제 2: 입력 개체로 설정</span><span class="sxs-lookup"><span data-stu-id="71ea9-112">Example 2: Set by Input Object</span></span>
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

### <span data-ttu-id="71ea9-113">예제 3: 리소스 ID로 설정</span><span class="sxs-lookup"><span data-stu-id="71ea9-113">Example 3: Set by resource Id</span></span>
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

## <span data-ttu-id="71ea9-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71ea9-114">PARAMETERS</span></span>

### <span data-ttu-id="71ea9-115">-Action</span><span class="sxs-lookup"><span data-stu-id="71ea9-115">-Action</span></span>
<span data-ttu-id="71ea9-116">예약된 쿼리 규칙 경고 작업</span><span class="sxs-lookup"><span data-stu-id="71ea9-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="71ea9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71ea9-117">-AsJob</span></span>
<span data-ttu-id="71ea9-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="71ea9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71ea9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ea9-119">-DefaultProfile</span></span>
<span data-ttu-id="71ea9-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71ea9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71ea9-121">-Description</span><span class="sxs-lookup"><span data-stu-id="71ea9-121">-Description</span></span>
<span data-ttu-id="71ea9-122">이 경고에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="71ea9-122">The description for this alert</span></span>

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

### <span data-ttu-id="71ea9-123">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="71ea9-123">-Enabled</span></span>
<span data-ttu-id="71ea9-124">Azure 경고 상태 - 유효한 값 - $true $false</span><span class="sxs-lookup"><span data-stu-id="71ea9-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="71ea9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71ea9-125">-InputObject</span></span>
<span data-ttu-id="71ea9-126">예약된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="71ea9-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="71ea9-127">-Location</span><span class="sxs-lookup"><span data-stu-id="71ea9-127">-Location</span></span>
<span data-ttu-id="71ea9-128">이 경고의 위치</span><span class="sxs-lookup"><span data-stu-id="71ea9-128">The location for this alert</span></span>

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

### <span data-ttu-id="71ea9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="71ea9-129">-Name</span></span>
<span data-ttu-id="71ea9-130">경고 이름</span><span class="sxs-lookup"><span data-stu-id="71ea9-130">The alert name</span></span>

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

### <span data-ttu-id="71ea9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ea9-131">-ResourceGroupName</span></span>
<span data-ttu-id="71ea9-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="71ea9-132">The resource group name</span></span>

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

### <span data-ttu-id="71ea9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71ea9-133">-ResourceId</span></span>
<span data-ttu-id="71ea9-134">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="71ea9-134">The resource Id</span></span>

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

### <span data-ttu-id="71ea9-135">-Schedule</span><span class="sxs-lookup"><span data-stu-id="71ea9-135">-Schedule</span></span>
<span data-ttu-id="71ea9-136">예약된 쿼리 규칙 일정</span><span class="sxs-lookup"><span data-stu-id="71ea9-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="71ea9-137">-Source</span><span class="sxs-lookup"><span data-stu-id="71ea9-137">-Source</span></span>
<span data-ttu-id="71ea9-138">예약된 쿼리 규칙 원본</span><span class="sxs-lookup"><span data-stu-id="71ea9-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="71ea9-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="71ea9-139">-Tag</span></span>
<span data-ttu-id="71ea9-140">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="71ea9-140">Resource tags</span></span>

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

### <span data-ttu-id="71ea9-141">-확인</span><span class="sxs-lookup"><span data-stu-id="71ea9-141">-Confirm</span></span>
<span data-ttu-id="71ea9-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71ea9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ea9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ea9-143">-WhatIf</span></span>
<span data-ttu-id="71ea9-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71ea9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ea9-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71ea9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ea9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ea9-146">CommonParameters</span></span>
<span data-ttu-id="71ea9-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71ea9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ea9-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71ea9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ea9-149">입력</span><span class="sxs-lookup"><span data-stu-id="71ea9-149">INPUTS</span></span>

### <span data-ttu-id="71ea9-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="71ea9-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="71ea9-151">System.String</span><span class="sxs-lookup"><span data-stu-id="71ea9-151">System.String</span></span>

### <span data-ttu-id="71ea9-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="71ea9-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="71ea9-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="71ea9-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="71ea9-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="71ea9-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="71ea9-155">출력</span><span class="sxs-lookup"><span data-stu-id="71ea9-155">OUTPUTS</span></span>

### <span data-ttu-id="71ea9-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="71ea9-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="71ea9-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71ea9-157">NOTES</span></span>

## <span data-ttu-id="71ea9-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71ea9-158">RELATED LINKS</span></span>
