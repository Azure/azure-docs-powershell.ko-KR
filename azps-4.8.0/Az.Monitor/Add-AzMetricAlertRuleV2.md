---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 142f1984b875b9ee298063708d654b97d7401fc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048188"
---
# <span data-ttu-id="82aad-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="82aad-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="82aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82aad-102">SYNOPSIS</span></span>
<span data-ttu-id="82aad-103">V2 (비 클래식) 메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="82aad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82aad-104">SYNTAX</span></span>

### <span data-ttu-id="82aad-105">CreateAlertByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="82aad-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82aad-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="82aad-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82aad-107">설명은</span><span class="sxs-lookup"><span data-stu-id="82aad-107">DESCRIPTION</span></span>
<span data-ttu-id="82aad-108">**V2 (비 클래식) 메트릭 기반 알림 규칙** 을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="82aad-109">추가 된 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="82aad-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="82aad-111">예제의</span><span class="sxs-lookup"><span data-stu-id="82aad-111">EXAMPLES</span></span>

### <span data-ttu-id="82aad-112">예제 1: 가상 컴퓨터에 메트릭 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="82aad-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="82aad-113">이 명령은 가상 컴퓨터에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="82aad-114">$condition는 New-AzMetricAlertRuleV2Criteria cmdlet의 출력과 $act는 New-AzActionGroup cmdlet의 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="82aad-115">예제 2: 구독의 모든 가상 컴퓨터에 대 한 메트릭 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="82aad-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="82aad-116">이 명령은 미국 내 구독에 있는 모든 가상 컴퓨터에 대 한 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="82aad-117">예제 3: 메트릭 알림 규칙 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="82aad-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="82aad-118">이 명령은 메트릭 알림 규칙을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="82aad-119">여기서는 Get-AzMetricAlertRuleV2에 대 한 파이프 출력이 Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="82aad-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="82aad-120">예제 4: 차원이 포함 된 메트릭 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="82aad-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="82aad-121">차원 값을 선택 하거나 여러 조건을 포함 하는 것 처럼 복잡 한 메트릭 경고 규칙을 만들려면 도우미 cmdlet New-AzMetricAlertRuleV2DimensionSelection 및 AzMetricAlertRuleV2Criteria를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="82aad-122">위의 cmdlet 집합에서는 차원이 포함 된 메트릭 알림 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="82aad-123">변수</span><span class="sxs-lookup"><span data-stu-id="82aad-123">PARAMETERS</span></span>

### <span data-ttu-id="82aad-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="82aad-124">-ActionGroup</span></span>
<span data-ttu-id="82aad-125">규칙에 대 한 작업 그룹</span><span class="sxs-lookup"><span data-stu-id="82aad-125">The Action Group for rule</span></span>

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

### <span data-ttu-id="82aad-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="82aad-126">-ActionGroupId</span></span>
<span data-ttu-id="82aad-127">규칙의 작업 그룹 id</span><span class="sxs-lookup"><span data-stu-id="82aad-127">The Action Group id for rule</span></span>

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

### <span data-ttu-id="82aad-128">-조건</span><span class="sxs-lookup"><span data-stu-id="82aad-128">-Condition</span></span>
<span data-ttu-id="82aad-129">규칙 조건</span><span class="sxs-lookup"><span data-stu-id="82aad-129">The condition for rule</span></span>

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

### <span data-ttu-id="82aad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82aad-130">-DefaultProfile</span></span>
<span data-ttu-id="82aad-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82aad-132">-설명</span><span class="sxs-lookup"><span data-stu-id="82aad-132">-Description</span></span>
<span data-ttu-id="82aad-133">메트릭 경고 규칙에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="82aad-133">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="82aad-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="82aad-134">-DisableRule</span></span>
<span data-ttu-id="82aad-135">사용 안 함 규칙 (상태) 플래그</span><span class="sxs-lookup"><span data-stu-id="82aad-135">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="82aad-136">-빈도</span><span class="sxs-lookup"><span data-stu-id="82aad-136">-Frequency</span></span>
<span data-ttu-id="82aad-137">규칙에 대 한 평가 빈도</span><span class="sxs-lookup"><span data-stu-id="82aad-137">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="82aad-138">-이름</span><span class="sxs-lookup"><span data-stu-id="82aad-138">-Name</span></span>
<span data-ttu-id="82aad-139">메트릭 알림 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-139">The name of metric alert rule</span></span>

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

