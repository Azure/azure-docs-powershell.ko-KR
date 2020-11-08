---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204685"
---
# <span data-ttu-id="a463e-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="a463e-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="a463e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a463e-102">SYNOPSIS</span></span>
<span data-ttu-id="a463e-103">파이프라인 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="a463e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a463e-104">SYNTAX</span></span>

### <span data-ttu-id="a463e-105">GetByNameAndId (기본값)</span><span class="sxs-lookup"><span data-stu-id="a463e-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a463e-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="a463e-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a463e-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="a463e-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a463e-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="a463e-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a463e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a463e-109">DESCRIPTION</span></span>
<span data-ttu-id="a463e-110">**Get-AzSynapsePipelineRun** 명령은 지정 된 파이프라인에 대 한 실행 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="a463e-111">PipelineRunId가 지정 된 경우 해당 ID를 사용 하 여 실행에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="a463e-112">PipelineRunId가 지정 되지 않은 경우에는 RunStartedAfter 및 RunStartedBefore 값 사이에 발생 한 모든 파이프라인의 모든 실행에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="a463e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a463e-113">EXAMPLES</span></span>

### <span data-ttu-id="a463e-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="a463e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="a463e-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 인 파이프라인 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="a463e-116">변수</span><span class="sxs-lookup"><span data-stu-id="a463e-116">PARAMETERS</span></span>

### <span data-ttu-id="a463e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a463e-117">-DefaultProfile</span></span>
<span data-ttu-id="a463e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a463e-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a463e-119">-PipelineName</span></span>
<span data-ttu-id="a463e-120">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-120">The pipeline name.</span></span>

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

### <span data-ttu-id="a463e-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a463e-121">-PipelineRunId</span></span>
<span data-ttu-id="a463e-122">파이프라인 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="a463e-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a463e-123">-RunStartedAfter</span></span>
<span data-ttu-id="a463e-124">' ISO 8601 ' 형식으로 실행 이벤트가 업데이트 된 시간 또는 이후</span><span class="sxs-lookup"><span data-stu-id="a463e-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="a463e-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a463e-125">-RunStartedBefore</span></span>
<span data-ttu-id="a463e-126">' ISO 8601 ' 형식으로 실행 이벤트를 업데이트 한 날짜 또는 그 이전의 시간</span><span class="sxs-lookup"><span data-stu-id="a463e-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="a463e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a463e-127">-WorkspaceName</span></span>
<span data-ttu-id="a463e-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a463e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a463e-129">-WorkspaceObject</span></span>
<span data-ttu-id="a463e-130">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a463e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a463e-131">CommonParameters</span></span>
<span data-ttu-id="a463e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a463e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a463e-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a463e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a463e-134">입력</span><span class="sxs-lookup"><span data-stu-id="a463e-134">INPUTS</span></span>

### <span data-ttu-id="a463e-135">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="a463e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a463e-136">출력</span><span class="sxs-lookup"><span data-stu-id="a463e-136">OUTPUTS</span></span>

### <span data-ttu-id="a463e-137">Synapse. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="a463e-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="a463e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a463e-138">NOTES</span></span>

## <span data-ttu-id="a463e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a463e-139">RELATED LINKS</span></span>
