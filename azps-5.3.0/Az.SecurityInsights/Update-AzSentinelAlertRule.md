---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494918"
---
# <span data-ttu-id="b6c0c-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b6c0c-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="b6c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c0c-103">분석(경고 규칙)을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="b6c0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6c0c-104">SYNTAX</span></span>

### <span data-ttu-id="b6c0c-105">AlertRuleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6c0c-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="b6c0c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6c0c-106">InputObject</span></span>
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

### <span data-ttu-id="b6c0c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c0c-107">ResourceId</span></span>
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

## <span data-ttu-id="b6c0c-108">설명</span><span class="sxs-lookup"><span data-stu-id="b6c0c-108">DESCRIPTION</span></span>
<span data-ttu-id="b6c0c-109">**Update-AzSentinelAlertRule** cmdlet은 지정된 작업 영역의 분석(경고 규칙)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="b6c0c-110">-InputObject 또는 -ResourceId 또는 -AlertId를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="b6c0c-111">1개 이상의 proprtery parmaters를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="b6c0c-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="b6c0c-113">예제</span><span class="sxs-lookup"><span data-stu-id="b6c0c-113">EXAMPLES</span></span>

### <span data-ttu-id="b6c0c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6c0c-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="b6c0c-115">이 예제에서는 **AlertRule** 설정을 *Disabled로* 업데이트하고 *Disabled-AlertRuleDisplayName으로 이름을 변경합니다.*</span><span class="sxs-lookup"><span data-stu-id="b6c0c-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="b6c0c-116">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="b6c0c-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="b6c0c-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="b6c0c-118">이 예제에서는 InputObject 설정을 사용 안 으로 설정하여 **AlertRule을** *업데이트합니다.*</span><span class="sxs-lookup"><span data-stu-id="b6c0c-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="b6c0c-119">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="b6c0c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6c0c-120">PARAMETERS</span></span>

### <span data-ttu-id="b6c0c-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="b6c0c-121">-AlertRuleId</span></span>
<span data-ttu-id="b6c0c-122">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="b6c0c-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="b6c0c-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="b6c0c-124">경고 규칙 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="b6c0c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c0c-125">-DefaultProfile</span></span>
<span data-ttu-id="b6c0c-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6c0c-127">-Description</span><span class="sxs-lookup"><span data-stu-id="b6c0c-127">-Description</span></span>
<span data-ttu-id="b6c0c-128">설명.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-128">Description.</span></span>

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

### <span data-ttu-id="b6c0c-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="b6c0c-129">-Disabled</span></span>
<span data-ttu-id="b6c0c-130">경고 규칙 사용 안</span><span class="sxs-lookup"><span data-stu-id="b6c0c-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="b6c0c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b6c0c-131">-DisplayName</span></span>
<span data-ttu-id="b6c0c-132">경고 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="b6c0c-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="b6c0c-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="b6c0c-134">경고 규칙 표시 이름은 필터를 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="b6c0c-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="b6c0c-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="b6c0c-136">경고 규칙 표시 이름 필터.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="b6c0c-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b6c0c-137">-Enabled</span></span>
<span data-ttu-id="b6c0c-138">경고 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="b6c0c-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="b6c0c-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6c0c-139">-InputObject</span></span>
<span data-ttu-id="b6c0c-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-140">InputObject.</span></span>

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

### <span data-ttu-id="b6c0c-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="b6c0c-141">-ProductFilter</span></span>
<span data-ttu-id="b6c0c-142">경고 규칙 제품 필터.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="b6c0c-143">-Query</span><span class="sxs-lookup"><span data-stu-id="b6c0c-143">-Query</span></span>
<span data-ttu-id="b6c0c-144">경고 규칙 쿼리.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="b6c0c-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="b6c0c-145">-QueryFrequency</span></span>
<span data-ttu-id="b6c0c-146">경고 규칙 쿼리 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="b6c0c-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="b6c0c-147">-QueryPeriod</span></span>
<span data-ttu-id="b6c0c-148">경고 규칙 쿼리 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="b6c0c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c0c-149">-ResourceGroupName</span></span>
<span data-ttu-id="b6c0c-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-150">Resource group name.</span></span>

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

### <span data-ttu-id="b6c0c-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c0c-151">-ResourceId</span></span>
<span data-ttu-id="b6c0c-152">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-152">Resource Id.</span></span>

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

### <span data-ttu-id="b6c0c-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="b6c0c-153">-SeveritiesFilter</span></span>
<span data-ttu-id="b6c0c-154">경고 규칙 심각도 필터.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="b6c0c-155">-심각도</span><span class="sxs-lookup"><span data-stu-id="b6c0c-155">-Severity</span></span>
<span data-ttu-id="b6c0c-156">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-156">Incident Severity.</span></span>

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

### <span data-ttu-id="b6c0c-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="b6c0c-157">-SuppressionDisabled</span></span>
<span data-ttu-id="b6c0c-158">경고 규칙 표시 안 을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="b6c0c-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="b6c0c-159">-SuppressionDuration</span></span>
<span data-ttu-id="b6c0c-160">경고 규칙 표시 안 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="b6c0c-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b6c0c-161">-SuppressionEnabled</span></span>
<span data-ttu-id="b6c0c-162">경고 규칙 표시 안 을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="b6c0c-163">-전술</span><span class="sxs-lookup"><span data-stu-id="b6c0c-163">-Tactics</span></span>
<span data-ttu-id="b6c0c-164">경고 규칙 전술.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="b6c0c-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="b6c0c-165">-TriggerOperator</span></span>
<span data-ttu-id="b6c0c-166">경고 규칙 트리거 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="b6c0c-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="b6c0c-167">-TriggerThreshold</span></span>
<span data-ttu-id="b6c0c-168">경고 규칙 트리거 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="b6c0c-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6c0c-169">-WorkspaceName</span></span>
<span data-ttu-id="b6c0c-170">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-170">Workspace Name.</span></span>

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

### <span data-ttu-id="b6c0c-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6c0c-171">-Confirm</span></span>
<span data-ttu-id="b6c0c-172">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c0c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c0c-173">-WhatIf</span></span>
<span data-ttu-id="b6c0c-174">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6c0c-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c0c-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c0c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c0c-176">CommonParameters</span></span>
<span data-ttu-id="b6c0c-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c0c-178">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6c0c-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c0c-179">입력</span><span class="sxs-lookup"><span data-stu-id="b6c0c-179">INPUTS</span></span>

### <span data-ttu-id="b6c0c-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b6c0c-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="b6c0c-181">System.String</span><span class="sxs-lookup"><span data-stu-id="b6c0c-181">System.String</span></span>

## <span data-ttu-id="b6c0c-182">출력</span><span class="sxs-lookup"><span data-stu-id="b6c0c-182">OUTPUTS</span></span>

### <span data-ttu-id="b6c0c-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b6c0c-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="b6c0c-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6c0c-184">NOTES</span></span>

## <span data-ttu-id="b6c0c-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6c0c-185">RELATED LINKS</span></span>
