---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047482"
---
# <span data-ttu-id="2eb4c-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2eb4c-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="2eb4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb4c-103">Synapse Analytics 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="2eb4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2eb4c-104">SYNTAX</span></span>

### <span data-ttu-id="2eb4c-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2eb4c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb4c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eb4c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb4c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2eb4c-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb4c-108">**AzSynapseFirewallRule** Cmdlet은 Azure Synapse Analytics 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="2eb4c-109">규칙 이름을 지정 하지 않으면이 cmdlet은 모든 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="2eb4c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2eb4c-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb4c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2eb4c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2eb4c-112">이 명령은 작업 영역 아래에 있는 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="2eb4c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2eb4c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="2eb4c-114">이 명령은 name ContosoFirewallRule를 사용 하 여 작업 영역 ContosoWorkspace에서 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="2eb4c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="2eb4c-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="2eb4c-116">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="2eb4c-117">변수</span><span class="sxs-lookup"><span data-stu-id="2eb4c-117">PARAMETERS</span></span>

### <span data-ttu-id="2eb4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb4c-118">-DefaultProfile</span></span>
<span data-ttu-id="2eb4c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb4c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2eb4c-120">-Name</span></span>
<span data-ttu-id="2eb4c-121">작업 영역에 대 한 firerwall 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="2eb4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2eb4c-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-123">Resource group name.</span></span>

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

### <span data-ttu-id="2eb4c-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2eb4c-124">-WorkspaceName</span></span>
<span data-ttu-id="2eb4c-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2eb4c-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="2eb4c-126">-WorkSpaceObject</span></span>
<span data-ttu-id="2eb4c-127">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2eb4c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb4c-128">CommonParameters</span></span>
<span data-ttu-id="2eb4c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb4c-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb4c-131">입력</span><span class="sxs-lookup"><span data-stu-id="2eb4c-131">INPUTS</span></span>

### <span data-ttu-id="2eb4c-132">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2eb4c-133">출력</span><span class="sxs-lookup"><span data-stu-id="2eb4c-133">OUTPUTS</span></span>

### <span data-ttu-id="2eb4c-134">Synapse. PSSynapseIpFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="2eb4c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="2eb4c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2eb4c-135">NOTES</span></span>

## <span data-ttu-id="2eb4c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2eb4c-136">RELATED LINKS</span></span>
