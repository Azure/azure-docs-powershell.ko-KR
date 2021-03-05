---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963632"
---
# <span data-ttu-id="50afe-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="50afe-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="50afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50afe-102">SYNOPSIS</span></span>
<span data-ttu-id="50afe-103">분석에서 자동화된 응답을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="50afe-104">구문</span><span class="sxs-lookup"><span data-stu-id="50afe-104">SYNTAX</span></span>

### <span data-ttu-id="50afe-105">ActionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="50afe-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50afe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50afe-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50afe-107">설명</span><span class="sxs-lookup"><span data-stu-id="50afe-107">DESCRIPTION</span></span>
<span data-ttu-id="50afe-108">**Remove-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역의 경고 규칙에서 자동화된 응답을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="50afe-109">파이프라인 연산자를 사용하여 **AlertRuleAction** 개체를 전달하거나 또는 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="50afe-110">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="50afe-111">예제</span><span class="sxs-lookup"><span data-stu-id="50afe-111">EXAMPLES</span></span>

### <span data-ttu-id="50afe-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="50afe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="50afe-113">이 명령은 작업 영역에서 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="50afe-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50afe-114">PARAMETERS</span></span>

### <span data-ttu-id="50afe-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="50afe-115">-ActionId</span></span>
<span data-ttu-id="50afe-116">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-116">Action Id.</span></span>

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

### <span data-ttu-id="50afe-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="50afe-117">-AlertRuleId</span></span>
<span data-ttu-id="50afe-118">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50afe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50afe-119">-DefaultProfile</span></span>
<span data-ttu-id="50afe-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50afe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50afe-121">-InputObject</span></span>
<span data-ttu-id="50afe-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="50afe-122">InputObject.</span></span>

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

### <span data-ttu-id="50afe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50afe-123">-PassThru</span></span>
<span data-ttu-id="50afe-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="50afe-124">PassThru</span></span>

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

### <span data-ttu-id="50afe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50afe-125">-ResourceGroupName</span></span>
<span data-ttu-id="50afe-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50afe-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50afe-127">-WorkspaceName</span></span>
<span data-ttu-id="50afe-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50afe-129">-확인</span><span class="sxs-lookup"><span data-stu-id="50afe-129">-Confirm</span></span>
<span data-ttu-id="50afe-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50afe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50afe-131">-WhatIf</span></span>
<span data-ttu-id="50afe-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50afe-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50afe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50afe-134">CommonParameters</span></span>
<span data-ttu-id="50afe-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50afe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50afe-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50afe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50afe-137">입력</span><span class="sxs-lookup"><span data-stu-id="50afe-137">INPUTS</span></span>

### <span data-ttu-id="50afe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="50afe-138">System.String</span></span>
### <span data-ttu-id="50afe-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="50afe-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="50afe-140">출력</span><span class="sxs-lookup"><span data-stu-id="50afe-140">OUTPUTS</span></span>

### <span data-ttu-id="50afe-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="50afe-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="50afe-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50afe-142">NOTES</span></span>

## <span data-ttu-id="50afe-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50afe-143">RELATED LINKS</span></span>
