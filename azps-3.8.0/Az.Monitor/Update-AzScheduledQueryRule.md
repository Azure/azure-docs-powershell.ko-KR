---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1d58fba402f292c0935fc10715e06b323353046c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877310"
---
# <span data-ttu-id="d7df4-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d7df4-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="d7df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7df4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7df4-103">로그 알림 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7df4-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="d7df4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7df4-104">SYNTAX</span></span>

### <span data-ttu-id="d7df4-105">ByRuleName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7df4-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7df4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7df4-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7df4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7df4-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7df4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d7df4-108">DESCRIPTION</span></span>
<span data-ttu-id="d7df4-109">로그 경고 규칙을 업데이트 하 고,이 명령에서는 "Enabled" 속성만 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="d7df4-110">다른 속성을 업데이트 하려면 "Set-AzScheduledQueryRule" 명령을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7df4-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="d7df4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d7df4-111">EXAMPLES</span></span>

### <span data-ttu-id="d7df4-112">예제 1-규칙 이름별 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7df4-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="d7df4-113">예제 2-입력 개체를 기준으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7df4-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="d7df4-114">예제 3-리소스 Id 별 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7df4-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="d7df4-115">변수</span><span class="sxs-lookup"><span data-stu-id="d7df4-115">PARAMETERS</span></span>

### <span data-ttu-id="d7df4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7df4-116">-DefaultProfile</span></span>
<span data-ttu-id="d7df4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7df4-118">-사용</span><span class="sxs-lookup"><span data-stu-id="d7df4-118">-Enabled</span></span>
<span data-ttu-id="d7df4-119">Azure alert state-유효한 값-$true, $false</span><span class="sxs-lookup"><span data-stu-id="d7df4-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="d7df4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7df4-120">-InputObject</span></span>
<span data-ttu-id="d7df4-121">예약 된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="d7df4-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="d7df4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d7df4-122">-Name</span></span>
<span data-ttu-id="d7df4-123">알림 이름</span><span class="sxs-lookup"><span data-stu-id="d7df4-123">The alert name</span></span>

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

### <span data-ttu-id="d7df4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7df4-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7df4-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d7df4-125">The resource group name</span></span>

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

### <span data-ttu-id="d7df4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7df4-126">-ResourceId</span></span>
<span data-ttu-id="d7df4-127">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d7df4-127">The resource Id</span></span>

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

### <span data-ttu-id="d7df4-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d7df4-128">-Confirm</span></span>
<span data-ttu-id="d7df4-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7df4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7df4-130">-WhatIf</span></span>
<span data-ttu-id="d7df4-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7df4-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7df4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7df4-133">CommonParameters</span></span>
<span data-ttu-id="d7df4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7df4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7df4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7df4-136">입력</span><span class="sxs-lookup"><span data-stu-id="d7df4-136">INPUTS</span></span>

### <span data-ttu-id="d7df4-137">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="d7df4-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7df4-138">System.String</span></span>

## <span data-ttu-id="d7df4-139">출력</span><span class="sxs-lookup"><span data-stu-id="d7df4-139">OUTPUTS</span></span>

### <span data-ttu-id="d7df4-140">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7df4-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="d7df4-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d7df4-141">NOTES</span></span>

## <span data-ttu-id="d7df4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7df4-142">RELATED LINKS</span></span>
