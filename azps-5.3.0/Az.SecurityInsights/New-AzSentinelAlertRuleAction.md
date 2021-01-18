---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494939"
---
# <span data-ttu-id="1c3af-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="1c3af-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="1c3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3af-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3af-103">Analatic에 자동화된 응답을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="1c3af-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c3af-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3af-105">설명</span><span class="sxs-lookup"><span data-stu-id="1c3af-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3af-106">**New-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역의 경고 규칙에 대한 자동화된 응답을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="1c3af-107">논리 앱 모듈을 사용하여 찾을 수 있는 논리 앱 재지정 ID 및 트리거 URI를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="1c3af-108">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1c3af-109">예제</span><span class="sxs-lookup"><span data-stu-id="1c3af-109">EXAMPLES</span></span>

### <span data-ttu-id="1c3af-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c3af-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="1c3af-111">이 예제에서는 논리 앱의 속성을 사용하여 지정된 경고 규칙에 대한 **AlertRuleAction을** 만든 다음 $AlertRuleAction 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="1c3af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3af-112">PARAMETERS</span></span>

### <span data-ttu-id="1c3af-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="1c3af-113">-ActionId</span></span>
<span data-ttu-id="1c3af-114">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-114">Action Id.</span></span>

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

### <span data-ttu-id="1c3af-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="1c3af-115">-AlertRuleId</span></span>
<span data-ttu-id="1c3af-116">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="1c3af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3af-117">-DefaultProfile</span></span>
<span data-ttu-id="1c3af-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3af-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="1c3af-119">-LogicAppResourceId</span></span>
<span data-ttu-id="1c3af-120">작업 논리 앱 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="1c3af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3af-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c3af-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-122">Resource group name.</span></span>

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

### <span data-ttu-id="1c3af-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="1c3af-123">-TriggerUri</span></span>
<span data-ttu-id="1c3af-124">작업 논리 앱 트리거 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="1c3af-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c3af-125">-WorkspaceName</span></span>
<span data-ttu-id="1c3af-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-126">Workspace Name.</span></span>

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

### <span data-ttu-id="1c3af-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3af-127">-Confirm</span></span>
<span data-ttu-id="1c3af-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3af-129">-WhatIf</span></span>
<span data-ttu-id="1c3af-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c3af-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c3af-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3af-132">CommonParameters</span></span>
<span data-ttu-id="1c3af-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3af-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c3af-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3af-135">입력</span><span class="sxs-lookup"><span data-stu-id="1c3af-135">INPUTS</span></span>

### <span data-ttu-id="1c3af-136">없음</span><span class="sxs-lookup"><span data-stu-id="1c3af-136">None</span></span>
## <span data-ttu-id="1c3af-137">출력</span><span class="sxs-lookup"><span data-stu-id="1c3af-137">OUTPUTS</span></span>

### <span data-ttu-id="1c3af-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="1c3af-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="1c3af-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c3af-139">NOTES</span></span>

## <span data-ttu-id="1c3af-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c3af-140">RELATED LINKS</span></span>
