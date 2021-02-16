---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182764"
---
# <span data-ttu-id="97db5-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="97db5-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="97db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97db5-102">SYNOPSIS</span></span>
<span data-ttu-id="97db5-103">파이프라인을 호출하여 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="97db5-104">구문</span><span class="sxs-lookup"><span data-stu-id="97db5-104">SYNTAX</span></span>

### <span data-ttu-id="97db5-105">NewByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="97db5-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97db5-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="97db5-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97db5-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="97db5-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97db5-108">설명</span><span class="sxs-lookup"><span data-stu-id="97db5-108">DESCRIPTION</span></span>
<span data-ttu-id="97db5-109">**Invoke-AzSynapsePipeline** 명령은 지정된 파이프라인에서 실행을 시작하고 이 실행에 대한 ID를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="97db5-110">이 GUID는 **Get-AzSynapsePipelineRun** 또는 **Get-AzSynapseActivityRun으로** 전달하여 이 실행에 대한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="97db5-111">예제</span><span class="sxs-lookup"><span data-stu-id="97db5-111">EXAMPLES</span></span>

### <span data-ttu-id="97db5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="97db5-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="97db5-113">이 명령은 작업 영역 ContosoWorkspace에서 ContosoPipeline이라는 파이프라인에 대한 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="97db5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="97db5-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="97db5-115">이 명령은 파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoPipeline이라는 파이프라인에 대한 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="97db5-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="97db5-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="97db5-117">이 명령은 파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoPipeline이라는 파이프라인에 대한 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="97db5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97db5-118">PARAMETERS</span></span>

### <span data-ttu-id="97db5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97db5-119">-AsJob</span></span>
<span data-ttu-id="97db5-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97db5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97db5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97db5-121">-DefaultProfile</span></span>
<span data-ttu-id="97db5-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97db5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97db5-123">-InputObject</span></span>
<span data-ttu-id="97db5-124">파이프라인 실행에 대한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="97db5-125">-IsRecovery</span></span>
<span data-ttu-id="97db5-126">복구 모드 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-126">Recovery mode flag.</span></span>
<span data-ttu-id="97db5-127">복구 모드가 true로 설정된 경우 지정된 참조된 파이프라인 실행 및 새 실행이 동일한 groupId 아래에 그룹화됩니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="97db5-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="97db5-128">-Parameter</span></span>
<span data-ttu-id="97db5-129">파이프라인 실행에 대한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="97db5-130">-ParameterFile</span></span>
<span data-ttu-id="97db5-131">파이프라인 실행에 대한 매개 변수가 있는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="97db5-132">-PipelineName</span></span>
<span data-ttu-id="97db5-133">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="97db5-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="97db5-135">다시 실행에 대한 파이프라인 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="97db5-136">실행 ID를 지정하면 지정된 실행의 매개 변수를 사용하여 새 실행을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="97db5-137">-StartActivityName</span></span>
<span data-ttu-id="97db5-138">복구 모드에서 다시 시작은 이 작업에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="97db5-139">지정하지 않으면 모든 활동이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-139">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97db5-140">-WorkspaceName</span></span>
<span data-ttu-id="97db5-141">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97db5-142">-WorkspaceObject</span></span>
<span data-ttu-id="97db5-143">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97db5-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97db5-144">-Confirm</span></span>
<span data-ttu-id="97db5-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97db5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97db5-146">-WhatIf</span></span>
<span data-ttu-id="97db5-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="97db5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97db5-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97db5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97db5-149">CommonParameters</span></span>
<span data-ttu-id="97db5-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97db5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97db5-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97db5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97db5-152">입력</span><span class="sxs-lookup"><span data-stu-id="97db5-152">INPUTS</span></span>

### <span data-ttu-id="97db5-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="97db5-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="97db5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="97db5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="97db5-155">출력</span><span class="sxs-lookup"><span data-stu-id="97db5-155">OUTPUTS</span></span>

### <span data-ttu-id="97db5-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="97db5-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="97db5-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97db5-157">NOTES</span></span>

## <span data-ttu-id="97db5-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97db5-158">RELATED LINKS</span></span>
