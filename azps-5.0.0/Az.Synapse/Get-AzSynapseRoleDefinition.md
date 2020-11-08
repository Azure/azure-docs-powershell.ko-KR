---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217963"
---
# <span data-ttu-id="515f1-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="515f1-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="515f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515f1-102">SYNOPSIS</span></span>
<span data-ttu-id="515f1-103">Synapse Analytics 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="515f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="515f1-104">SYNTAX</span></span>

### <span data-ttu-id="515f1-105">GetByWorkspaceNameAndIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="515f1-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="515f1-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="515f1-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="515f1-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="515f1-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="515f1-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="515f1-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="515f1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="515f1-109">DESCRIPTION</span></span>
<span data-ttu-id="515f1-110">**AzSynapseRoleDefinition** Cmdlet은 Azure Synapse Analytics 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="515f1-111">역할 이름 또는 역할 Id를 지정 하지 않으면이 cmdlet은 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="515f1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="515f1-112">EXAMPLES</span></span>

### <span data-ttu-id="515f1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="515f1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="515f1-114">이 명령은 작업 영역 아래에 있는 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="515f1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="515f1-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="515f1-116">이 명령은 name ContosoRole를 사용 하 여 작업 영역 ContosoWorkspace에서 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="515f1-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="515f1-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="515f1-118">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="515f1-119">변수</span><span class="sxs-lookup"><span data-stu-id="515f1-119">PARAMETERS</span></span>

### <span data-ttu-id="515f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515f1-120">-DefaultProfile</span></span>
<span data-ttu-id="515f1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="515f1-122">-Id</span><span class="sxs-lookup"><span data-stu-id="515f1-122">-Id</span></span>
<span data-ttu-id="515f1-123">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="515f1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="515f1-124">-Name</span></span>
<span data-ttu-id="515f1-125">주도자에 게 지정 된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="515f1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="515f1-126">-WorkspaceName</span></span>
<span data-ttu-id="515f1-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="515f1-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="515f1-128">-WorkspaceObject</span></span>
<span data-ttu-id="515f1-129">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="515f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515f1-130">CommonParameters</span></span>
<span data-ttu-id="515f1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="515f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515f1-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="515f1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515f1-133">입력</span><span class="sxs-lookup"><span data-stu-id="515f1-133">INPUTS</span></span>

### <span data-ttu-id="515f1-134">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="515f1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="515f1-135">출력</span><span class="sxs-lookup"><span data-stu-id="515f1-135">OUTPUTS</span></span>

### <span data-ttu-id="515f1-136">Synapse. PSSynapseRole/.</span><span class="sxs-lookup"><span data-stu-id="515f1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="515f1-137">상속자</span><span class="sxs-lookup"><span data-stu-id="515f1-137">NOTES</span></span>

## <span data-ttu-id="515f1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="515f1-138">RELATED LINKS</span></span>
