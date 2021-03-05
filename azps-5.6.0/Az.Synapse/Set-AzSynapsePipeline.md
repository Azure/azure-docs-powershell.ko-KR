---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: cd79d9315c6352b604a40269286073792596a41e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992138"
---
# <span data-ttu-id="35ea4-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="35ea4-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="35ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="35ea4-103">작업 영역의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="35ea4-104">구문</span><span class="sxs-lookup"><span data-stu-id="35ea4-104">SYNTAX</span></span>

### <span data-ttu-id="35ea4-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="35ea4-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ea4-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="35ea4-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ea4-107">설명</span><span class="sxs-lookup"><span data-stu-id="35ea4-107">DESCRIPTION</span></span>
<span data-ttu-id="35ea4-108">**Set-AzSynapsePipeline cmdlet은** 작업 영역의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="35ea4-109">예제</span><span class="sxs-lookup"><span data-stu-id="35ea4-109">EXAMPLES</span></span>

### <span data-ttu-id="35ea4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="35ea4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="35ea4-111">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoPipeline이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="35ea4-112">명령은 파일에서 파이프라인을 pipeline.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="35ea4-113">이 파일에는 활동에 대한 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-113">This file includes information about activities.</span></span>

### <span data-ttu-id="35ea4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="35ea4-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="35ea4-115">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 ContosoPipeline이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="35ea4-116">명령은 파일에서 파이프라인을 pipeline.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="35ea4-117">이 파일에는 활동에 대한 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-117">This file includes information about activities.</span></span>

## <span data-ttu-id="35ea4-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="35ea4-118">PARAMETERS</span></span>

### <span data-ttu-id="35ea4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35ea4-119">-AsJob</span></span>
<span data-ttu-id="35ea4-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="35ea4-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ea4-121">-DefaultProfile</span></span>
<span data-ttu-id="35ea4-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ea4-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="35ea4-123">-DefinitionFile</span></span>
<span data-ttu-id="35ea4-124">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="35ea4-125">-Name</span></span>
<span data-ttu-id="35ea4-126">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35ea4-127">-WorkspaceName</span></span>
<span data-ttu-id="35ea4-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35ea4-129">-WorkspaceObject</span></span>
<span data-ttu-id="35ea4-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-131">-확인</span><span class="sxs-lookup"><span data-stu-id="35ea4-131">-Confirm</span></span>
<span data-ttu-id="35ea4-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ea4-133">-WhatIf</span></span>
<span data-ttu-id="35ea4-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ea4-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ea4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ea4-136">CommonParameters</span></span>
<span data-ttu-id="35ea4-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35ea4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ea4-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35ea4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ea4-139">입력</span><span class="sxs-lookup"><span data-stu-id="35ea4-139">INPUTS</span></span>

### <span data-ttu-id="35ea4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35ea4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="35ea4-141">출력</span><span class="sxs-lookup"><span data-stu-id="35ea4-141">OUTPUTS</span></span>

### <span data-ttu-id="35ea4-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="35ea4-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="35ea4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35ea4-143">NOTES</span></span>

## <span data-ttu-id="35ea4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35ea4-144">RELATED LINKS</span></span>
