---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: 56674f2696e5d7cebdaa9f84072f890c69535223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015691"
---
# <span data-ttu-id="11730-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="11730-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="11730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11730-102">SYNOPSIS</span></span>
<span data-ttu-id="11730-103">Synapse Analytics SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11730-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="11730-104">구문</span><span class="sxs-lookup"><span data-stu-id="11730-104">SYNTAX</span></span>

### <span data-ttu-id="11730-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="11730-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11730-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11730-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11730-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11730-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11730-108">설명</span><span class="sxs-lookup"><span data-stu-id="11730-108">DESCRIPTION</span></span>
<span data-ttu-id="11730-109">[이 기능은 제한된 미리 보기에 있습니다. 처음에는 특정 구독에만 액세스할 수 있습니다.] **Get-AzSynapseSqlDatabase** cmdlet은 Azure Synapse Analytics SQL 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11730-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="11730-110">예제</span><span class="sxs-lookup"><span data-stu-id="11730-110">EXAMPLES</span></span>

### <span data-ttu-id="11730-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="11730-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="11730-112">이 명령은 작업 SQL 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11730-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="11730-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="11730-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="11730-114">이 명령은 contosoSqlDatabase 이름으로 SQL ContosoWorkspace에서 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11730-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="11730-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="11730-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="11730-116">이 명령은 파이프라인을 통해 작업 SQL 모든 데이터베이스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11730-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="11730-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="11730-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="11730-118">이 명령은 지정된 SQL 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11730-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="11730-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11730-119">PARAMETERS</span></span>

### <span data-ttu-id="11730-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11730-120">-DefaultProfile</span></span>
<span data-ttu-id="11730-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11730-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11730-122">-Name</span><span class="sxs-lookup"><span data-stu-id="11730-122">-Name</span></span>
<span data-ttu-id="11730-123">Synapse 데이터베이스의 SQL.</span><span class="sxs-lookup"><span data-stu-id="11730-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11730-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11730-124">-ResourceGroupName</span></span>
<span data-ttu-id="11730-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11730-125">Resource group name.</span></span>

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

### <span data-ttu-id="11730-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11730-126">-ResourceId</span></span>
<span data-ttu-id="11730-127">데이터베이스의 Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11730-127">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11730-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11730-128">-WorkspaceName</span></span>
<span data-ttu-id="11730-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11730-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="11730-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11730-130">-WorkspaceObject</span></span>
<span data-ttu-id="11730-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11730-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="11730-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11730-132">CommonParameters</span></span>
<span data-ttu-id="11730-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11730-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11730-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11730-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11730-135">입력</span><span class="sxs-lookup"><span data-stu-id="11730-135">INPUTS</span></span>

### <span data-ttu-id="11730-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11730-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="11730-137">출력</span><span class="sxs-lookup"><span data-stu-id="11730-137">OUTPUTS</span></span>

### <span data-ttu-id="11730-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="11730-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="11730-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11730-139">NOTES</span></span>

## <span data-ttu-id="11730-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11730-140">RELATED LINKS</span></span>
