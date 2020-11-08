---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204188"
---
# <span data-ttu-id="02bcd-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="02bcd-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="02bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="02bcd-103">Synapse Analytics 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="02bcd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">SYNTAX</span></span>

### <span data-ttu-id="02bcd-105">GetByWorkspaceNameAndIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02bcd-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02bcd-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02bcd-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02bcd-109">설명은</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">DESCRIPTION</span></span>
<span data-ttu-id="02bcd-110">**AzSynapseRoleDefinition** Cmdlet은 Azure Synapse Analytics 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="02bcd-111">역할 이름 또는 역할 Id를 지정 하지 않으면이 cmdlet은 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="02bcd-112">예제의</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">EXAMPLES</span></span>

### <span data-ttu-id="02bcd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="02bcd-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="02bcd-114">이 명령은 작업 영역 아래에 있는 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="02bcd-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="02bcd-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="02bcd-116">이 명령은 name ContosoRole를 사용 하 여 작업 영역 ContosoWorkspace에서 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="02bcd-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="02bcd-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="02bcd-118">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 역할 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="02bcd-119">변수</span><span class="sxs-lookup"><span data-stu-id="02bcd-119">PARAMETERS</span></span>

### <span data-ttu-id="02bcd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02bcd-120">-DefaultProfile</span></span>
<span data-ttu-id="02bcd-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02bcd-122">-Id</span><span class="sxs-lookup"><span data-stu-id="02bcd-122">-Id</span></span>
<span data-ttu-id="02bcd-123">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="02bcd-124">-이름</span><span class="sxs-lookup"><span data-stu-id="02bcd-124">-Name</span></span>
<span data-ttu-id="02bcd-125">주도자에 게 지정 된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="02bcd-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02bcd-126">-WorkspaceName</span></span>
<span data-ttu-id="02bcd-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="02bcd-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="02bcd-128">-WorkspaceObject</span></span>
<span data-ttu-id="02bcd-129">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="02bcd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02bcd-130">CommonParameters</span></span>
<span data-ttu-id="02bcd-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02bcd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02bcd-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="02bcd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02bcd-133">입력</span><span class="sxs-lookup"><span data-stu-id="02bcd-133">INPUTS</span></span>

### <span data-ttu-id="02bcd-134">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="02bcd-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="02bcd-135">출력</span><span class="sxs-lookup"><span data-stu-id="02bcd-135">OUTPUTS</span></span>

### <span data-ttu-id="02bcd-136">Synapse. PSSynapseRole/.</span><span class="sxs-lookup"><span data-stu-id="02bcd-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="02bcd-137">상속자</span><span class="sxs-lookup"><span data-stu-id="02bcd-137">NOTES</span></span>

## <span data-ttu-id="02bcd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02bcd-138">RELATED LINKS</span></span>
