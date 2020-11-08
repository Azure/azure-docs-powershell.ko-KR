---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212487"
---
# <span data-ttu-id="9a72c-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="9a72c-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="9a72c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a72c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a72c-103">작업 영역에서 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="9a72c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a72c-104">SYNTAX</span></span>

### <span data-ttu-id="9a72c-105">RemoveByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a72c-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a72c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9a72c-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a72c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a72c-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a72c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a72c-108">DESCRIPTION</span></span>
<span data-ttu-id="9a72c-109">**AzSynapsePipelineRun** cmdlet은 파이프라인 실행 ID를 사용 하 여 지정 된 작업 영역에서 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="9a72c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a72c-110">EXAMPLES</span></span>

### <span data-ttu-id="9a72c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a72c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="9a72c-112">이 명령은 workspace ContosoWorkspace에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용 하 여 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9a72c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9a72c-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="9a72c-114">이 명령은 workspace ContosoWorkspace to 파이프라인에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용 하 여 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9a72c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="9a72c-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="9a72c-116">이 명령은 workspace ContosoWorkspace to 파이프라인에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용 하 여 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9a72c-117">변수</span><span class="sxs-lookup"><span data-stu-id="9a72c-117">PARAMETERS</span></span>

### <span data-ttu-id="9a72c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a72c-118">-AsJob</span></span>
<span data-ttu-id="9a72c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a72c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a72c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a72c-120">-DefaultProfile</span></span>
<span data-ttu-id="9a72c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a72c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a72c-122">-InputObject</span></span>
<span data-ttu-id="9a72c-123">파이프라인 실행에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="9a72c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a72c-124">-PassThru</span></span>
<span data-ttu-id="9a72c-125">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9a72c-126">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9a72c-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="9a72c-127">-PipelineRunId</span></span>
<span data-ttu-id="9a72c-128">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="9a72c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a72c-129">-WorkspaceName</span></span>
<span data-ttu-id="9a72c-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a72c-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9a72c-131">-WorkspaceObject</span></span>
<span data-ttu-id="9a72c-132">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a72c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="9a72c-133">-Confirm</span></span>
<span data-ttu-id="9a72c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a72c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a72c-135">-WhatIf</span></span>
<span data-ttu-id="9a72c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a72c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a72c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a72c-138">CommonParameters</span></span>
<span data-ttu-id="9a72c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a72c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a72c-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a72c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a72c-141">입력</span><span class="sxs-lookup"><span data-stu-id="9a72c-141">INPUTS</span></span>

### <span data-ttu-id="9a72c-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="9a72c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9a72c-143">Synapse. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="9a72c-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="9a72c-144">출력</span><span class="sxs-lookup"><span data-stu-id="9a72c-144">OUTPUTS</span></span>

### <span data-ttu-id="9a72c-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9a72c-145">System.Boolean</span></span>

## <span data-ttu-id="9a72c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="9a72c-146">NOTES</span></span>

## <span data-ttu-id="9a72c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a72c-147">RELATED LINKS</span></span>
