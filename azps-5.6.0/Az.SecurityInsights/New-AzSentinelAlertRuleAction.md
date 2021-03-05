---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: ed4d1b5d833ce73a9b0a19e38a05192d11a0d8f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976363"
---
# <span data-ttu-id="4aff0-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="4aff0-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="4aff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aff0-102">SYNOPSIS</span></span>
<span data-ttu-id="4aff0-103">Analatic에 자동화된 응답을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="4aff0-104">구문</span><span class="sxs-lookup"><span data-stu-id="4aff0-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aff0-105">설명</span><span class="sxs-lookup"><span data-stu-id="4aff0-105">DESCRIPTION</span></span>
<span data-ttu-id="4aff0-106">**New-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역의 경고 규칙에 대한 자동화된 응답을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="4aff0-107">Logic App 모듈을 사용하여 찾을 수 있는 Logic App Resorce ID 및 트리거 Uri를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="4aff0-108">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4aff0-109">예제</span><span class="sxs-lookup"><span data-stu-id="4aff0-109">EXAMPLES</span></span>

### <span data-ttu-id="4aff0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4aff0-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="4aff0-111">이 예제에서는 Logic App의 속성을 사용하여 지정된 경고 규칙에 대한 **AlertRuleAction을** 만든 다음, 해당 경고 $AlertRuleAction 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="4aff0-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4aff0-112">PARAMETERS</span></span>

### <span data-ttu-id="4aff0-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="4aff0-113">-ActionId</span></span>
<span data-ttu-id="4aff0-114">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff0-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="4aff0-115">-AlertRuleId</span></span>
<span data-ttu-id="4aff0-116">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="4aff0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aff0-117">-DefaultProfile</span></span>
<span data-ttu-id="4aff0-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aff0-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="4aff0-119">-LogicAppResourceId</span></span>
<span data-ttu-id="4aff0-120">작업 논리 앱 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="4aff0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aff0-121">-ResourceGroupName</span></span>
<span data-ttu-id="4aff0-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-122">Resource group name.</span></span>

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

### <span data-ttu-id="4aff0-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="4aff0-123">-TriggerUri</span></span>
<span data-ttu-id="4aff0-124">작업 논리 앱 트리거 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="4aff0-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4aff0-125">-WorkspaceName</span></span>
<span data-ttu-id="4aff0-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-126">Workspace Name.</span></span>

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

### <span data-ttu-id="4aff0-127">-확인</span><span class="sxs-lookup"><span data-stu-id="4aff0-127">-Confirm</span></span>
<span data-ttu-id="4aff0-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aff0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aff0-129">-WhatIf</span></span>
<span data-ttu-id="4aff0-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4aff0-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aff0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aff0-132">CommonParameters</span></span>
<span data-ttu-id="4aff0-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4aff0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aff0-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aff0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aff0-135">입력</span><span class="sxs-lookup"><span data-stu-id="4aff0-135">INPUTS</span></span>

### <span data-ttu-id="4aff0-136">없음</span><span class="sxs-lookup"><span data-stu-id="4aff0-136">None</span></span>
## <span data-ttu-id="4aff0-137">출력</span><span class="sxs-lookup"><span data-stu-id="4aff0-137">OUTPUTS</span></span>

### <span data-ttu-id="4aff0-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="4aff0-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="4aff0-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4aff0-139">NOTES</span></span>

## <span data-ttu-id="4aff0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aff0-140">RELATED LINKS</span></span>
