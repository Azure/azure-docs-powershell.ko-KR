---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201708"
---
# <span data-ttu-id="380a9-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="380a9-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="380a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380a9-102">SYNOPSIS</span></span>
<span data-ttu-id="380a9-103">분석에서 자동화된 응답을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="380a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="380a9-104">SYNTAX</span></span>

### <span data-ttu-id="380a9-105">ActionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="380a9-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="380a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="380a9-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="380a9-107">DESCRIPTION</span></span>
<span data-ttu-id="380a9-108">**Remove-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역의 경고 규칙에서 자동화된 응답을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="380a9-109">파이프라인 연산자를 사용하여 **AlertRuleAction** 개체를 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="380a9-110">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="380a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="380a9-111">EXAMPLES</span></span>

### <span data-ttu-id="380a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="380a9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="380a9-113">이 명령은 작업 영역의 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="380a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="380a9-114">PARAMETERS</span></span>

### <span data-ttu-id="380a9-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="380a9-115">-ActionId</span></span>
<span data-ttu-id="380a9-116">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-116">Action Id.</span></span>

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

### <span data-ttu-id="380a9-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="380a9-117">-AlertRuleId</span></span>
<span data-ttu-id="380a9-118">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="380a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380a9-119">-DefaultProfile</span></span>
<span data-ttu-id="380a9-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="380a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="380a9-121">-InputObject</span></span>
<span data-ttu-id="380a9-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="380a9-122">InputObject.</span></span>

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

### <span data-ttu-id="380a9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="380a9-123">-PassThru</span></span>
<span data-ttu-id="380a9-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="380a9-124">PassThru</span></span>

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

### <span data-ttu-id="380a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="380a9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-126">Resource group name.</span></span>

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

### <span data-ttu-id="380a9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="380a9-127">-WorkspaceName</span></span>
<span data-ttu-id="380a9-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-128">Workspace Name.</span></span>

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

### <span data-ttu-id="380a9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="380a9-129">-Confirm</span></span>
<span data-ttu-id="380a9-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="380a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380a9-131">-WhatIf</span></span>
<span data-ttu-id="380a9-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="380a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380a9-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="380a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380a9-134">CommonParameters</span></span>
<span data-ttu-id="380a9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="380a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380a9-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="380a9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380a9-137">입력</span><span class="sxs-lookup"><span data-stu-id="380a9-137">INPUTS</span></span>

### <span data-ttu-id="380a9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="380a9-138">System.String</span></span>
### <span data-ttu-id="380a9-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="380a9-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="380a9-140">출력</span><span class="sxs-lookup"><span data-stu-id="380a9-140">OUTPUTS</span></span>

### <span data-ttu-id="380a9-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="380a9-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="380a9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="380a9-142">NOTES</span></span>

## <span data-ttu-id="380a9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="380a9-143">RELATED LINKS</span></span>
