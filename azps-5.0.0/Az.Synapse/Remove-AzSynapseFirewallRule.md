---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216603"
---
# <span data-ttu-id="7c51c-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7c51c-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="7c51c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c51c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c51c-103">Synapse Analytics 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7c51c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c51c-104">SYNTAX</span></span>

### <span data-ttu-id="7c51c-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c51c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c51c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c51c-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c51c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c51c-107">DESCRIPTION</span></span>
<span data-ttu-id="7c51c-108">**AzSynapseFirewallRule** Cmdlet은 Azure Synapse Analytics 방화벽 규칙을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7c51c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c51c-109">EXAMPLES</span></span>

### <span data-ttu-id="7c51c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c51c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="7c51c-111">이 명령은 이름 ContosoFirewallRule를 사용 하 여 작업 영역 ContosoWorkspace에서 ContosoFirewallRule 이라는 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="7c51c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c51c-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="7c51c-113">이 명령은 파이프라인을 통해 작업 영역 아래에서 ContosoFirewallRule 이라는 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="7c51c-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c51c-114">PARAMETERS</span></span>

### <span data-ttu-id="7c51c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c51c-115">-AsJob</span></span>
<span data-ttu-id="7c51c-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c51c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c51c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c51c-117">-DefaultProfile</span></span>
<span data-ttu-id="7c51c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c51c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7c51c-119">-Name</span></span>
<span data-ttu-id="7c51c-120">작업 영역에 대 한 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="7c51c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c51c-121">-PassThru</span></span>
<span data-ttu-id="7c51c-122">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7c51c-123">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c51c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c51c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c51c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-125">Resource group name.</span></span>

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

### <span data-ttu-id="7c51c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c51c-126">-WorkspaceName</span></span>
<span data-ttu-id="7c51c-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7c51c-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c51c-128">-WorkspaceObject</span></span>
<span data-ttu-id="7c51c-129">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c51c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7c51c-130">-Confirm</span></span>
<span data-ttu-id="7c51c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c51c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c51c-132">-WhatIf</span></span>
<span data-ttu-id="7c51c-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c51c-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c51c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c51c-135">CommonParameters</span></span>
<span data-ttu-id="7c51c-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c51c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c51c-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c51c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c51c-138">입력</span><span class="sxs-lookup"><span data-stu-id="7c51c-138">INPUTS</span></span>

### <span data-ttu-id="7c51c-139">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7c51c-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7c51c-140">출력</span><span class="sxs-lookup"><span data-stu-id="7c51c-140">OUTPUTS</span></span>

### <span data-ttu-id="7c51c-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7c51c-141">System.Boolean</span></span>

## <span data-ttu-id="7c51c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7c51c-142">NOTES</span></span>

## <span data-ttu-id="7c51c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c51c-143">RELATED LINKS</span></span>
