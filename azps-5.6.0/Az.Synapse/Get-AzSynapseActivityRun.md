---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: c32b0714a64e0fa97b5376861360bc3645995418
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981856"
---
# <span data-ttu-id="2acfd-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="2acfd-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="2acfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2acfd-102">SYNOPSIS</span></span>
<span data-ttu-id="2acfd-103">파이프라인 실행에 대한 활동 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="2acfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="2acfd-104">SYNTAX</span></span>

### <span data-ttu-id="2acfd-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2acfd-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acfd-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="2acfd-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2acfd-107">설명</span><span class="sxs-lookup"><span data-stu-id="2acfd-107">DESCRIPTION</span></span>
<span data-ttu-id="2acfd-108">**Get-AzSynapseActivityRun** cmdlet은 지정된 기간에 발생한 지정된 파이프라인 실행에 대한 작업 영역의 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="2acfd-109">또한 활동 이름 및 실행 상태에 대한 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="2acfd-110">예제</span><span class="sxs-lookup"><span data-stu-id="2acfd-110">EXAMPLES</span></span>

### <span data-ttu-id="2acfd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2acfd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="2acfd-112">이 명령은 ID "f288712d-fb08-4cb8-96ef-82d3b9b를 사용하여 ContosoPipeline 실행이라는 파이프라인의 모든 활동 실행에 대한 세부 정보를 제공합니다. "2018-09-01T21:00"과 "2018-09-30T21:00" 사이에 발생한 30621입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="2acfd-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2acfd-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="2acfd-114">이 명령은 ID "f288712d-fb08-4cb8-96ef-82d3b9b3을 사용하여 ContosoPipeline 실행이라는 파이프라인에서 실행되는 모든 작업 실행에 대한 세부 정보를 제공합니다. 파이프라인을 통해 "2018-09-01T21:00"과 "2018-09-30T21:00" 사이에 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="2acfd-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2acfd-115">PARAMETERS</span></span>

### <span data-ttu-id="2acfd-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="2acfd-116">-ActivityName</span></span>
<span data-ttu-id="2acfd-117">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-117">The name of the activity.</span></span>

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

### <span data-ttu-id="2acfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acfd-118">-DefaultProfile</span></span>
<span data-ttu-id="2acfd-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acfd-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2acfd-120">-PipelineName</span></span>
<span data-ttu-id="2acfd-121">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acfd-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2acfd-122">-PipelineRunId</span></span>
<span data-ttu-id="2acfd-123">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acfd-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2acfd-124">-RunStartedAfter</span></span>
<span data-ttu-id="2acfd-125">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 그 후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acfd-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2acfd-126">-RunStartedBefore</span></span>
<span data-ttu-id="2acfd-127">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 이전의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acfd-128">-Status</span><span class="sxs-lookup"><span data-stu-id="2acfd-128">-Status</span></span>
<span data-ttu-id="2acfd-129">파이프라인 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="2acfd-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2acfd-130">-WorkspaceName</span></span>
<span data-ttu-id="2acfd-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2acfd-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2acfd-132">-WorkspaceObject</span></span>
<span data-ttu-id="2acfd-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2acfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acfd-134">CommonParameters</span></span>
<span data-ttu-id="2acfd-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2acfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acfd-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2acfd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acfd-137">입력</span><span class="sxs-lookup"><span data-stu-id="2acfd-137">INPUTS</span></span>

### <span data-ttu-id="2acfd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2acfd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2acfd-139">출력</span><span class="sxs-lookup"><span data-stu-id="2acfd-139">OUTPUTS</span></span>

### <span data-ttu-id="2acfd-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="2acfd-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="2acfd-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2acfd-141">NOTES</span></span>

## <span data-ttu-id="2acfd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2acfd-142">RELATED LINKS</span></span>
