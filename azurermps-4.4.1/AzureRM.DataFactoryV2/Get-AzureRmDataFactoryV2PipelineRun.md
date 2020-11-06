---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537324"
---
# <span data-ttu-id="6c467-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="6c467-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="6c467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c467-102">SYNOPSIS</span></span>
<span data-ttu-id="6c467-103">파이프라인 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c467-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c467-104">SYNTAX</span></span>

### <span data-ttu-id="6c467-105">ByFactoryNameByRunId (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c467-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### <span data-ttu-id="6c467-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="6c467-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### <span data-ttu-id="6c467-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="6c467-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### <span data-ttu-id="6c467-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="6c467-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## <span data-ttu-id="6c467-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6c467-109">DESCRIPTION</span></span>
<span data-ttu-id="6c467-110">**Get-AzureRmDataFactoryV2PipelineRun** 명령은 지정 된 파이프라인에 대 한 실행 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="6c467-111">PipelineRunId가 지정 된 경우 해당 ID를 사용 하 여 실행에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="6c467-112">PipelineRunId가 지정 되지 않은 경우에는 LastUpdatedAfter 및 LastUpdatedBefore 값 사이에 발생 한 지정 된 파이프라인의 모든 실행에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="6c467-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6c467-113">EXAMPLES</span></span>

### <span data-ttu-id="6c467-114">예제 1: pipline run에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6c467-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :

```

<span data-ttu-id="6c467-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 인 파이프라인 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>


## <span data-ttu-id="6c467-116">변수</span><span class="sxs-lookup"><span data-stu-id="6c467-116">PARAMETERS</span></span>

### <span data-ttu-id="6c467-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c467-117">-DataFactory</span></span>
<span data-ttu-id="6c467-118">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6c467-119">-DataFactoryName</span></span>
<span data-ttu-id="6c467-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="6c467-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="6c467-122">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 후</span><span class="sxs-lookup"><span data-stu-id="6c467-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="6c467-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="6c467-124">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 이전입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="6c467-125">-PipelineName</span></span>
<span data-ttu-id="6c467-126">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-126">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="6c467-127">-PipelineRunId</span></span>
<span data-ttu-id="6c467-128">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-128">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c467-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c467-129">-ResourceGroupName</span></span>
<span data-ttu-id="6c467-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6c467-131">입력</span><span class="sxs-lookup"><span data-stu-id="6c467-131">INPUTS</span></span>

### <span data-ttu-id="6c467-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6c467-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="6c467-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6c467-133">System.String</span></span>


## <span data-ttu-id="6c467-134">출력</span><span class="sxs-lookup"><span data-stu-id="6c467-134">OUTPUTS</span></span>

### <span data-ttu-id="6c467-135">DataFactoryV2 ' 1 [[Microsoft Azure. PSPipelineRun, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6c467-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6c467-136">DataFactoryV2. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="6c467-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>


## <span data-ttu-id="6c467-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6c467-137">NOTES</span></span>

## <span data-ttu-id="6c467-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c467-138">RELATED LINKS</span></span>
[<span data-ttu-id="6c467-139">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="6c467-139">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="6c467-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="6c467-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

