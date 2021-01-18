---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494529"
---
# <span data-ttu-id="62575-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="62575-101">Set-AzActionRule</span></span>

## <span data-ttu-id="62575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62575-102">SYNOPSIS</span></span>
<span data-ttu-id="62575-103">작업 규칙을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-103">Create or update an action rule.</span></span>

## <span data-ttu-id="62575-104">구문</span><span class="sxs-lookup"><span data-stu-id="62575-104">SYNTAX</span></span>

### <span data-ttu-id="62575-105">BySimplifiedFormatDiagnosticsActionRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="62575-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62575-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="62575-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62575-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="62575-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62575-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="62575-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62575-109">설명</span><span class="sxs-lookup"><span data-stu-id="62575-109">DESCRIPTION</span></span>
<span data-ttu-id="62575-110">**Set-AzActionRule은** 작업 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="62575-111">예제</span><span class="sxs-lookup"><span data-stu-id="62575-111">EXAMPLES</span></span>

### <span data-ttu-id="62575-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="62575-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="62575-113">이 cmdlet은 구독 범위를 통해 압축에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62575-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="62575-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="62575-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="62575-115">이 cmdlet은 리소스 그룹 범위 목록을 통해 작업 그룹에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62575-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="62575-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="62575-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="62575-117">이 cmdlet은 리소스 범위를 사용하여 진단 설정에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62575-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="62575-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62575-118">PARAMETERS</span></span>

### <span data-ttu-id="62575-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="62575-119">-ActionGroupId</span></span>
<span data-ttu-id="62575-120">알림을 하게 될 작업 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="62575-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="62575-121">-ActionRuleType</span></span>
<span data-ttu-id="62575-122">작업 규칙 Json 형식</span><span class="sxs-lookup"><span data-stu-id="62575-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="62575-123">-AlertContextCondition</span></span>
<span data-ttu-id="62575-124">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-125">Contains:smartgroups</span><span class="sxs-lookup"><span data-stu-id="62575-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="62575-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="62575-127">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="62575-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62575-129">-DefaultProfile</span></span>
<span data-ttu-id="62575-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62575-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62575-131">-Description</span><span class="sxs-lookup"><span data-stu-id="62575-131">-Description</span></span>
<span data-ttu-id="62575-132">작업 규칙 설명</span><span class="sxs-lookup"><span data-stu-id="62575-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="62575-133">-DescriptionCondition</span></span>
<span data-ttu-id="62575-134">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-135">포함:테스트 경고</span><span class="sxs-lookup"><span data-stu-id="62575-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62575-136">-InputObject</span></span>
<span data-ttu-id="62575-137">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="62575-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62575-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="62575-138">-MonitorCondition</span></span>
<span data-ttu-id="62575-139">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="62575-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="62575-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="62575-142">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-143">Equals:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="62575-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-144">-Name</span><span class="sxs-lookup"><span data-stu-id="62575-144">-Name</span></span>
<span data-ttu-id="62575-145">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="62575-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="62575-146">-ReccurenceType</span></span>
<span data-ttu-id="62575-147">표시 안 을 적용해야 하는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="62575-148">-ReccurentValue</span></span>
<span data-ttu-id="62575-149">해당하는 경우 재시도 값입니다. 매주의 경우 - \[ 1,2 월 - \] \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="62575-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62575-150">-ResourceGroupName</span></span>
<span data-ttu-id="62575-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="62575-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="62575-152">-Scope</span></span>
<span data-ttu-id="62575-153">콤마로 구분된 값 목록</span><span class="sxs-lookup"><span data-stu-id="62575-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="62575-154">-SeverityCondition</span></span>
<span data-ttu-id="62575-155">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-156">같음:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="62575-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-157">-Status</span><span class="sxs-lookup"><span data-stu-id="62575-157">-Status</span></span>
<span data-ttu-id="62575-158">작업 규칙의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="62575-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="62575-159">-SuppressionEndTime</span></span>
<span data-ttu-id="62575-160">표시 안 압정 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="62575-160">Suppression End Time.</span></span>
<span data-ttu-id="62575-161">형식 12/09/2018 06:00:00 +재발성 압축 일정의 경우 한 번, 매일, 매주 또는 매월 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="62575-162">-SuppressionStartTime</span></span>
<span data-ttu-id="62575-163">표시 안 하다 시작 시간.</span><span class="sxs-lookup"><span data-stu-id="62575-163">Suppression Start Time.</span></span>
<span data-ttu-id="62575-164">형식 12/09/2018 06:00:00 +재발성 압축 일정의 경우 한 번, 매일, 매주 또는 매월 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="62575-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="62575-166">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예:</span><span class="sxs-lookup"><span data-stu-id="62575-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="62575-167">포함:Virtual Machines, Storage 계정</span><span class="sxs-lookup"><span data-stu-id="62575-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62575-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62575-168">-Confirm</span></span>
<span data-ttu-id="62575-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62575-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62575-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62575-170">-WhatIf</span></span>
<span data-ttu-id="62575-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="62575-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62575-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62575-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62575-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62575-173">CommonParameters</span></span>
<span data-ttu-id="62575-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62575-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62575-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62575-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62575-176">입력</span><span class="sxs-lookup"><span data-stu-id="62575-176">INPUTS</span></span>

### <span data-ttu-id="62575-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="62575-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="62575-178">출력</span><span class="sxs-lookup"><span data-stu-id="62575-178">OUTPUTS</span></span>

### <span data-ttu-id="62575-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="62575-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="62575-180">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62575-180">NOTES</span></span>

## <span data-ttu-id="62575-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62575-181">RELATED LINKS</span></span>
