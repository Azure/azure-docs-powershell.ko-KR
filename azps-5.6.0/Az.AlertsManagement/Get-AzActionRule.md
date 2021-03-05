---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: c90c4ba559bfe6e453a984546217692181f40597
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961040"
---
# <span data-ttu-id="821f0-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="821f0-101">Get-AzActionRule</span></span>

## <span data-ttu-id="821f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821f0-102">SYNOPSIS</span></span>
<span data-ttu-id="821f0-103">작업 규칙 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="821f0-103">Get Action Rules Information</span></span>

## <span data-ttu-id="821f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="821f0-104">SYNTAX</span></span>

### <span data-ttu-id="821f0-105">ListActionRules(기본값)</span><span class="sxs-lookup"><span data-stu-id="821f0-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="821f0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="821f0-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="821f0-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="821f0-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="821f0-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="821f0-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="821f0-109">설명</span><span class="sxs-lookup"><span data-stu-id="821f0-109">DESCRIPTION</span></span>
<span data-ttu-id="821f0-110">**Get-AzActionRule** cmdlet은 구성된 작업 규칙을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="821f0-111">예제</span><span class="sxs-lookup"><span data-stu-id="821f0-111">EXAMPLES</span></span>

### <span data-ttu-id="821f0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="821f0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="821f0-113">Sev2 심각도 및 플랫폼 모니터 서비스에 필터링된 리소스 그룹 test-rg에 구성된 모든 작업 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="821f0-114">목록에서 Format-List 각 작업 규칙의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="821f0-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="821f0-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="821f0-116">test-rg 리소스 그룹의 이름 Test-Action-Rule이 있는 작업 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="821f0-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="821f0-117">PARAMETERS</span></span>

### <span data-ttu-id="821f0-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="821f0-118">-ActionGroup</span></span>
<span data-ttu-id="821f0-119">작업 그룹</span><span class="sxs-lookup"><span data-stu-id="821f0-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="821f0-120">-AlertRuleId</span></span>
<span data-ttu-id="821f0-121">경고 규칙 ID에 대한 필터링</span><span class="sxs-lookup"><span data-stu-id="821f0-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821f0-122">-DefaultProfile</span></span>
<span data-ttu-id="821f0-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="821f0-124">-Description</span><span class="sxs-lookup"><span data-stu-id="821f0-124">-Description</span></span>
<span data-ttu-id="821f0-125">스마트 그룹 ID가 있는 모든 경고 필터링</span><span class="sxs-lookup"><span data-stu-id="821f0-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="821f0-126">-ImpactedScope</span></span>
<span data-ttu-id="821f0-127">영향을 미치는 범위에 대한 필터링</span><span class="sxs-lookup"><span data-stu-id="821f0-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="821f0-128">-MonitorService</span></span>
<span data-ttu-id="821f0-129">Moniter Service에서 필터링</span><span class="sxs-lookup"><span data-stu-id="821f0-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-130">-Name</span><span class="sxs-lookup"><span data-stu-id="821f0-130">-Name</span></span>
<span data-ttu-id="821f0-131">작업 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821f0-132">-ResourceGroupName</span></span>
<span data-ttu-id="821f0-133">작업 규칙이 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="821f0-134">-ResourceId</span></span>
<span data-ttu-id="821f0-135">리소스 ID로 작업 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-136">-심각도</span><span class="sxs-lookup"><span data-stu-id="821f0-136">-Severity</span></span>
<span data-ttu-id="821f0-137">경고의 심각도 필터링</span><span class="sxs-lookup"><span data-stu-id="821f0-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="821f0-138">-TargetResourceGroup</span></span>
<span data-ttu-id="821f0-139">경고의 대상 리소스의 리소스 그룹 이름을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="821f0-140">-TargetResourceId</span></span>
<span data-ttu-id="821f0-141">경고의 대상 리소스의 리소스 ID를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="821f0-142">-TargetResourceType</span></span>
<span data-ttu-id="821f0-143">경고의 대상 리소스의 리소스 유형을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821f0-144">CommonParameters</span></span>
<span data-ttu-id="821f0-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="821f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821f0-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="821f0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821f0-147">입력</span><span class="sxs-lookup"><span data-stu-id="821f0-147">INPUTS</span></span>

### <span data-ttu-id="821f0-148">없음</span><span class="sxs-lookup"><span data-stu-id="821f0-148">None</span></span>

## <span data-ttu-id="821f0-149">출력</span><span class="sxs-lookup"><span data-stu-id="821f0-149">OUTPUTS</span></span>

### <span data-ttu-id="821f0-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="821f0-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="821f0-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="821f0-151">NOTES</span></span>

## <span data-ttu-id="821f0-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="821f0-152">RELATED LINKS</span></span>
