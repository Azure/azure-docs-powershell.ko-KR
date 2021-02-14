---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188804"
---
# <span data-ttu-id="77fba-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="77fba-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="77fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fba-102">SYNOPSIS</span></span>
<span data-ttu-id="77fba-103">Synapse Analytics Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="77fba-104">구문</span><span class="sxs-lookup"><span data-stu-id="77fba-104">SYNTAX</span></span>

### <span data-ttu-id="77fba-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="77fba-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77fba-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fba-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77fba-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fba-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77fba-108">설명</span><span class="sxs-lookup"><span data-stu-id="77fba-108">DESCRIPTION</span></span>
<span data-ttu-id="77fba-109">**Get-AzSynapseSparkPool** cmdlet은 Azure Synapse Analytics Spark 풀에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="77fba-110">예제</span><span class="sxs-lookup"><span data-stu-id="77fba-110">EXAMPLES</span></span>

### <span data-ttu-id="77fba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="77fba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="77fba-112">이 명령은 작업 영역 아래에 있는 모든 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="77fba-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="77fba-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="77fba-114">이 명령은 ContosoSparkPool 이름의 작업 영역 ContosoWorkspace에서 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="77fba-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="77fba-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="77fba-116">이 명령은 파이프라인을 통해 작업 영역의 모든 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="77fba-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="77fba-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="77fba-118">이 명령은 지정된 리소스 ID를 사용하여 Spark 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="77fba-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77fba-119">PARAMETERS</span></span>

### <span data-ttu-id="77fba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fba-120">-DefaultProfile</span></span>
<span data-ttu-id="77fba-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77fba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="77fba-122">-Name</span></span>
<span data-ttu-id="77fba-123">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="77fba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fba-124">-ResourceGroupName</span></span>
<span data-ttu-id="77fba-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-125">Resource group name.</span></span>

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

### <span data-ttu-id="77fba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77fba-126">-ResourceId</span></span>
<span data-ttu-id="77fba-127">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="77fba-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="77fba-128">-WorkspaceName</span></span>
<span data-ttu-id="77fba-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="77fba-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="77fba-130">-WorkspaceObject</span></span>
<span data-ttu-id="77fba-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="77fba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fba-132">CommonParameters</span></span>
<span data-ttu-id="77fba-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77fba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fba-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77fba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fba-135">입력</span><span class="sxs-lookup"><span data-stu-id="77fba-135">INPUTS</span></span>

### <span data-ttu-id="77fba-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="77fba-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="77fba-137">출력</span><span class="sxs-lookup"><span data-stu-id="77fba-137">OUTPUTS</span></span>

### <span data-ttu-id="77fba-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="77fba-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="77fba-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77fba-139">NOTES</span></span>

## <span data-ttu-id="77fba-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77fba-140">RELATED LINKS</span></span>
