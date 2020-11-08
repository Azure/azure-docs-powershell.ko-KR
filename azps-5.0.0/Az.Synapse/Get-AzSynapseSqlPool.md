---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216610"
---
# <span data-ttu-id="fc49e-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fc49e-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="fc49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc49e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc49e-103">Synapse Analytics SQL 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fc49e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc49e-104">SYNTAX</span></span>

### <span data-ttu-id="fc49e-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc49e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc49e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc49e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc49e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc49e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc49e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fc49e-108">DESCRIPTION</span></span>
<span data-ttu-id="fc49e-109">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fc49e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc49e-110">EXAMPLES</span></span>

### <span data-ttu-id="fc49e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc49e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fc49e-112">이 명령은 작업 영역 아래에 있는 모든 SQL 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="fc49e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fc49e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fc49e-114">이 명령은 name ContosoSqlPool를 사용 하 여 작업 영역 ContosoWorkspace에서 SQL 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="fc49e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="fc49e-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="fc49e-116">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 SQL 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="fc49e-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="fc49e-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="fc49e-118">이 명령은 지정 된 리소스 ID를 사용 하 여 SQL 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="fc49e-119">변수</span><span class="sxs-lookup"><span data-stu-id="fc49e-119">PARAMETERS</span></span>

### <span data-ttu-id="fc49e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc49e-120">-DefaultProfile</span></span>
<span data-ttu-id="fc49e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc49e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fc49e-122">-Name</span></span>
<span data-ttu-id="fc49e-123">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fc49e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc49e-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc49e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-125">Resource group name.</span></span>

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

### <span data-ttu-id="fc49e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc49e-126">-ResourceId</span></span>
<span data-ttu-id="fc49e-127">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="fc49e-128">-버전</span><span class="sxs-lookup"><span data-stu-id="fc49e-128">-Version</span></span>
<span data-ttu-id="fc49e-129">[이 기능은 제한 된 미리 보기에 있으며, 처음에는 특정 플랜에만 액세스할 수 있습니다.] Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="fc49e-130">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="fc49e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fc49e-131">-WorkspaceName</span></span>
<span data-ttu-id="fc49e-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fc49e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fc49e-133">-WorkspaceObject</span></span>
<span data-ttu-id="fc49e-134">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fc49e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc49e-135">CommonParameters</span></span>
<span data-ttu-id="fc49e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc49e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc49e-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc49e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc49e-138">입력</span><span class="sxs-lookup"><span data-stu-id="fc49e-138">INPUTS</span></span>

### <span data-ttu-id="fc49e-139">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="fc49e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fc49e-140">출력</span><span class="sxs-lookup"><span data-stu-id="fc49e-140">OUTPUTS</span></span>

### <span data-ttu-id="fc49e-141">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="fc49e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fc49e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="fc49e-142">NOTES</span></span>

## <span data-ttu-id="fc49e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc49e-143">RELATED LINKS</span></span>
