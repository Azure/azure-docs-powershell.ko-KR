---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 71622fbfa60a8961f10346aa9197b2c019f31bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981824"
---
# <span data-ttu-id="8d799-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8d799-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="8d799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d799-102">SYNOPSIS</span></span>
<span data-ttu-id="8d799-103">Synapse Analytics 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8d799-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d799-104">SYNTAX</span></span>

### <span data-ttu-id="8d799-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8d799-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d799-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d799-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d799-107">설명</span><span class="sxs-lookup"><span data-stu-id="8d799-107">DESCRIPTION</span></span>
<span data-ttu-id="8d799-108">**Get-AzSynapseFirewallRule** cmdlet은 Azure Synapse Analytics 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="8d799-109">규칙 이름을 지정하지 않으면 이 cmdlet은 모든 규칙을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="8d799-110">예제</span><span class="sxs-lookup"><span data-stu-id="8d799-110">EXAMPLES</span></span>

### <span data-ttu-id="8d799-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d799-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8d799-112">이 명령은 작업 영역 아래에서 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="8d799-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d799-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="8d799-114">이 명령은 ContosoFirewallRule 이름이 있는 작업 영역 ContosoWorkspace에서 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="8d799-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="8d799-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="8d799-116">이 명령은 파이프라인을 통해 작업 영역 아래에서 모든 방화벽 규칙을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="8d799-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8d799-117">PARAMETERS</span></span>

### <span data-ttu-id="8d799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d799-118">-DefaultProfile</span></span>
<span data-ttu-id="8d799-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d799-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8d799-120">-Name</span></span>
<span data-ttu-id="8d799-121">작업 영역의 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d799-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d799-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d799-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d799-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8d799-124">-WorkspaceName</span></span>
<span data-ttu-id="8d799-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d799-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="8d799-126">-WorkSpaceObject</span></span>
<span data-ttu-id="8d799-127">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d799-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d799-128">CommonParameters</span></span>
<span data-ttu-id="8d799-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d799-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d799-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d799-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d799-131">입력</span><span class="sxs-lookup"><span data-stu-id="8d799-131">INPUTS</span></span>

### <span data-ttu-id="8d799-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d799-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8d799-133">출력</span><span class="sxs-lookup"><span data-stu-id="8d799-133">OUTPUTS</span></span>

### <span data-ttu-id="8d799-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8d799-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="8d799-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d799-135">NOTES</span></span>

## <span data-ttu-id="8d799-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d799-136">RELATED LINKS</span></span>
