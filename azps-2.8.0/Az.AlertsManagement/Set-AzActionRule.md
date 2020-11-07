---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698179"
---
# <span data-ttu-id="a4d95-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="a4d95-101">Set-AzActionRule</span></span>

## <span data-ttu-id="a4d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d95-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d95-103">작업 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-103">Create or update an action rule.</span></span>

## <span data-ttu-id="a4d95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4d95-104">SYNTAX</span></span>

### <span data-ttu-id="a4d95-105">BySimplifiedFormatDiagnosticsActionRule (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4d95-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d95-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4d95-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4d95-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="a4d95-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d95-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="a4d95-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d95-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a4d95-109">DESCRIPTION</span></span>
<span data-ttu-id="a4d95-110">**Set-AzActionRule** 작업 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="a4d95-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a4d95-111">EXAMPLES</span></span>

### <span data-ttu-id="a4d95-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4d95-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="a4d95-113">이 cmdlet은 supression에 대 한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="a4d95-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a4d95-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="a4d95-115">이 cmdlet은 작업 그룹에 대 한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="a4d95-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="a4d95-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="a4d95-117">이 cmdlet은 진단 설정에 대 한 작업 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="a4d95-118">변수</span><span class="sxs-lookup"><span data-stu-id="a4d95-118">PARAMETERS</span></span>

### <span data-ttu-id="a4d95-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="a4d95-119">-ActionGroupId</span></span>
<span data-ttu-id="a4d95-120">알림을 받을 작업 그룹 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="a4d95-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="a4d95-121">-ActionRuleType</span></span>
<span data-ttu-id="a4d95-122">작업 규칙 Json 형식</span><span class="sxs-lookup"><span data-stu-id="a4d95-122">Action rule Json format</span></span>

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

### <span data-ttu-id="a4d95-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-123">-AlertContextCondition</span></span>
<span data-ttu-id="a4d95-124">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-125">포함: smartgroups</span><span class="sxs-lookup"><span data-stu-id="a4d95-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="a4d95-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="a4d95-127">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-128">Equals:/구독/ad825170-845c-47db-8f00-11978947b089/resourceGroups/metricAlerts/제공자/공급자/microsoft-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="a4d95-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="a4d95-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d95-129">-DefaultProfile</span></span>
<span data-ttu-id="a4d95-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d95-131">-설명</span><span class="sxs-lookup"><span data-stu-id="a4d95-131">-Description</span></span>
<span data-ttu-id="a4d95-132">작업 규칙 설명</span><span class="sxs-lookup"><span data-stu-id="a4d95-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="a4d95-133">-설명 조건</span><span class="sxs-lookup"><span data-stu-id="a4d95-133">-DescriptionCondition</span></span>
<span data-ttu-id="a4d95-134">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-135">포함: 테스트 알림</span><span class="sxs-lookup"><span data-stu-id="a4d95-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="a4d95-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4d95-136">-InputObject</span></span>
<span data-ttu-id="a4d95-137">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="a4d95-137">The action rule resource</span></span>

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

### <span data-ttu-id="a4d95-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-138">-MonitorCondition</span></span>
<span data-ttu-id="a4d95-139">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-140">참고: 해결 됨</span><span class="sxs-lookup"><span data-stu-id="a4d95-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="a4d95-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="a4d95-142">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-143">같음: 플랫폼, 로그 분석</span><span class="sxs-lookup"><span data-stu-id="a4d95-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="a4d95-144">-이름</span><span class="sxs-lookup"><span data-stu-id="a4d95-144">-Name</span></span>
<span data-ttu-id="a4d95-145">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="a4d95-145">Action rule Name</span></span>

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

### <span data-ttu-id="a4d95-146">-로이 Etype</span><span class="sxs-lookup"><span data-stu-id="a4d95-146">-ReccurenceType</span></span>
<span data-ttu-id="a4d95-147">억제를 적용 해야 하는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="a4d95-148">-값</span><span class="sxs-lookup"><span data-stu-id="a4d95-148">-ReccurentValue</span></span>
<span data-ttu-id="a4d95-149">해당 하는 경우 Reccurent 값입니다. \[월간-1, \] \[ 3, 5, 30의 경우 2\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="a4d95-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d95-150">-ResourceGroupName</span></span>
<span data-ttu-id="a4d95-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a4d95-151">Resource Group Name</span></span>

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

### <span data-ttu-id="a4d95-152">-범위</span><span class="sxs-lookup"><span data-stu-id="a4d95-152">-Scope</span></span>
<span data-ttu-id="a4d95-153">쉼표로 구분 된 값 목록</span><span class="sxs-lookup"><span data-stu-id="a4d95-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="a4d95-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-154">-SeverityCondition</span></span>
<span data-ttu-id="a4d95-155">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-156">Equals: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="a4d95-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="a4d95-157">-상태</span><span class="sxs-lookup"><span data-stu-id="a4d95-157">-Status</span></span>
<span data-ttu-id="a4d95-158">작업 규칙의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="a4d95-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="a4d95-159">-SuppressionEndTime</span></span>
<span data-ttu-id="a4d95-160">억제 종료 시간.</span><span class="sxs-lookup"><span data-stu-id="a4d95-160">Suppression End Time.</span></span>
<span data-ttu-id="a4d95-161">12/09/2018 06:00:00 + Reccurent Supression에서는 한 번, 매일, 매주 또는 매월 중에서 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="a4d95-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="a4d95-162">-SuppressionStartTime</span></span>
<span data-ttu-id="a4d95-163">비 표시 시작 시간.</span><span class="sxs-lookup"><span data-stu-id="a4d95-163">Suppression Start Time.</span></span>
<span data-ttu-id="a4d95-164">12/09/2018 06:00:00 + Reccurent Supression에서는 한 번, 매일, 매주 또는 매월 중에서 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="a4d95-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="a4d95-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="a4d95-166">필요한 형식-{ \< 연산 \> : \< 쉼표로 구분 된 값 목록 \> } 예를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="a4d95-167">포함: 가상 컴퓨터, 저장소 계정</span><span class="sxs-lookup"><span data-stu-id="a4d95-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="a4d95-168">-확인</span><span class="sxs-lookup"><span data-stu-id="a4d95-168">-Confirm</span></span>
<span data-ttu-id="a4d95-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d95-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d95-170">-WhatIf</span></span>
<span data-ttu-id="a4d95-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4d95-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d95-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d95-173">CommonParameters</span></span>
<span data-ttu-id="a4d95-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d95-175">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4d95-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d95-176">입력</span><span class="sxs-lookup"><span data-stu-id="a4d95-176">INPUTS</span></span>

### <span data-ttu-id="a4d95-177">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="a4d95-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="a4d95-178">출력</span><span class="sxs-lookup"><span data-stu-id="a4d95-178">OUTPUTS</span></span>

### <span data-ttu-id="a4d95-179">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="a4d95-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="a4d95-180">상속자</span><span class="sxs-lookup"><span data-stu-id="a4d95-180">NOTES</span></span>

## <span data-ttu-id="a4d95-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4d95-181">RELATED LINKS</span></span>
