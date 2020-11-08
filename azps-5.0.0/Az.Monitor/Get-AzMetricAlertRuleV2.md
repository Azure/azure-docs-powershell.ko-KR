---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226756"
---
# <span data-ttu-id="13d3a-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="13d3a-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="13d3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="13d3a-103">V2 (비 클래식) 메트릭 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="13d3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13d3a-104">SYNTAX</span></span>

### <span data-ttu-id="13d3a-105">ByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="13d3a-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d3a-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="13d3a-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d3a-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="13d3a-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d3a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13d3a-108">DESCRIPTION</span></span>
<span data-ttu-id="13d3a-109">**AzMetricAlertRuleV2** cmdlet은 해당 이름 또는 URI 또는 지정 된 리소스 그룹 또는 구독의 모든 메트릭 알림 규칙에 따라 메트릭 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="13d3a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13d3a-110">EXAMPLES</span></span>

### <span data-ttu-id="13d3a-111">예제 1: 현재 구독에서 모든 메트릭 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="13d3a-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="13d3a-112">이 명령은 현재 구독에 있는 모든 메트릭 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="13d3a-113">예제 2: 리소스 그룹의 모든 메트릭 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="13d3a-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="13d3a-114">이 명령은 metricAlertsRG 이라는 리소스 그룹의 모든 메트릭 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="13d3a-115">예제 3: 이름으로 메트릭 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="13d3a-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="13d3a-116">이 명령은 metricAlertsRG 이라는 리소스 그룹에서 PS3182019 라는 메트릭 경고 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="13d3a-117">예제 4: ruleID로 메트릭 알림 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="13d3a-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="13d3a-118">이 명령은 지정 된 리소스 ID를 갖는 메트릭 알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="13d3a-119">변수</span><span class="sxs-lookup"><span data-stu-id="13d3a-119">PARAMETERS</span></span>

### <span data-ttu-id="13d3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d3a-120">-DefaultProfile</span></span>
<span data-ttu-id="13d3a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d3a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="13d3a-122">-Name</span></span>
<span data-ttu-id="13d3a-123">메트릭 알림 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-123">The Name of metric alert rule</span></span>

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

### <span data-ttu-id="13d3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="13d3a-125">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d3a-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d3a-126">-ResourceId</span></span>
<span data-ttu-id="13d3a-127">메트릭 알림 규칙의 규칙 Id</span><span class="sxs-lookup"><span data-stu-id="13d3a-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d3a-128">CommonParameters</span></span>
<span data-ttu-id="13d3a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d3a-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13d3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d3a-131">입력</span><span class="sxs-lookup"><span data-stu-id="13d3a-131">INPUTS</span></span>

### <span data-ttu-id="13d3a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13d3a-132">System.String</span></span>

## <span data-ttu-id="13d3a-133">출력</span><span class="sxs-lookup"><span data-stu-id="13d3a-133">OUTPUTS</span></span>

### <span data-ttu-id="13d3a-134">PSMetricAlertRuleV2를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d3a-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="13d3a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="13d3a-135">NOTES</span></span>

## <span data-ttu-id="13d3a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13d3a-136">RELATED LINKS</span></span>
