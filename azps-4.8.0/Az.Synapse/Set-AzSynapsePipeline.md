---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212488"
---
# <span data-ttu-id="acc6d-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="acc6d-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="acc6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="acc6d-103">작업 영역에 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="acc6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acc6d-104">SYNTAX</span></span>

### <span data-ttu-id="acc6d-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="acc6d-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc6d-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="acc6d-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc6d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="acc6d-107">DESCRIPTION</span></span>
<span data-ttu-id="acc6d-108">**Set-AzSynapsePipeline** cmdlet은 작업 영역에 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="acc6d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="acc6d-109">EXAMPLES</span></span>

### <span data-ttu-id="acc6d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="acc6d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="acc6d-111">이 명령은 ContosoWorkspace 이라는 작업 영역에 ContosoPipeline 이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="acc6d-112">명령은 파일의 pipeline.js정보에 파이프라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="acc6d-113">이 파일에는 활동에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-113">This file includes information about activities.</span></span>

### <span data-ttu-id="acc6d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="acc6d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="acc6d-115">이 명령은 ContosoWorkspace ~ 파이프라인 이라는 작업 영역에 ContosoPipeline 이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="acc6d-116">명령은 파일의 pipeline.js정보에 파이프라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="acc6d-117">이 파일에는 활동에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-117">This file includes information about activities.</span></span>

## <span data-ttu-id="acc6d-118">변수</span><span class="sxs-lookup"><span data-stu-id="acc6d-118">PARAMETERS</span></span>

### <span data-ttu-id="acc6d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acc6d-119">-AsJob</span></span>
<span data-ttu-id="acc6d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="acc6d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acc6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc6d-121">-DefaultProfile</span></span>
<span data-ttu-id="acc6d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc6d-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="acc6d-123">-DefinitionFile</span></span>
<span data-ttu-id="acc6d-124">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-124">The JSON file path.</span></span>

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

### <span data-ttu-id="acc6d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="acc6d-125">-Name</span></span>
<span data-ttu-id="acc6d-126">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-126">The pipeline name.</span></span>

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

### <span data-ttu-id="acc6d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acc6d-127">-WorkspaceName</span></span>
<span data-ttu-id="acc6d-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="acc6d-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acc6d-129">-WorkspaceObject</span></span>
<span data-ttu-id="acc6d-130">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="acc6d-131">-확인</span><span class="sxs-lookup"><span data-stu-id="acc6d-131">-Confirm</span></span>
<span data-ttu-id="acc6d-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc6d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc6d-133">-WhatIf</span></span>
<span data-ttu-id="acc6d-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc6d-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc6d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc6d-136">CommonParameters</span></span>
<span data-ttu-id="acc6d-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc6d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc6d-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="acc6d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc6d-139">입력</span><span class="sxs-lookup"><span data-stu-id="acc6d-139">INPUTS</span></span>

### <span data-ttu-id="acc6d-140">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="acc6d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="acc6d-141">출력</span><span class="sxs-lookup"><span data-stu-id="acc6d-141">OUTPUTS</span></span>

### <span data-ttu-id="acc6d-142">Synapse. PSPipelineResource/.</span><span class="sxs-lookup"><span data-stu-id="acc6d-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="acc6d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="acc6d-143">NOTES</span></span>

## <span data-ttu-id="acc6d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acc6d-144">RELATED LINKS</span></span>
