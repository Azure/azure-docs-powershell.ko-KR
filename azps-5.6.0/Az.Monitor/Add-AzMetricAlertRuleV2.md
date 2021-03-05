---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: f679b674de8ed2f860278cb3a384f73ed17e5f54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980267"
---
# <span data-ttu-id="c28e8-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c28e8-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="c28e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c28e8-103">V2(클래식이 아닌) 메트릭 기반 경고 규칙을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="c28e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="c28e8-104">SYNTAX</span></span>

### <span data-ttu-id="c28e8-105">CreateAlertByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="c28e8-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c28e8-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="c28e8-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c28e8-107">설명</span><span class="sxs-lookup"><span data-stu-id="c28e8-107">DESCRIPTION</span></span>
<span data-ttu-id="c28e8-108">V2(클래식이 아닌) 메트릭 기반 경고 규칙을 **추가하거나 업데이트합니다.**</span><span class="sxs-lookup"><span data-stu-id="c28e8-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="c28e8-109">추가된 규칙은 리소스 그룹과 연결되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="c28e8-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c28e8-111">예제</span><span class="sxs-lookup"><span data-stu-id="c28e8-111">EXAMPLES</span></span>

### <span data-ttu-id="c28e8-112">예제 1: 가상 머신에 메트릭 경고 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="c28e8-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c28e8-113">이 명령은 가상 머신에 대한 메트릭 경고 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="c28e8-114">$condition [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet의 출력이고 [$act-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) cmdlet의 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="c28e8-115">예제 2: 구독의 모든 가상 머신에 대한 메트릭 경고 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="c28e8-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c28e8-116">이 명령은 eastus에 있는 구독의 모든 가상 머신에 대한 메트릭 경고 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="c28e8-117">예제 3: 메트릭 경고 규칙을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="c28e8-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c28e8-118">이 명령은 메트릭 경고 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="c28e8-119">여기에서 [Get-AzMetricAlertRuleV2의](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) 배관 출력을 [Add-AzMetricAlertRuleV2로 출력합니다.](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="c28e8-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="c28e8-120">예제 4: 차원을 사용하여 메트릭 경고 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="c28e8-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="c28e8-121">차원 값을 선택하거나 여러 조건이 있는 메트릭 경고 규칙과 같은 더 복잡한 메트릭 경고 규칙을 만들하려면 도우미 cmdlet [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) 및 [New-AzMetricAlertRuleV2Criteria를](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="c28e8-122">위의 cmdlet 집합은 차원을 사용하여 메트릭 경고 규칙을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="c28e8-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c28e8-123">PARAMETERS</span></span>

### <span data-ttu-id="c28e8-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="c28e8-124">-ActionGroup</span></span>
<span data-ttu-id="c28e8-125">규칙에 대한 작업 그룹</span><span class="sxs-lookup"><span data-stu-id="c28e8-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c28e8-126">-ActionGroupId</span></span>
<span data-ttu-id="c28e8-127">규칙에 대한 작업 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="c28e8-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-128">-조건</span><span class="sxs-lookup"><span data-stu-id="c28e8-128">-Condition</span></span>
<span data-ttu-id="c28e8-129">규칙 조건</span><span class="sxs-lookup"><span data-stu-id="c28e8-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28e8-130">-DefaultProfile</span></span>
<span data-ttu-id="c28e8-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28e8-132">-Description</span><span class="sxs-lookup"><span data-stu-id="c28e8-132">-Description</span></span>
<span data-ttu-id="c28e8-133">메트릭 경고 규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="c28e8-133">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="c28e8-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c28e8-134">-DisableRule</span></span>
<span data-ttu-id="c28e8-135">사용하지 않도록 설정 규칙(상태) 플래그</span><span class="sxs-lookup"><span data-stu-id="c28e8-135">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="c28e8-136">-빈도</span><span class="sxs-lookup"><span data-stu-id="c28e8-136">-Frequency</span></span>
<span data-ttu-id="c28e8-137">규칙에 대한 평가 빈도</span><span class="sxs-lookup"><span data-stu-id="c28e8-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c28e8-138">-Name</span></span>
<span data-ttu-id="c28e8-139">메트릭 경고 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="c28e8-139">The name of metric alert rule</span></span>

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

### <span data-ttu-id="c28e8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28e8-140">-ResourceGroupName</span></span>
<span data-ttu-id="c28e8-141">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c28e8-141">The Resource Group Name</span></span>

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

### <span data-ttu-id="c28e8-142">-심각도</span><span class="sxs-lookup"><span data-stu-id="c28e8-142">-Severity</span></span>
<span data-ttu-id="c28e8-143">메트릭 경고 규칙의 심각도</span><span class="sxs-lookup"><span data-stu-id="c28e8-143">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="c28e8-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c28e8-144">-TargetResourceId</span></span>
<span data-ttu-id="c28e8-145">규칙에 대한 대상 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c28e8-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="c28e8-146">-TargetResourceRegion</span></span>
<span data-ttu-id="c28e8-147">규칙의 대상 리소스 영역</span><span class="sxs-lookup"><span data-stu-id="c28e8-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="c28e8-148">-TargetResourceScope</span></span>
<span data-ttu-id="c28e8-149">규칙의 대상 리소스 범위</span><span class="sxs-lookup"><span data-stu-id="c28e8-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="c28e8-150">-TargetResourceType</span></span>
<span data-ttu-id="c28e8-151">규칙의 대상 리소스 유형</span><span class="sxs-lookup"><span data-stu-id="c28e8-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28e8-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="c28e8-152">-WindowSize</span></span>
<span data-ttu-id="c28e8-153">규칙의 창 크기</span><span class="sxs-lookup"><span data-stu-id="c28e8-153">The window size for rule</span></span>

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

### <span data-ttu-id="c28e8-154">-확인</span><span class="sxs-lookup"><span data-stu-id="c28e8-154">-Confirm</span></span>
<span data-ttu-id="c28e8-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28e8-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28e8-156">-WhatIf</span></span>
<span data-ttu-id="c28e8-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28e8-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28e8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28e8-159">CommonParameters</span></span>
<span data-ttu-id="c28e8-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c28e8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28e8-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28e8-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28e8-162">입력</span><span class="sxs-lookup"><span data-stu-id="c28e8-162">INPUTS</span></span>

### <span data-ttu-id="c28e8-163">System.String</span><span class="sxs-lookup"><span data-stu-id="c28e8-163">System.String</span></span>

### <span data-ttu-id="c28e8-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c28e8-164">System.TimeSpan</span></span>

### <span data-ttu-id="c28e8-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c28e8-165">System.String[]</span></span>

### <span data-ttu-id="c28e8-166">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c28e8-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c28e8-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="c28e8-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="c28e8-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c28e8-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c28e8-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c28e8-169">System.Int32</span></span>

## <span data-ttu-id="c28e8-170">출력</span><span class="sxs-lookup"><span data-stu-id="c28e8-170">OUTPUTS</span></span>

### <span data-ttu-id="c28e8-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c28e8-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="c28e8-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c28e8-172">NOTES</span></span>

## <span data-ttu-id="c28e8-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c28e8-173">RELATED LINKS</span></span>
