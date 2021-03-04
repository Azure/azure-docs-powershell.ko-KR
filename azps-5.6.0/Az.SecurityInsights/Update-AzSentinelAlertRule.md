---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969883"
---
# <span data-ttu-id="81e8a-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="81e8a-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="81e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="81e8a-103">분석(경고 규칙)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="81e8a-104">구문</span><span class="sxs-lookup"><span data-stu-id="81e8a-104">SYNTAX</span></span>

### <span data-ttu-id="81e8a-105">AlertRuleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="81e8a-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e8a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="81e8a-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e8a-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e8a-108">설명</span><span class="sxs-lookup"><span data-stu-id="81e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="81e8a-109">**Update-AzSentinelAlertRule** cmdlet은 지정된 작업 영역의 분석(경고 규칙)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="81e8a-110">-InputObject 또는 -ResourceId 또는 -AlertId를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="81e8a-111">1개 이상의 프로퍼리 파마터를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="81e8a-112">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="81e8a-113">예제</span><span class="sxs-lookup"><span data-stu-id="81e8a-113">EXAMPLES</span></span>

### <span data-ttu-id="81e8a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="81e8a-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="81e8a-115">이 예제에서는 **AlertRule** 설정을  사용하지 않도록 설정하고 *Disabled-AlertRuleDisplayName로 이름을 변경합니다.*</span><span class="sxs-lookup"><span data-stu-id="81e8a-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="81e8a-116">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="81e8a-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="81e8a-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="81e8a-118">이 예제에서는 InputObject를 사용하지 않도록 설정하여 **AlertRule을** *업데이트합니다.*</span><span class="sxs-lookup"><span data-stu-id="81e8a-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="81e8a-119">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="81e8a-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81e8a-120">PARAMETERS</span></span>

### <span data-ttu-id="81e8a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="81e8a-121">-AlertRuleId</span></span>
<span data-ttu-id="81e8a-122">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="81e8a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="81e8a-124">경고 규칙 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e8a-125">-DefaultProfile</span></span>
<span data-ttu-id="81e8a-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-127">-Description</span><span class="sxs-lookup"><span data-stu-id="81e8a-127">-Description</span></span>
<span data-ttu-id="81e8a-128">설명입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-129">-사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="81e8a-129">-Disabled</span></span>
<span data-ttu-id="81e8a-130">경고 규칙 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81e8a-131">-DisplayName</span></span>
<span data-ttu-id="81e8a-132">경고 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="81e8a-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="81e8a-134">경고 규칙 표시 이름은 필터를 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="81e8a-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="81e8a-136">경고 규칙 표시 이름 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-137">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="81e8a-137">-Enabled</span></span>
<span data-ttu-id="81e8a-138">경고 규칙이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81e8a-139">-InputObject</span></span>
<span data-ttu-id="81e8a-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="81e8a-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="81e8a-141">-ProductFilter</span></span>
<span data-ttu-id="81e8a-142">경고 규칙 제품 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-143">-쿼리</span><span class="sxs-lookup"><span data-stu-id="81e8a-143">-Query</span></span>
<span data-ttu-id="81e8a-144">경고 규칙 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="81e8a-145">-QueryFrequency</span></span>
<span data-ttu-id="81e8a-146">경고 규칙 쿼리 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="81e8a-147">-QueryPeriod</span></span>
<span data-ttu-id="81e8a-148">경고 규칙 쿼리 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e8a-149">-ResourceGroupName</span></span>
<span data-ttu-id="81e8a-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e8a-151">-ResourceId</span></span>
<span data-ttu-id="81e8a-152">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="81e8a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="81e8a-154">경고 규칙 심각도 필터.</span><span class="sxs-lookup"><span data-stu-id="81e8a-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-155">-심각도</span><span class="sxs-lookup"><span data-stu-id="81e8a-155">-Severity</span></span>
<span data-ttu-id="81e8a-156">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="81e8a-157">-SuppressionDisabled</span></span>
<span data-ttu-id="81e8a-158">경고 규칙 억제를 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="81e8a-159">-SuppressionDuration</span></span>
<span data-ttu-id="81e8a-160">경고 규칙 억제 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="81e8a-161">-SuppressionEnabled</span></span>
<span data-ttu-id="81e8a-162">경고 규칙 억제를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-163">-전술</span><span class="sxs-lookup"><span data-stu-id="81e8a-163">-Tactics</span></span>
<span data-ttu-id="81e8a-164">경고 규칙 전술.</span><span class="sxs-lookup"><span data-stu-id="81e8a-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="81e8a-165">-TriggerOperator</span></span>
<span data-ttu-id="81e8a-166">경고 규칙 트리거 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="81e8a-167">-TriggerThreshold</span></span>
<span data-ttu-id="81e8a-168">경고 규칙 트리거 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81e8a-169">-WorkspaceName</span></span>
<span data-ttu-id="81e8a-170">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-171">-확인</span><span class="sxs-lookup"><span data-stu-id="81e8a-171">-Confirm</span></span>
<span data-ttu-id="81e8a-172">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e8a-173">-WhatIf</span></span>
<span data-ttu-id="81e8a-174">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e8a-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e8a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e8a-176">CommonParameters</span></span>
<span data-ttu-id="81e8a-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81e8a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e8a-178">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81e8a-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e8a-179">입력</span><span class="sxs-lookup"><span data-stu-id="81e8a-179">INPUTS</span></span>

### <span data-ttu-id="81e8a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="81e8a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="81e8a-181">System.String</span><span class="sxs-lookup"><span data-stu-id="81e8a-181">System.String</span></span>

## <span data-ttu-id="81e8a-182">출력</span><span class="sxs-lookup"><span data-stu-id="81e8a-182">OUTPUTS</span></span>

### <span data-ttu-id="81e8a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="81e8a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="81e8a-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81e8a-184">NOTES</span></span>

## <span data-ttu-id="81e8a-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81e8a-185">RELATED LINKS</span></span>
