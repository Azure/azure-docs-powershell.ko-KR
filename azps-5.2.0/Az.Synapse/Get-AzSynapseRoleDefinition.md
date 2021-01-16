---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339153"
---
# <span data-ttu-id="436b3-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="436b3-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="436b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="436b3-102">SYNOPSIS</span></span>
<span data-ttu-id="436b3-103">Synapse Analytics 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="436b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="436b3-104">SYNTAX</span></span>

### <span data-ttu-id="436b3-105">GetByWorkspaceNameAndIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="436b3-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="436b3-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="436b3-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="436b3-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="436b3-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="436b3-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="436b3-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="436b3-109">설명</span><span class="sxs-lookup"><span data-stu-id="436b3-109">DESCRIPTION</span></span>
<span data-ttu-id="436b3-110">**Get-AzSynapseRoleDefinition** cmdlet은 Azure Synapse 분석 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="436b3-111">역할 이름 또는 역할 ID를 지정하지 않으면 이 cmdlet은 모든 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="436b3-112">예제</span><span class="sxs-lookup"><span data-stu-id="436b3-112">EXAMPLES</span></span>

### <span data-ttu-id="436b3-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="436b3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="436b3-114">이 명령은 작업 영역의 모든 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="436b3-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="436b3-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="436b3-116">이 명령은 ContosoRole 이름의 작업 영역 ContosoWorkspace에서 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="436b3-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="436b3-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="436b3-118">이 명령은 파이프라인을 통해 작업 영역의 모든 역할 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="436b3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="436b3-119">PARAMETERS</span></span>

### <span data-ttu-id="436b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436b3-120">-DefaultProfile</span></span>
<span data-ttu-id="436b3-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="436b3-122">-Id</span><span class="sxs-lookup"><span data-stu-id="436b3-122">-Id</span></span>
<span data-ttu-id="436b3-123">보안 주체에 할당된 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436b3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="436b3-124">-Name</span></span>
<span data-ttu-id="436b3-125">보안 주체에 할당된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436b3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="436b3-126">-WorkspaceName</span></span>
<span data-ttu-id="436b3-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436b3-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="436b3-128">-WorkspaceObject</span></span>
<span data-ttu-id="436b3-129">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="436b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436b3-130">CommonParameters</span></span>
<span data-ttu-id="436b3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="436b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436b3-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="436b3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436b3-133">입력</span><span class="sxs-lookup"><span data-stu-id="436b3-133">INPUTS</span></span>

### <span data-ttu-id="436b3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="436b3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="436b3-135">출력</span><span class="sxs-lookup"><span data-stu-id="436b3-135">OUTPUTS</span></span>

### <span data-ttu-id="436b3-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="436b3-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="436b3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="436b3-137">NOTES</span></span>

## <span data-ttu-id="436b3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="436b3-138">RELATED LINKS</span></span>
