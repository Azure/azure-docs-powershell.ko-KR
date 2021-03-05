---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015680"
---
# <span data-ttu-id="90305-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="90305-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="90305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90305-102">SYNOPSIS</span></span>
<span data-ttu-id="90305-103">Synapse Analytics SQL 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="90305-104">구문</span><span class="sxs-lookup"><span data-stu-id="90305-104">SYNTAX</span></span>

### <span data-ttu-id="90305-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="90305-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90305-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90305-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90305-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90305-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90305-108">설명</span><span class="sxs-lookup"><span data-stu-id="90305-108">DESCRIPTION</span></span>
<span data-ttu-id="90305-109">**Get-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="90305-110">예제</span><span class="sxs-lookup"><span data-stu-id="90305-110">EXAMPLES</span></span>

### <span data-ttu-id="90305-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="90305-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="90305-112">이 명령은 작업 SQL 모든 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="90305-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="90305-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="90305-114">이 명령은 contosoSqlPool 이름이 SQL ContosoWorkspace에서 SQL 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="90305-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="90305-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="90305-116">이 명령은 파이프라인을 통해 작업 SQL 모든 SQL 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="90305-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="90305-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="90305-118">이 명령은 지정된 SQL 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90305-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="90305-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90305-119">PARAMETERS</span></span>

### <span data-ttu-id="90305-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90305-120">-DefaultProfile</span></span>
<span data-ttu-id="90305-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90305-122">-Name</span><span class="sxs-lookup"><span data-stu-id="90305-122">-Name</span></span>
<span data-ttu-id="90305-123">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90305-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90305-124">-ResourceGroupName</span></span>
<span data-ttu-id="90305-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-125">Resource group name.</span></span>

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

### <span data-ttu-id="90305-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90305-126">-ResourceId</span></span>
<span data-ttu-id="90305-127">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="90305-128">-Version</span><span class="sxs-lookup"><span data-stu-id="90305-128">-Version</span></span>
<span data-ttu-id="90305-129">[이 기능은 제한된 미리 보기에 있습니다. 처음에는 특정 구독에만 액세스할 수 있습니다.] Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="90305-130">예를 들어 2 또는 3.</span><span class="sxs-lookup"><span data-stu-id="90305-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90305-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="90305-131">-WorkspaceName</span></span>
<span data-ttu-id="90305-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="90305-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="90305-133">-WorkspaceObject</span></span>
<span data-ttu-id="90305-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="90305-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="90305-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90305-135">CommonParameters</span></span>
<span data-ttu-id="90305-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90305-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90305-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90305-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90305-138">입력</span><span class="sxs-lookup"><span data-stu-id="90305-138">INPUTS</span></span>

### <span data-ttu-id="90305-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="90305-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="90305-140">출력</span><span class="sxs-lookup"><span data-stu-id="90305-140">OUTPUTS</span></span>

### <span data-ttu-id="90305-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="90305-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="90305-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90305-142">NOTES</span></span>

## <span data-ttu-id="90305-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90305-143">RELATED LINKS</span></span>
