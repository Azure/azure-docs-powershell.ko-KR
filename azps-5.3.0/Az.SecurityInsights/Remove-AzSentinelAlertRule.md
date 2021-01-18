---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494925"
---
# <span data-ttu-id="522b7-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="522b7-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="522b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="522b7-102">SYNOPSIS</span></span>
<span data-ttu-id="522b7-103">분석 데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-103">Delete an Analytic.</span></span>

## <span data-ttu-id="522b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="522b7-104">SYNTAX</span></span>

### <span data-ttu-id="522b7-105">AlertRuleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="522b7-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522b7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="522b7-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="522b7-107">DESCRIPTION</span></span>
<span data-ttu-id="522b7-108">**Remove-AzSentinelAlertRule** cmdlet은 지정된 작업 영역의 경고 규칙을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="522b7-109">파이프라인 연산자를 사용하여 **AlertRule** 개체를 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="522b7-110">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="522b7-111">예제</span><span class="sxs-lookup"><span data-stu-id="522b7-111">EXAMPLES</span></span>

### <span data-ttu-id="522b7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="522b7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="522b7-113">이 명령은 작업 영역의 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="522b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="522b7-114">PARAMETERS</span></span>

### <span data-ttu-id="522b7-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="522b7-115">-AlertRuleId</span></span>
<span data-ttu-id="522b7-116">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522b7-117">-DefaultProfile</span></span>
<span data-ttu-id="522b7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="522b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="522b7-119">-InputObject</span></span>
<span data-ttu-id="522b7-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="522b7-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522b7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="522b7-121">-PassThru</span></span>
<span data-ttu-id="522b7-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="522b7-122">PassThru</span></span>

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

### <span data-ttu-id="522b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="522b7-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522b7-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="522b7-125">-WorkspaceName</span></span>
<span data-ttu-id="522b7-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522b7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="522b7-127">-Confirm</span></span>
<span data-ttu-id="522b7-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="522b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522b7-129">-WhatIf</span></span>
<span data-ttu-id="522b7-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="522b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="522b7-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="522b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522b7-132">CommonParameters</span></span>
<span data-ttu-id="522b7-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="522b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522b7-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="522b7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522b7-135">입력</span><span class="sxs-lookup"><span data-stu-id="522b7-135">INPUTS</span></span>

### <span data-ttu-id="522b7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="522b7-136">System.String</span></span>
### <span data-ttu-id="522b7-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="522b7-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="522b7-138">출력</span><span class="sxs-lookup"><span data-stu-id="522b7-138">OUTPUTS</span></span>

### <span data-ttu-id="522b7-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="522b7-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="522b7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="522b7-140">NOTES</span></span>

## <span data-ttu-id="522b7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="522b7-141">RELATED LINKS</span></span>
