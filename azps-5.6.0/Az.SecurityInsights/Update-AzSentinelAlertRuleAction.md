---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955648"
---
# <span data-ttu-id="08a0c-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="08a0c-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="08a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="08a0c-103">자동화된 응답(경고 규칙 작업)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="08a0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="08a0c-104">SYNTAX</span></span>

### <span data-ttu-id="08a0c-105">ActionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="08a0c-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a0c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="08a0c-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08a0c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="08a0c-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a0c-108">설명</span><span class="sxs-lookup"><span data-stu-id="08a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="08a0c-109">**Update-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역의 책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="08a0c-110">**AlertRuleAction** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 *AlertRuleId* 및 *ActionId* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="08a0c-111">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="08a0c-112">예제</span><span class="sxs-lookup"><span data-stu-id="08a0c-112">EXAMPLES</span></span>

### <span data-ttu-id="08a0c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="08a0c-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="08a0c-114">이 예제에서는 기존 작업을 새 속성으로 대체하는 **AlertRuleAction을** 업데이트합니다. </span><span class="sxs-lookup"><span data-stu-id="08a0c-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="08a0c-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="08a0c-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="08a0c-116">이 예제에서는 기존 작업을 새 속성으로 대체하는 InputObject를 사용하여 **AlertRuleAction을** 업데이트합니다. </span><span class="sxs-lookup"><span data-stu-id="08a0c-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="08a0c-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="08a0c-117">PARAMETERS</span></span>

### <span data-ttu-id="08a0c-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="08a0c-118">-ActionId</span></span>
<span data-ttu-id="08a0c-119">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="08a0c-120">-AlertRuleId</span></span>
<span data-ttu-id="08a0c-121">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a0c-122">-DefaultProfile</span></span>
<span data-ttu-id="08a0c-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08a0c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08a0c-124">-InputObject</span></span>
<span data-ttu-id="08a0c-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="08a0c-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="08a0c-126">-LogicAppResourceId</span></span>
<span data-ttu-id="08a0c-127">작업 논리 앱 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="08a0c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a0c-128">-ResourceGroupName</span></span>
<span data-ttu-id="08a0c-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08a0c-130">-ResourceId</span></span>
<span data-ttu-id="08a0c-131">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="08a0c-132">-TriggerUri</span></span>
<span data-ttu-id="08a0c-133">작업 논리 앱 트리거 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="08a0c-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08a0c-134">-WorkspaceName</span></span>
<span data-ttu-id="08a0c-135">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="08a0c-136">-Confirm</span></span>
<span data-ttu-id="08a0c-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a0c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a0c-138">-WhatIf</span></span>
<span data-ttu-id="08a0c-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a0c-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a0c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a0c-141">CommonParameters</span></span>
<span data-ttu-id="08a0c-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08a0c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a0c-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08a0c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a0c-144">입력</span><span class="sxs-lookup"><span data-stu-id="08a0c-144">INPUTS</span></span>

### <span data-ttu-id="08a0c-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="08a0c-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="08a0c-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="08a0c-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="08a0c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="08a0c-147">System.String</span></span>

## <span data-ttu-id="08a0c-148">출력</span><span class="sxs-lookup"><span data-stu-id="08a0c-148">OUTPUTS</span></span>

### <span data-ttu-id="08a0c-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="08a0c-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="08a0c-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08a0c-150">NOTES</span></span>

## <span data-ttu-id="08a0c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08a0c-151">RELATED LINKS</span></span>
