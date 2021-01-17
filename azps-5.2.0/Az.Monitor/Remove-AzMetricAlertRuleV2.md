---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323294"
---
# <span data-ttu-id="1d37f-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1d37f-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="1d37f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d37f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d37f-103">V2(클래식이 아닌) 메트릭 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="1d37f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d37f-104">SYNTAX</span></span>

### <span data-ttu-id="1d37f-105">ByMetricRuleResourceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d37f-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d37f-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1d37f-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d37f-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d37f-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d37f-108">설명</span><span class="sxs-lookup"><span data-stu-id="1d37f-108">DESCRIPTION</span></span>
<span data-ttu-id="1d37f-109">**Remove-AzMetricAlertRuleV2** cmdlet은 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="1d37f-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1d37f-111">예제</span><span class="sxs-lookup"><span data-stu-id="1d37f-111">EXAMPLES</span></span>

### <span data-ttu-id="1d37f-112">예제 1: 이름으로 경고 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="1d37f-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="1d37f-113">이 명령은 PsSdk라는 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="1d37f-114">예제 2: ID로 경고 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="1d37f-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="1d37f-115">이 명령은 리소스 ID를 사용하여 경고 규칙을 제거합니다. `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="1d37f-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="1d37f-116">예제 3: 경고를 표시하고 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="1d37f-117">이 명령은 경고를 얻게 하여 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="1d37f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d37f-118">PARAMETERS</span></span>

### <span data-ttu-id="1d37f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d37f-119">-AsJob</span></span>
<span data-ttu-id="1d37f-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1d37f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d37f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d37f-121">-DefaultProfile</span></span>
<span data-ttu-id="1d37f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d37f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d37f-123">-InputObject</span></span>
<span data-ttu-id="1d37f-124">메트릭 규칙 개체</span><span class="sxs-lookup"><span data-stu-id="1d37f-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d37f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1d37f-125">-Name</span></span>
<span data-ttu-id="1d37f-126">메트릭 경고 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="1d37f-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d37f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d37f-127">-PassThru</span></span>
<span data-ttu-id="1d37f-128">성공적으로 지우면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="1d37f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d37f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1d37f-130">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d37f-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d37f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d37f-131">-ResourceId</span></span>
<span data-ttu-id="1d37f-132">The RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1d37f-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d37f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d37f-133">-Confirm</span></span>
<span data-ttu-id="1d37f-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d37f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d37f-135">-WhatIf</span></span>
<span data-ttu-id="1d37f-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1d37f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d37f-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d37f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d37f-138">CommonParameters</span></span>
<span data-ttu-id="1d37f-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d37f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d37f-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d37f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d37f-141">입력</span><span class="sxs-lookup"><span data-stu-id="1d37f-141">INPUTS</span></span>

### <span data-ttu-id="1d37f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1d37f-142">System.String</span></span>

### <span data-ttu-id="1d37f-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1d37f-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="1d37f-144">출력</span><span class="sxs-lookup"><span data-stu-id="1d37f-144">OUTPUTS</span></span>

### <span data-ttu-id="1d37f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d37f-145">System.Boolean</span></span>

## <span data-ttu-id="1d37f-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d37f-146">NOTES</span></span>

## <span data-ttu-id="1d37f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d37f-147">RELATED LINKS</span></span>
