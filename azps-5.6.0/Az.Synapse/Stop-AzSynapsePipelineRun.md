---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: 607b251deff02ae6a74f0ceb5fc4f88a9c899688
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991998"
---
# <span data-ttu-id="83b81-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="83b81-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="83b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b81-102">SYNOPSIS</span></span>
<span data-ttu-id="83b81-103">작업 영역의 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="83b81-104">구문</span><span class="sxs-lookup"><span data-stu-id="83b81-104">SYNTAX</span></span>

### <span data-ttu-id="83b81-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="83b81-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b81-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="83b81-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b81-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="83b81-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b81-108">설명</span><span class="sxs-lookup"><span data-stu-id="83b81-108">DESCRIPTION</span></span>
<span data-ttu-id="83b81-109">**Stop-AzSynapsePipelineRun** cmdlet은 파이프라인 실행 ID로 지정된 작업 영역의 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="83b81-110">예제</span><span class="sxs-lookup"><span data-stu-id="83b81-110">EXAMPLES</span></span>

### <span data-ttu-id="83b81-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="83b81-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="83b81-112">이 명령은 작업 영역 ContosoWorkspace에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용하여 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="83b81-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="83b81-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="83b81-114">이 명령은 작업 영역 ContosoWorkspace에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용하여 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="83b81-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="83b81-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="83b81-116">이 명령은 작업 영역 ContosoWorkspace에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용하여 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="83b81-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83b81-117">PARAMETERS</span></span>

### <span data-ttu-id="83b81-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83b81-118">-AsJob</span></span>
<span data-ttu-id="83b81-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="83b81-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83b81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b81-120">-DefaultProfile</span></span>
<span data-ttu-id="83b81-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b81-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83b81-122">-InputObject</span></span>
<span data-ttu-id="83b81-123">파이프라인 실행에 대한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83b81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83b81-124">-PassThru</span></span>
<span data-ttu-id="83b81-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="83b81-126">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="83b81-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="83b81-127">-PipelineRunId</span></span>
<span data-ttu-id="83b81-128">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b81-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="83b81-129">-WorkspaceName</span></span>
<span data-ttu-id="83b81-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b81-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="83b81-131">-WorkspaceObject</span></span>
<span data-ttu-id="83b81-132">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83b81-133">-확인</span><span class="sxs-lookup"><span data-stu-id="83b81-133">-Confirm</span></span>
<span data-ttu-id="83b81-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b81-135">-WhatIf</span></span>
<span data-ttu-id="83b81-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b81-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b81-138">CommonParameters</span></span>
<span data-ttu-id="83b81-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83b81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b81-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83b81-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b81-141">입력</span><span class="sxs-lookup"><span data-stu-id="83b81-141">INPUTS</span></span>

### <span data-ttu-id="83b81-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83b81-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="83b81-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="83b81-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="83b81-144">출력</span><span class="sxs-lookup"><span data-stu-id="83b81-144">OUTPUTS</span></span>

### <span data-ttu-id="83b81-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83b81-145">System.Boolean</span></span>

## <span data-ttu-id="83b81-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83b81-146">NOTES</span></span>

## <span data-ttu-id="83b81-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83b81-147">RELATED LINKS</span></span>
