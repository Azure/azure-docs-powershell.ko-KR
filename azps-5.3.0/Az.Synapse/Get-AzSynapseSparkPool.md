---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383986"
---
# <span data-ttu-id="d330d-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d330d-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="d330d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d330d-102">SYNOPSIS</span></span>
<span data-ttu-id="d330d-103">Synapse Analytics Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d330d-104">구문</span><span class="sxs-lookup"><span data-stu-id="d330d-104">SYNTAX</span></span>

### <span data-ttu-id="d330d-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d330d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d330d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d330d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d330d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d330d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d330d-108">설명</span><span class="sxs-lookup"><span data-stu-id="d330d-108">DESCRIPTION</span></span>
<span data-ttu-id="d330d-109">**Get-AzSynapseSparkPool** cmdlet은 Azure Synapse Analytics Spark 풀에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d330d-110">예제</span><span class="sxs-lookup"><span data-stu-id="d330d-110">EXAMPLES</span></span>

### <span data-ttu-id="d330d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d330d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d330d-112">이 명령은 작업 영역 아래에 있는 모든 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="d330d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d330d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="d330d-114">이 명령은 ContosoSparkPool 이름의 작업 영역 ContosoWorkspace에서 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="d330d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d330d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="d330d-116">이 명령은 파이프라인을 통해 작업 영역의 모든 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="d330d-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="d330d-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="d330d-118">이 명령은 지정된 리소스 ID를 사용하여 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="d330d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d330d-119">PARAMETERS</span></span>

### <span data-ttu-id="d330d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d330d-120">-DefaultProfile</span></span>
<span data-ttu-id="d330d-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d330d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d330d-122">-Name</span></span>
<span data-ttu-id="d330d-123">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d330d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d330d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d330d-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-125">Resource group name.</span></span>

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

### <span data-ttu-id="d330d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d330d-126">-ResourceId</span></span>
<span data-ttu-id="d330d-127">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d330d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d330d-128">-WorkspaceName</span></span>
<span data-ttu-id="d330d-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d330d-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d330d-130">-WorkspaceObject</span></span>
<span data-ttu-id="d330d-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d330d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d330d-132">CommonParameters</span></span>
<span data-ttu-id="d330d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d330d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d330d-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d330d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d330d-135">입력</span><span class="sxs-lookup"><span data-stu-id="d330d-135">INPUTS</span></span>

### <span data-ttu-id="d330d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d330d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d330d-137">출력</span><span class="sxs-lookup"><span data-stu-id="d330d-137">OUTPUTS</span></span>

### <span data-ttu-id="d330d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d330d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="d330d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d330d-139">NOTES</span></span>

## <span data-ttu-id="d330d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d330d-140">RELATED LINKS</span></span>
