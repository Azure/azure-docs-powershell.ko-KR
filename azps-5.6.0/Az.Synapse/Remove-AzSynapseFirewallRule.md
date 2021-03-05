---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6df0e33ff94be7bf5e060b929206c09180d830f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961088"
---
# <span data-ttu-id="903ca-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="903ca-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="903ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903ca-102">SYNOPSIS</span></span>
<span data-ttu-id="903ca-103">Synapse Analytics 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="903ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="903ca-104">SYNTAX</span></span>

### <span data-ttu-id="903ca-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="903ca-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903ca-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="903ca-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903ca-107">설명</span><span class="sxs-lookup"><span data-stu-id="903ca-107">DESCRIPTION</span></span>
<span data-ttu-id="903ca-108">**Remove-AzSynapseFirewallRule** cmdlet은 Azure Synapse Analytics 방화벽 규칙을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="903ca-109">예제</span><span class="sxs-lookup"><span data-stu-id="903ca-109">EXAMPLES</span></span>

### <span data-ttu-id="903ca-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="903ca-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="903ca-111">이 명령은 ContosoFirewallRule이라는 방화벽 규칙을 작업 영역 ContosoWorkspace에서 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="903ca-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="903ca-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="903ca-113">이 명령은 파이프라인을 통해 작업 영역 아래에 ContosoFirewallRule이라는 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="903ca-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="903ca-114">PARAMETERS</span></span>

### <span data-ttu-id="903ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="903ca-115">-AsJob</span></span>
<span data-ttu-id="903ca-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="903ca-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="903ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903ca-117">-DefaultProfile</span></span>
<span data-ttu-id="903ca-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903ca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="903ca-119">-Force</span></span>
<span data-ttu-id="903ca-120">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="903ca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="903ca-121">-Name</span></span>
<span data-ttu-id="903ca-122">작업 영역의 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="903ca-123">-PassThru</span></span>
<span data-ttu-id="903ca-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="903ca-125">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="903ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="903ca-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ca-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="903ca-128">-WorkspaceName</span></span>
<span data-ttu-id="903ca-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ca-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="903ca-130">-WorkspaceObject</span></span>
<span data-ttu-id="903ca-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="903ca-132">-확인</span><span class="sxs-lookup"><span data-stu-id="903ca-132">-Confirm</span></span>
<span data-ttu-id="903ca-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903ca-134">-WhatIf</span></span>
<span data-ttu-id="903ca-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="903ca-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903ca-137">CommonParameters</span></span>
<span data-ttu-id="903ca-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="903ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903ca-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="903ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903ca-140">입력</span><span class="sxs-lookup"><span data-stu-id="903ca-140">INPUTS</span></span>

### <span data-ttu-id="903ca-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="903ca-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="903ca-142">출력</span><span class="sxs-lookup"><span data-stu-id="903ca-142">OUTPUTS</span></span>

### <span data-ttu-id="903ca-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="903ca-143">System.Boolean</span></span>

## <span data-ttu-id="903ca-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="903ca-144">NOTES</span></span>

## <span data-ttu-id="903ca-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="903ca-145">RELATED LINKS</span></span>
