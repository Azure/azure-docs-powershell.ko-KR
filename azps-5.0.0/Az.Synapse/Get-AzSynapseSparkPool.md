---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309817"
---
# <span data-ttu-id="7f595-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7f595-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="7f595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f595-102">SYNOPSIS</span></span>
<span data-ttu-id="7f595-103">Synapse Analytics Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="7f595-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f595-104">SYNTAX</span></span>

### <span data-ttu-id="7f595-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f595-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f595-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f595-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f595-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f595-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f595-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7f595-108">DESCRIPTION</span></span>
<span data-ttu-id="7f595-109">**AzSynapseSparkPool** Cmdlet은 Azure Synapse Analytics Spark 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="7f595-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7f595-110">EXAMPLES</span></span>

### <span data-ttu-id="7f595-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f595-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7f595-112">이 명령은 작업 영역 아래에 있는 모든 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="7f595-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7f595-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="7f595-114">이 명령은 name ContosoSparkPool를 사용 하 여 workspace ContosoWorkspace의 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="7f595-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7f595-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="7f595-116">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="7f595-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="7f595-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="7f595-118">이 명령은 지정 된 리소스 ID를 갖는 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="7f595-119">변수</span><span class="sxs-lookup"><span data-stu-id="7f595-119">PARAMETERS</span></span>

### <span data-ttu-id="7f595-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f595-120">-DefaultProfile</span></span>
<span data-ttu-id="7f595-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f595-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7f595-122">-Name</span></span>
<span data-ttu-id="7f595-123">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7f595-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f595-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f595-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-125">Resource group name.</span></span>

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

### <span data-ttu-id="7f595-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f595-126">-ResourceId</span></span>
<span data-ttu-id="7f595-127">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7f595-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f595-128">-WorkspaceName</span></span>
<span data-ttu-id="7f595-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7f595-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f595-130">-WorkspaceObject</span></span>
<span data-ttu-id="7f595-131">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7f595-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f595-132">CommonParameters</span></span>
<span data-ttu-id="7f595-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f595-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f595-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f595-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f595-135">입력</span><span class="sxs-lookup"><span data-stu-id="7f595-135">INPUTS</span></span>

### <span data-ttu-id="7f595-136">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7f595-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7f595-137">출력</span><span class="sxs-lookup"><span data-stu-id="7f595-137">OUTPUTS</span></span>

### <span data-ttu-id="7f595-138">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="7f595-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="7f595-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7f595-139">NOTES</span></span>

## <span data-ttu-id="7f595-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f595-140">RELATED LINKS</span></span>
