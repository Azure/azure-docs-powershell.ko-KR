---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339182"
---
# <span data-ttu-id="e2250-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="e2250-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="e2250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2250-102">SYNOPSIS</span></span>
<span data-ttu-id="e2250-103">작업 영역의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="e2250-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2250-104">SYNTAX</span></span>

### <span data-ttu-id="e2250-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2250-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2250-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e2250-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2250-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2250-107">DESCRIPTION</span></span>
<span data-ttu-id="e2250-108">**Get-AzSynapsePipeline** cmdlet은 작업 영역의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="e2250-109">파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="e2250-110">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="e2250-111">예제</span><span class="sxs-lookup"><span data-stu-id="e2250-111">EXAMPLES</span></span>

### <span data-ttu-id="e2250-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2250-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e2250-113">이 명령은 ContosoWorkspace라는 작업 영역의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e2250-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="e2250-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="e2250-115">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoPipeline 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e2250-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="e2250-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="e2250-117">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 ContosoPipeline이라는 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e2250-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2250-118">PARAMETERS</span></span>

### <span data-ttu-id="e2250-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2250-119">-DefaultProfile</span></span>
<span data-ttu-id="e2250-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2250-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2250-121">-Name</span></span>
<span data-ttu-id="e2250-122">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2250-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2250-123">-WorkspaceName</span></span>
<span data-ttu-id="e2250-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2250-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2250-125">-WorkspaceObject</span></span>
<span data-ttu-id="e2250-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2250-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2250-127">CommonParameters</span></span>
<span data-ttu-id="e2250-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2250-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2250-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2250-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2250-130">입력</span><span class="sxs-lookup"><span data-stu-id="e2250-130">INPUTS</span></span>

### <span data-ttu-id="e2250-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2250-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e2250-132">출력</span><span class="sxs-lookup"><span data-stu-id="e2250-132">OUTPUTS</span></span>

### <span data-ttu-id="e2250-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="e2250-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="e2250-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2250-134">NOTES</span></span>

## <span data-ttu-id="e2250-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2250-135">RELATED LINKS</span></span>
