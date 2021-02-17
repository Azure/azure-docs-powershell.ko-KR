---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192161"
---
# <span data-ttu-id="c6d29-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c6d29-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="c6d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d29-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d29-103">로그 경고 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6d29-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="c6d29-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6d29-104">SYNTAX</span></span>

### <span data-ttu-id="c6d29-105">ByRuleName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c6d29-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6d29-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6d29-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6d29-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6d29-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6d29-108">설명</span><span class="sxs-lookup"><span data-stu-id="c6d29-108">DESCRIPTION</span></span>
<span data-ttu-id="c6d29-109">로그 경고 규칙을 업데이트하고 이 명령에서 "Enabled" 속성만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="c6d29-110">다른 속성을 업데이트하기 위해 [Set-AzScheduledQueryRule 명령을 참조합니다.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule)</span><span class="sxs-lookup"><span data-stu-id="c6d29-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="c6d29-111">예제</span><span class="sxs-lookup"><span data-stu-id="c6d29-111">EXAMPLES</span></span>

### <span data-ttu-id="c6d29-112">예제 1: 규칙 이름으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6d29-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c6d29-113">예제 2: 입력 개체로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6d29-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c6d29-114">예제 3: 리소스 ID로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6d29-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="c6d29-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6d29-115">PARAMETERS</span></span>

### <span data-ttu-id="c6d29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d29-116">-DefaultProfile</span></span>
<span data-ttu-id="c6d29-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6d29-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c6d29-118">-Enabled</span></span>
<span data-ttu-id="c6d29-119">Azure 경고 상태 - 유효한 값 - $true $false</span><span class="sxs-lookup"><span data-stu-id="c6d29-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6d29-120">-InputObject</span></span>
<span data-ttu-id="c6d29-121">예약된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="c6d29-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c6d29-122">-Name</span></span>
<span data-ttu-id="c6d29-123">경고 이름</span><span class="sxs-lookup"><span data-stu-id="c6d29-123">The alert name</span></span>

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

### <span data-ttu-id="c6d29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d29-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6d29-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c6d29-125">The resource group name</span></span>

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

### <span data-ttu-id="c6d29-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6d29-126">-ResourceId</span></span>
<span data-ttu-id="c6d29-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c6d29-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6d29-128">-Confirm</span></span>
<span data-ttu-id="c6d29-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6d29-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6d29-130">-WhatIf</span></span>
<span data-ttu-id="c6d29-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c6d29-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6d29-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6d29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d29-133">CommonParameters</span></span>
<span data-ttu-id="c6d29-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d29-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6d29-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d29-136">입력</span><span class="sxs-lookup"><span data-stu-id="c6d29-136">INPUTS</span></span>

### <span data-ttu-id="c6d29-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c6d29-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="c6d29-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c6d29-138">System.String</span></span>

## <span data-ttu-id="c6d29-139">출력</span><span class="sxs-lookup"><span data-stu-id="c6d29-139">OUTPUTS</span></span>

### <span data-ttu-id="c6d29-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c6d29-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="c6d29-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6d29-141">NOTES</span></span>

## <span data-ttu-id="c6d29-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d29-142">RELATED LINKS</span></span>
