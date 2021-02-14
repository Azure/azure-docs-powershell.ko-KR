---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201761"
---
# <span data-ttu-id="500d8-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="500d8-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="500d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500d8-102">SYNOPSIS</span></span>
<span data-ttu-id="500d8-103">분석(경고 규칙)을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="500d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="500d8-104">SYNTAX</span></span>

### <span data-ttu-id="500d8-105">ScheduledAlertRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="500d8-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500d8-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="500d8-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="500d8-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="500d8-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500d8-108">설명</span><span class="sxs-lookup"><span data-stu-id="500d8-108">DESCRIPTION</span></span>
<span data-ttu-id="500d8-109">**New-AzSentinelAlertRule** cmdlet은 지정된 작업 영역의 분석(경고 규칙)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="500d8-110">만들 경고 규칙의 종류를 지정하려면 *Fusion,* *Scheduled* 또는 *MicrosoftSecurityIncidentCreation의* 세 매개 변수 중 하나를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="500d8-111">각 종류에는 서로 다른 필수 패러마스터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="500d8-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="500d8-113">예제</span><span class="sxs-lookup"><span data-stu-id="500d8-113">EXAMPLES</span></span>

### <span data-ttu-id="500d8-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="500d8-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="500d8-115">이 예제에서는 고급 *Multistage* 공격 탐지용 템플릿을 기반으로 *Fusion* 종류의 **AlertRule을** 만든 다음 $AlertRule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="500d8-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="500d8-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="500d8-117">이 예제에서는 *IoT용 Azure Security Center* 경고를 기반으로 인시던트 만들기 템플릿을 기반으로 *MicrosoftSecurityIncidentCreation* 종류의 **AlertRule을** 만든 다음, 새 경고에 $AlertRule 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="500d8-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="500d8-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="500d8-119">이 예제에서는 예약된 종류의  **DataConnector를** 만든 다음, $AlertRule 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="500d8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500d8-120">PARAMETERS</span></span>

### <span data-ttu-id="500d8-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="500d8-121">-AlertRuleId</span></span>
<span data-ttu-id="500d8-122">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="500d8-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="500d8-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="500d8-124">경고 규칙 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500d8-125">-DefaultProfile</span></span>
<span data-ttu-id="500d8-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500d8-127">-Description</span><span class="sxs-lookup"><span data-stu-id="500d8-127">-Description</span></span>
<span data-ttu-id="500d8-128">설명입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="500d8-129">-DisplayName</span></span>
<span data-ttu-id="500d8-130">경고 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="500d8-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="500d8-132">경고 규칙 표시 이름은 필터를 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="500d8-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="500d8-134">경고 규칙 표시 이름 필터.</span><span class="sxs-lookup"><span data-stu-id="500d8-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="500d8-135">-Enabled</span></span>
<span data-ttu-id="500d8-136">경고 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="500d8-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="500d8-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="500d8-137">-Fusion</span></span>
<span data-ttu-id="500d8-138">경고 규칙 종류.</span><span class="sxs-lookup"><span data-stu-id="500d8-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="500d8-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="500d8-140">경고 규칙 종류.</span><span class="sxs-lookup"><span data-stu-id="500d8-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="500d8-141">-ProductFilter</span></span>
<span data-ttu-id="500d8-142">경고 규칙 제품 필터.</span><span class="sxs-lookup"><span data-stu-id="500d8-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-143">-Query</span><span class="sxs-lookup"><span data-stu-id="500d8-143">-Query</span></span>
<span data-ttu-id="500d8-144">경고 규칙 쿼리.</span><span class="sxs-lookup"><span data-stu-id="500d8-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="500d8-145">-QueryFrequency</span></span>
<span data-ttu-id="500d8-146">경고 규칙 쿼리 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="500d8-147">-QueryPeriod</span></span>
<span data-ttu-id="500d8-148">경고 규칙 쿼리 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500d8-149">-ResourceGroupName</span></span>
<span data-ttu-id="500d8-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-151">-Scheduled</span><span class="sxs-lookup"><span data-stu-id="500d8-151">-Scheduled</span></span>
<span data-ttu-id="500d8-152">경고 규칙 종류.</span><span class="sxs-lookup"><span data-stu-id="500d8-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="500d8-153">-SeveritiesFilter</span></span>
<span data-ttu-id="500d8-154">경고 규칙 심각도 필터.</span><span class="sxs-lookup"><span data-stu-id="500d8-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-155">-심각도</span><span class="sxs-lookup"><span data-stu-id="500d8-155">-Severity</span></span>
<span data-ttu-id="500d8-156">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="500d8-157">-SuppressionDuration</span></span>
<span data-ttu-id="500d8-158">경고 규칙 표시 안 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="500d8-159">-SuppressionEnabled</span></span>
<span data-ttu-id="500d8-160">경고 규칙 표시 안 을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-161">-전술</span><span class="sxs-lookup"><span data-stu-id="500d8-161">-Tactics</span></span>
<span data-ttu-id="500d8-162">경고 규칙 전술.</span><span class="sxs-lookup"><span data-stu-id="500d8-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="500d8-163">-TriggerOperator</span></span>
<span data-ttu-id="500d8-164">경고 규칙 트리거 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="500d8-165">-TriggerThreshold</span></span>
<span data-ttu-id="500d8-166">경고 규칙 트리거 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="500d8-167">-WorkspaceName</span></span>
<span data-ttu-id="500d8-168">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-168">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500d8-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="500d8-169">-Confirm</span></span>
<span data-ttu-id="500d8-170">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500d8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500d8-171">-WhatIf</span></span>
<span data-ttu-id="500d8-172">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="500d8-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="500d8-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500d8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500d8-174">CommonParameters</span></span>
<span data-ttu-id="500d8-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="500d8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500d8-176">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="500d8-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500d8-177">입력</span><span class="sxs-lookup"><span data-stu-id="500d8-177">INPUTS</span></span>

### <span data-ttu-id="500d8-178">없음</span><span class="sxs-lookup"><span data-stu-id="500d8-178">None</span></span>
## <span data-ttu-id="500d8-179">출력</span><span class="sxs-lookup"><span data-stu-id="500d8-179">OUTPUTS</span></span>

### <span data-ttu-id="500d8-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="500d8-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="500d8-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="500d8-181">NOTES</span></span>

## <span data-ttu-id="500d8-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="500d8-182">RELATED LINKS</span></span>
