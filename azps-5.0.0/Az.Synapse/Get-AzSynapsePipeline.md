---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218455"
---
# <span data-ttu-id="b9f6a-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="b9f6a-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="b9f6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f6a-103">작업 영역의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="b9f6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9f6a-104">SYNTAX</span></span>

### <span data-ttu-id="b9f6a-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9f6a-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9f6a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b9f6a-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f6a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="b9f6a-108">**AzSynapsePipeline** cmdlet은 작업 영역의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="b9f6a-109">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="b9f6a-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="b9f6a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b9f6a-111">EXAMPLES</span></span>

### <span data-ttu-id="b9f6a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9f6a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b9f6a-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b9f6a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9f6a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="b9f6a-115">이 명령은 ContosoWorkspace 이라는 작업 영역의 ContosoPipeline 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b9f6a-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="b9f6a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="b9f6a-117">이 명령은 ContosoWorkspace ~ 파이프라인 이라는 작업 영역의 ContosoPipeline 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b9f6a-118">변수</span><span class="sxs-lookup"><span data-stu-id="b9f6a-118">PARAMETERS</span></span>

### <span data-ttu-id="b9f6a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f6a-119">-DefaultProfile</span></span>
<span data-ttu-id="b9f6a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f6a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b9f6a-121">-Name</span></span>
<span data-ttu-id="b9f6a-122">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-122">The pipeline name.</span></span>

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

### <span data-ttu-id="b9f6a-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9f6a-123">-WorkspaceName</span></span>
<span data-ttu-id="b9f6a-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9f6a-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9f6a-125">-WorkspaceObject</span></span>
<span data-ttu-id="b9f6a-126">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9f6a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f6a-127">CommonParameters</span></span>
<span data-ttu-id="b9f6a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f6a-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f6a-130">입력</span><span class="sxs-lookup"><span data-stu-id="b9f6a-130">INPUTS</span></span>

### <span data-ttu-id="b9f6a-131">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b9f6a-132">출력</span><span class="sxs-lookup"><span data-stu-id="b9f6a-132">OUTPUTS</span></span>

### <span data-ttu-id="b9f6a-133">Synapse. PSPipelineResource/.</span><span class="sxs-lookup"><span data-stu-id="b9f6a-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="b9f6a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b9f6a-134">NOTES</span></span>

## <span data-ttu-id="b9f6a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9f6a-135">RELATED LINKS</span></span>
