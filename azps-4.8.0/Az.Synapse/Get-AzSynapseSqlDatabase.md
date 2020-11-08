---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204186"
---
# <span data-ttu-id="2853e-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2853e-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="2853e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2853e-102">SYNOPSIS</span></span>
<span data-ttu-id="2853e-103">Synapse Analytics SQL 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="2853e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2853e-104">SYNTAX</span></span>

### <span data-ttu-id="2853e-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2853e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2853e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2853e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2853e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2853e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2853e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2853e-108">DESCRIPTION</span></span>
<span data-ttu-id="2853e-109">[이 기능은 제한 된 미리 보기에 있으며, 처음에는 특정 플랜에만 액세스할 수 있습니다.] **AzSynapseSqlDatabase** Cmdlet은 Azure SYNAPSE Analytics SQL 데이터베이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="2853e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2853e-110">EXAMPLES</span></span>

### <span data-ttu-id="2853e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2853e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2853e-112">이 명령은 작업 영역 아래에 있는 모든 SQL 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="2853e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2853e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="2853e-114">이 명령은 name ContosoSqlDatabase를 사용 하 여 작업 영역 ContosoWorkspace에서 SQL 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="2853e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="2853e-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="2853e-116">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 SQL 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="2853e-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="2853e-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="2853e-118">이 명령은 지정 된 리소스 ID를 사용 하 여 SQL 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="2853e-119">변수</span><span class="sxs-lookup"><span data-stu-id="2853e-119">PARAMETERS</span></span>

### <span data-ttu-id="2853e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2853e-120">-DefaultProfile</span></span>
<span data-ttu-id="2853e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2853e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2853e-122">-Name</span></span>
<span data-ttu-id="2853e-123">Synapse SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="2853e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2853e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2853e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-125">Resource group name.</span></span>

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

### <span data-ttu-id="2853e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2853e-126">-ResourceId</span></span>
<span data-ttu-id="2853e-127">Synapse SQL 데이터베이스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="2853e-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2853e-128">-WorkspaceName</span></span>
<span data-ttu-id="2853e-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2853e-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2853e-130">-WorkspaceObject</span></span>
<span data-ttu-id="2853e-131">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2853e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2853e-132">CommonParameters</span></span>
<span data-ttu-id="2853e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2853e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2853e-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2853e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2853e-135">입력</span><span class="sxs-lookup"><span data-stu-id="2853e-135">INPUTS</span></span>

### <span data-ttu-id="2853e-136">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="2853e-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2853e-137">출력</span><span class="sxs-lookup"><span data-stu-id="2853e-137">OUTPUTS</span></span>

### <span data-ttu-id="2853e-138">Synapse. PSSynapseSqlDatabase/.</span><span class="sxs-lookup"><span data-stu-id="2853e-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="2853e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2853e-139">NOTES</span></span>

## <span data-ttu-id="2853e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2853e-140">RELATED LINKS</span></span>
