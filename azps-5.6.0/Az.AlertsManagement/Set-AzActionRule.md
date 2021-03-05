---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 65d402f06770542265bd9b0a6e9e50cd943114f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015595"
---
# <span data-ttu-id="2a2a8-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="2a2a8-101">Set-AzActionRule</span></span>

## <span data-ttu-id="2a2a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2a8-103">작업 규칙을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-103">Create or update an action rule.</span></span>

## <span data-ttu-id="2a2a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a2a8-104">SYNTAX</span></span>

### <span data-ttu-id="2a2a8-105">BySimplifiedFormatDiagnosticsActionRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="2a2a8-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a2a8-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2a8-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="2a2a8-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2a8-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="2a2a8-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a2a8-109">설명</span><span class="sxs-lookup"><span data-stu-id="2a2a8-109">DESCRIPTION</span></span>
<span data-ttu-id="2a2a8-110">**Set-AzActionRule은** 작업 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="2a2a8-111">예제</span><span class="sxs-lookup"><span data-stu-id="2a2a8-111">EXAMPLES</span></span>

### <span data-ttu-id="2a2a8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a2a8-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="2a2a8-113">이 cmdlet은 구독 범위와 함께 supression에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="2a2a8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="2a2a8-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="2a2a8-115">이 cmdlet은 리소스 그룹 범위 목록과 함께 작업 그룹에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="2a2a8-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="2a2a8-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="2a2a8-117">이 cmdlet은 리소스 범위와 함께 진단 설정에 대한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="2a2a8-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2a2a8-118">PARAMETERS</span></span>

### <span data-ttu-id="2a2a8-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="2a2a8-119">-ActionGroupId</span></span>
<span data-ttu-id="2a2a8-120">알림을 하게 될 작업 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="2a2a8-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="2a2a8-121">-ActionRuleType</span></span>
<span data-ttu-id="2a2a8-122">작업 규칙 Json 형식</span><span class="sxs-lookup"><span data-stu-id="2a2a8-122">Action rule Json format</span></span>

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

### <span data-ttu-id="2a2a8-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-123">-AlertContextCondition</span></span>
<span data-ttu-id="2a2a8-124">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-125">Contains:smartgroups</span><span class="sxs-lookup"><span data-stu-id="2a2a8-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="2a2a8-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="2a2a8-127">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-128">Equals://subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="2a2a8-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="2a2a8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2a8-129">-DefaultProfile</span></span>
<span data-ttu-id="2a2a8-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2a8-131">-Description</span><span class="sxs-lookup"><span data-stu-id="2a2a8-131">-Description</span></span>
<span data-ttu-id="2a2a8-132">작업 규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="2a2a8-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="2a2a8-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-133">-DescriptionCondition</span></span>
<span data-ttu-id="2a2a8-134">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-135">내용:테스트 경고</span><span class="sxs-lookup"><span data-stu-id="2a2a8-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="2a2a8-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a2a8-136">-InputObject</span></span>
<span data-ttu-id="2a2a8-137">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="2a2a8-137">The action rule resource</span></span>

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

### <span data-ttu-id="2a2a8-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-138">-MonitorCondition</span></span>
<span data-ttu-id="2a2a8-139">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="2a2a8-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="2a2a8-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="2a2a8-142">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-143">Equals:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="2a2a8-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="2a2a8-144">-Name</span><span class="sxs-lookup"><span data-stu-id="2a2a8-144">-Name</span></span>
<span data-ttu-id="2a2a8-145">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="2a2a8-145">Action rule Name</span></span>

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

### <span data-ttu-id="2a2a8-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="2a2a8-146">-ReccurenceType</span></span>
<span data-ttu-id="2a2a8-147">억제를 적용해야 하는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="2a2a8-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="2a2a8-148">-ReccurentValue</span></span>
<span data-ttu-id="2a2a8-149">해당하는 경우 재시도 값입니다. 주간의 경우 - \[ 1,2 월간의 경우 \] - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="2a2a8-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="2a2a8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2a8-150">-ResourceGroupName</span></span>
<span data-ttu-id="2a2a8-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2a2a8-151">Resource Group Name</span></span>

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

### <span data-ttu-id="2a2a8-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="2a2a8-152">-Scope</span></span>
<span data-ttu-id="2a2a8-153">콤마로 구분된 값 목록</span><span class="sxs-lookup"><span data-stu-id="2a2a8-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="2a2a8-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-154">-SeverityCondition</span></span>
<span data-ttu-id="2a2a8-155">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-156">Equals:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="2a2a8-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="2a2a8-157">-Status</span><span class="sxs-lookup"><span data-stu-id="2a2a8-157">-Status</span></span>
<span data-ttu-id="2a2a8-158">작업 규칙의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="2a2a8-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="2a2a8-159">-SuppressionEndTime</span></span>
<span data-ttu-id="2a2a8-160">억제 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-160">Suppression End Time.</span></span>
<span data-ttu-id="2a2a8-161">2018년 12월 09일 06:00:00 +를 1회, 일, 매주 또는 매월 재발방지 일정의 경우 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="2a2a8-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="2a2a8-162">-SuppressionStartTime</span></span>
<span data-ttu-id="2a2a8-163">억제 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-163">Suppression Start Time.</span></span>
<span data-ttu-id="2a2a8-164">2018년 12월 09일 06:00:00 +를 1회, 일, 매주 또는 매월 재발방지 일정의 경우 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="2a2a8-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="2a2a8-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="2a2a8-166">예상 형식 - { \<operation\> : \<comma separated list of values\> } 예.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="2a2a8-167">포함:Virtual Machines, Storage 계정</span><span class="sxs-lookup"><span data-stu-id="2a2a8-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="2a2a8-168">-확인</span><span class="sxs-lookup"><span data-stu-id="2a2a8-168">-Confirm</span></span>
<span data-ttu-id="2a2a8-169">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2a8-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2a8-170">-WhatIf</span></span>
<span data-ttu-id="2a2a8-171">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a2a8-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2a8-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2a8-173">CommonParameters</span></span>
<span data-ttu-id="2a2a8-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2a8-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2a8-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a2a8-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2a8-176">입력</span><span class="sxs-lookup"><span data-stu-id="2a2a8-176">INPUTS</span></span>

### <span data-ttu-id="2a2a8-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2a2a8-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2a2a8-178">출력</span><span class="sxs-lookup"><span data-stu-id="2a2a8-178">OUTPUTS</span></span>

### <span data-ttu-id="2a2a8-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2a2a8-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2a2a8-180">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a2a8-180">NOTES</span></span>

## <span data-ttu-id="2a2a8-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a2a8-181">RELATED LINKS</span></span>