### <span data-ttu-id="82aad-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82aad-140">-ResourceGroupName</span></span>
<span data-ttu-id="82aad-141">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="82aad-141">The Resource Group Name</span></span>

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

### <span data-ttu-id="82aad-142">-심각도</span><span class="sxs-lookup"><span data-stu-id="82aad-142">-Severity</span></span>
<span data-ttu-id="82aad-143">메트릭 알림 규칙의 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-143">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="82aad-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="82aad-144">-TargetResourceId</span></span>
<span data-ttu-id="82aad-145">규칙의 대상 리소스 id</span><span class="sxs-lookup"><span data-stu-id="82aad-145">The target resource id for rule</span></span>

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

### <span data-ttu-id="82aad-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="82aad-146">-TargetResourceRegion</span></span>
<span data-ttu-id="82aad-147">규칙에 대 한 대상 리소스 영역</span><span class="sxs-lookup"><span data-stu-id="82aad-147">The target resource region for rule</span></span>

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

### <span data-ttu-id="82aad-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="82aad-148">-TargetResourceScope</span></span>
<span data-ttu-id="82aad-149">규칙에 대 한 대상 리소스 범위</span><span class="sxs-lookup"><span data-stu-id="82aad-149">The target resource scope for rule</span></span>

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

### <span data-ttu-id="82aad-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="82aad-150">-TargetResourceType</span></span>
<span data-ttu-id="82aad-151">규칙에 대 한 대상 리소스 형식</span><span class="sxs-lookup"><span data-stu-id="82aad-151">The target resource type for rule</span></span>

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

### <span data-ttu-id="82aad-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="82aad-152">-WindowSize</span></span>
<span data-ttu-id="82aad-153">규칙의 창 크기</span><span class="sxs-lookup"><span data-stu-id="82aad-153">The window size for rule</span></span>

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

### <span data-ttu-id="82aad-154">-확인</span><span class="sxs-lookup"><span data-stu-id="82aad-154">-Confirm</span></span>
<span data-ttu-id="82aad-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82aad-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82aad-156">-WhatIf</span></span>
<span data-ttu-id="82aad-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82aad-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82aad-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82aad-159">CommonParameters</span></span>
<span data-ttu-id="82aad-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82aad-161">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82aad-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82aad-162">입력</span><span class="sxs-lookup"><span data-stu-id="82aad-162">INPUTS</span></span>

### <span data-ttu-id="82aad-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82aad-163">System.String</span></span>

### <span data-ttu-id="82aad-164">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="82aad-164">System.TimeSpan</span></span>

### <span data-ttu-id="82aad-165">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="82aad-165">System.String[]</span></span>

### <span data-ttu-id="82aad-166">System.webserver. List ' 1 [[IPSMultiMetricCriteria, [Microsoft Azure. 1.0.1.0., Microsoft Azure. PowerShell., Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="82aad-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="82aad-167">Microsoft. Azure. 관리. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="82aad-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="82aad-168">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="82aad-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="82aad-169">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="82aad-169">System.Int32</span></span>

## <span data-ttu-id="82aad-170">출력</span><span class="sxs-lookup"><span data-stu-id="82aad-170">OUTPUTS</span></span>

### <span data-ttu-id="82aad-171">PSMetricAlertRuleV2를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="82aad-172">상속자</span><span class="sxs-lookup"><span data-stu-id="82aad-172">NOTES</span></span>

## <span data-ttu-id="82aad-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82aad-173">RELATED LINKS</span></span>
