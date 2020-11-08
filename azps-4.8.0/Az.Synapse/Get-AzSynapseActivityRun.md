---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204695"
---
# <span data-ttu-id="28def-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="28def-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="28def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28def-102">SYNOPSIS</span></span>
<span data-ttu-id="28def-103">파이프라인 실행에 대 한 작업 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28def-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="28def-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28def-104">SYNTAX</span></span>

### <span data-ttu-id="28def-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="28def-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28def-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="28def-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28def-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28def-107">DESCRIPTION</span></span>
<span data-ttu-id="28def-108">**AzSynapseActivityRun** cmdlet은 지정 된 시간에 발생 한 특정 파이프라인 실행에 대 한 작업 영역의 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28def-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="28def-109">또한 활동 이름 및 실행 상태에 대 한 필터를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28def-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="28def-110">예제의</span><span class="sxs-lookup"><span data-stu-id="28def-110">EXAMPLES</span></span>

### <span data-ttu-id="28def-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="28def-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="28def-112">이 명령은 "2018-09-01T21:00"과 "2018-09-30T21:00" 사이에 발생 한 ID가 "f288712d-fb08-4cb8-96ef-82d3b9b30621" 인 ContosoPipeline run 이라는 파이프라인의 모든 작업 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28def-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="28def-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="28def-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="28def-114">이 명령은 "2018-09-01T21:00" 및 "2018-09-30T21:00"에서 파이프라인 까지의 ID가 "f288712d-fb08-4cb8-96ef-82d3b9b30621" 인 ContosoPipeline run 이라는 파이프라인의 모든 작업 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28def-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="28def-115">변수</span><span class="sxs-lookup"><span data-stu-id="28def-115">PARAMETERS</span></span>

### <span data-ttu-id="28def-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="28def-116">-ActivityName</span></span>
<span data-ttu-id="28def-117">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-117">The name of the activity.</span></span>

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

### <span data-ttu-id="28def-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28def-118">-DefaultProfile</span></span>
<span data-ttu-id="28def-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28def-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="28def-120">-PipelineName</span></span>
<span data-ttu-id="28def-121">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-121">The pipeline name.</span></span>

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

### <span data-ttu-id="28def-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="28def-122">-PipelineRunId</span></span>
<span data-ttu-id="28def-123">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="28def-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="28def-124">-RunStartedAfter</span></span>
<span data-ttu-id="28def-125">' ISO 8601 ' 형식으로 실행 이벤트가 업데이트 된 시간 또는 이후</span><span class="sxs-lookup"><span data-stu-id="28def-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="28def-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="28def-126">-RunStartedBefore</span></span>
<span data-ttu-id="28def-127">' ISO 8601 ' 형식으로 실행 이벤트를 업데이트 한 날짜 또는 그 이전의 시간</span><span class="sxs-lookup"><span data-stu-id="28def-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="28def-128">-상태</span><span class="sxs-lookup"><span data-stu-id="28def-128">-Status</span></span>
<span data-ttu-id="28def-129">파이프라인의 상태가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28def-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="28def-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28def-130">-WorkspaceName</span></span>
<span data-ttu-id="28def-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="28def-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="28def-132">-WorkspaceObject</span></span>
<span data-ttu-id="28def-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="28def-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="28def-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28def-134">CommonParameters</span></span>
<span data-ttu-id="28def-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28def-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28def-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28def-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28def-137">입력</span><span class="sxs-lookup"><span data-stu-id="28def-137">INPUTS</span></span>

### <span data-ttu-id="28def-138">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="28def-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="28def-139">출력</span><span class="sxs-lookup"><span data-stu-id="28def-139">OUTPUTS</span></span>

### <span data-ttu-id="28def-140">Synapse. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="28def-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="28def-141">상속자</span><span class="sxs-lookup"><span data-stu-id="28def-141">NOTES</span></span>

## <span data-ttu-id="28def-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28def-142">RELATED LINKS</span></span>
