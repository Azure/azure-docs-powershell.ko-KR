---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047476"
---
# <span data-ttu-id="cd12e-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="cd12e-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="cd12e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd12e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd12e-103">파이프라인을 호출 하 여 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="cd12e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd12e-104">SYNTAX</span></span>

### <span data-ttu-id="cd12e-105">NewByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd12e-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd12e-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd12e-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd12e-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="cd12e-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd12e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cd12e-108">DESCRIPTION</span></span>
<span data-ttu-id="cd12e-109">**AzSynapsePipeline** 명령은 지정 된 파이프라인에서 실행을 시작 하 고 해당 실행에 대 한 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="cd12e-110">이 GUID는 **AzSynapsePipelineRun** 또는 **get-AzSynapseActivityRun** 에 전달 되어이 실행에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="cd12e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cd12e-111">EXAMPLES</span></span>

### <span data-ttu-id="cd12e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd12e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="cd12e-113">이 명령은 workspace ContosoWorkspace에서 ContosoPipeline 이라는 파이프라인에 대해 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cd12e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="cd12e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="cd12e-115">이 명령은 workspace ContosoWorkspace to 파이프라인에서 ContosoPipeline 이라는 파이프라인에 대해 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cd12e-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="cd12e-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="cd12e-117">이 명령은 workspace ContosoWorkspace to 파이프라인에서 ContosoPipeline 이라는 파이프라인에 대해 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cd12e-118">변수</span><span class="sxs-lookup"><span data-stu-id="cd12e-118">PARAMETERS</span></span>

### <span data-ttu-id="cd12e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd12e-119">-AsJob</span></span>
<span data-ttu-id="cd12e-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd12e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd12e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd12e-121">-DefaultProfile</span></span>
<span data-ttu-id="cd12e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd12e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd12e-123">-InputObject</span></span>
<span data-ttu-id="cd12e-124">파이프라인 실행에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="cd12e-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="cd12e-125">-IsRecovery</span></span>
<span data-ttu-id="cd12e-126">복구 모드 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-126">Recovery mode flag.</span></span>
<span data-ttu-id="cd12e-127">복구 모드를 true로 설정 하면 지정 된 참조 파이프라인이 실행 되 고 새 실행이 동일한 groupId 아래 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="cd12e-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cd12e-128">-Parameter</span></span>
<span data-ttu-id="cd12e-129">파이프라인 실행을 위한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="cd12e-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="cd12e-130">-ParameterFile</span></span>
<span data-ttu-id="cd12e-131">파이프라인 실행을 위한 매개 변수를 사용 하는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="cd12e-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="cd12e-132">-PipelineName</span></span>
<span data-ttu-id="cd12e-133">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-133">The pipeline name.</span></span>

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

### <span data-ttu-id="cd12e-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="cd12e-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="cd12e-135">다시 실행에 대 한 파이프라인 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="cd12e-136">실행 ID를 지정 하면 지정 된 실행의 매개 변수를 사용 하 여 새 실행이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="cd12e-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="cd12e-137">-StartActivityName</span></span>
<span data-ttu-id="cd12e-138">복구 모드에서는이 작업에서 다시 실행이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="cd12e-139">지정 하지 않으면 모든 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="cd12e-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd12e-140">-WorkspaceName</span></span>
<span data-ttu-id="cd12e-141">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cd12e-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cd12e-142">-WorkspaceObject</span></span>
<span data-ttu-id="cd12e-143">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cd12e-144">-확인</span><span class="sxs-lookup"><span data-stu-id="cd12e-144">-Confirm</span></span>
<span data-ttu-id="cd12e-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd12e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd12e-146">-WhatIf</span></span>
<span data-ttu-id="cd12e-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd12e-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd12e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd12e-149">CommonParameters</span></span>
<span data-ttu-id="cd12e-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd12e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd12e-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd12e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd12e-152">입력</span><span class="sxs-lookup"><span data-stu-id="cd12e-152">INPUTS</span></span>

### <span data-ttu-id="cd12e-153">Synapse. PSPipelineResource/.</span><span class="sxs-lookup"><span data-stu-id="cd12e-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="cd12e-154">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="cd12e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cd12e-155">출력</span><span class="sxs-lookup"><span data-stu-id="cd12e-155">OUTPUTS</span></span>

### <span data-ttu-id="cd12e-156">Synapse. PSCreateRunResponse/.</span><span class="sxs-lookup"><span data-stu-id="cd12e-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="cd12e-157">상속자</span><span class="sxs-lookup"><span data-stu-id="cd12e-157">NOTES</span></span>

## <span data-ttu-id="cd12e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd12e-158">RELATED LINKS</span></span>
