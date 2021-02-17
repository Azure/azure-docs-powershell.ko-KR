---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198865"
---
# <span data-ttu-id="e0cf7-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e0cf7-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="e0cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cf7-103">파이프라인 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="e0cf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0cf7-104">SYNTAX</span></span>

### <span data-ttu-id="e0cf7-105">ByFactoryNameByRunId(기본값)</span><span class="sxs-lookup"><span data-stu-id="e0cf7-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf7-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="e0cf7-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf7-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="e0cf7-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0cf7-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="e0cf7-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0cf7-109">설명</span><span class="sxs-lookup"><span data-stu-id="e0cf7-109">DESCRIPTION</span></span>
<span data-ttu-id="e0cf7-110">**Get-AzDataFactoryV2PipelineRun** 명령은 지정된 파이프라인에 대한 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="e0cf7-111">PipelineRunId를 지정하면 해당 ID를 통해 실행에 대한 세부 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="e0cf7-112">PipelineRunId를 지정하지 않으면 LastUpdatedAfter와 LastUpdatedBefore 값 간에 발생된 파이프라인에 대한 모든 실행에 대한 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="e0cf7-113">예제</span><span class="sxs-lookup"><span data-stu-id="e0cf7-113">EXAMPLES</span></span>

### <span data-ttu-id="e0cf7-114">예제 1: 파이프라인 실행에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="e0cf7-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="e0cf7-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72"를 사용하여 파이프라인 실행에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="e0cf7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0cf7-116">PARAMETERS</span></span>

### <span data-ttu-id="e0cf7-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e0cf7-117">-DataFactory</span></span>
<span data-ttu-id="e0cf7-118">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e0cf7-119">-DataFactoryName</span></span>
<span data-ttu-id="e0cf7-120">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cf7-121">-DefaultProfile</span></span>
<span data-ttu-id="e0cf7-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0cf7-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="e0cf7-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="e0cf7-124">파이프라인 실행이 ISO8601 형식으로 업데이트된 시간 또는 그 이후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="e0cf7-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="e0cf7-126">파이프라인 실행이 ISO8601 형식으로 업데이트된 시간 또는 이전 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e0cf7-127">-PipelineName</span></span>
<span data-ttu-id="e0cf7-128">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e0cf7-129">-PipelineRunId</span></span>
<span data-ttu-id="e0cf7-130">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0cf7-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0cf7-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cf7-133">CommonParameters</span></span>
<span data-ttu-id="e0cf7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cf7-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e0cf7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cf7-136">입력</span><span class="sxs-lookup"><span data-stu-id="e0cf7-136">INPUTS</span></span>

### <span data-ttu-id="e0cf7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e0cf7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e0cf7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e0cf7-138">System.String</span></span>

## <span data-ttu-id="e0cf7-139">출력</span><span class="sxs-lookup"><span data-stu-id="e0cf7-139">OUTPUTS</span></span>

### <span data-ttu-id="e0cf7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e0cf7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="e0cf7-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0cf7-141">NOTES</span></span>

## <span data-ttu-id="e0cf7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0cf7-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0cf7-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e0cf7-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e0cf7-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e0cf7-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

