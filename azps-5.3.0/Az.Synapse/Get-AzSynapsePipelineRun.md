---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491091"
---
# <span data-ttu-id="f3cc6-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="f3cc6-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="f3cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cc6-103">파이프라인 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="f3cc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3cc6-104">SYNTAX</span></span>

### <span data-ttu-id="f3cc6-105">GetByNameAndId(기본값)</span><span class="sxs-lookup"><span data-stu-id="f3cc6-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3cc6-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="f3cc6-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cc6-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="f3cc6-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3cc6-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="f3cc6-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3cc6-109">설명</span><span class="sxs-lookup"><span data-stu-id="f3cc6-109">DESCRIPTION</span></span>
<span data-ttu-id="f3cc6-110">**Get-AzSynapsePipelineRun** 명령은 지정된 파이프라인에 대한 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="f3cc6-111">PipelineRunId를 지정하면 해당 ID를 통해 실행에 대한 세부 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="f3cc6-112">PipelineRunId를 지정하지 않으면 RunStartedAfter와 RunStartedBefore 값 간에 발생된 파이프라인에 대한 모든 실행에 대한 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="f3cc6-113">예제</span><span class="sxs-lookup"><span data-stu-id="f3cc6-113">EXAMPLES</span></span>

### <span data-ttu-id="f3cc6-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3cc6-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="f3cc6-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72"를 사용하여 파이프라인 실행에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="f3cc6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3cc6-116">PARAMETERS</span></span>

### <span data-ttu-id="f3cc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3cc6-117">-DefaultProfile</span></span>
<span data-ttu-id="f3cc6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3cc6-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f3cc6-119">-PipelineName</span></span>
<span data-ttu-id="f3cc6-120">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f3cc6-121">-PipelineRunId</span></span>
<span data-ttu-id="f3cc6-122">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="f3cc6-123">-RunStartedAfter</span></span>
<span data-ttu-id="f3cc6-124">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 그 이후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="f3cc6-125">-RunStartedBefore</span></span>
<span data-ttu-id="f3cc6-126">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 이전 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3cc6-127">-WorkspaceName</span></span>
<span data-ttu-id="f3cc6-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3cc6-129">-WorkspaceObject</span></span>
<span data-ttu-id="f3cc6-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cc6-131">CommonParameters</span></span>
<span data-ttu-id="f3cc6-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cc6-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3cc6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cc6-134">입력</span><span class="sxs-lookup"><span data-stu-id="f3cc6-134">INPUTS</span></span>

### <span data-ttu-id="f3cc6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3cc6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f3cc6-136">출력</span><span class="sxs-lookup"><span data-stu-id="f3cc6-136">OUTPUTS</span></span>

### <span data-ttu-id="f3cc6-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="f3cc6-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="f3cc6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3cc6-138">NOTES</span></span>

## <span data-ttu-id="f3cc6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3cc6-139">RELATED LINKS</span></span>
