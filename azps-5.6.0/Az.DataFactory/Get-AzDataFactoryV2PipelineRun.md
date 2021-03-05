---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 68c524f2c8712b0da0600abda2fa8035dd5a979c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975136"
---
# <span data-ttu-id="d6c0b-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d6c0b-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="d6c0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c0b-103">파이프라인 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="d6c0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6c0b-104">SYNTAX</span></span>

### <span data-ttu-id="d6c0b-105">ByFactoryNameByRunId(기본값)</span><span class="sxs-lookup"><span data-stu-id="d6c0b-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6c0b-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="d6c0b-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6c0b-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="d6c0b-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6c0b-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="d6c0b-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6c0b-109">설명</span><span class="sxs-lookup"><span data-stu-id="d6c0b-109">DESCRIPTION</span></span>
<span data-ttu-id="d6c0b-110">**Get-AzDataFactoryV2PipelineRun** 명령은 지정된 파이프라인에 대한 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="d6c0b-111">PipelineRunId가 지정되어 있는 경우 해당 ID를 통해 실행에 대한 세부 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="d6c0b-112">PipelineRunId를 지정하지 않은 경우 LastUpdatedAfter 및 LastUpdatedBefore 값 사이에 발생한 파이프라인에 대한 모든 실행에 대한 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="d6c0b-113">예제</span><span class="sxs-lookup"><span data-stu-id="d6c0b-113">EXAMPLES</span></span>

### <span data-ttu-id="d6c0b-114">예제 1: 파이프라인 실행에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="d6c0b-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="d6c0b-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72"를 사용하여 파이프라인 실행에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="d6c0b-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6c0b-116">PARAMETERS</span></span>

### <span data-ttu-id="d6c0b-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6c0b-117">-DataFactory</span></span>
<span data-ttu-id="d6c0b-118">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-118">The data factory object.</span></span>

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

### <span data-ttu-id="d6c0b-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d6c0b-119">-DataFactoryName</span></span>
<span data-ttu-id="d6c0b-120">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-120">The data factory name.</span></span>

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

### <span data-ttu-id="d6c0b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c0b-121">-DefaultProfile</span></span>
<span data-ttu-id="d6c0b-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6c0b-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="d6c0b-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="d6c0b-124">파이프라인 실행이 ISO8601 형식으로 업데이트된 시간 또는 그 후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="d6c0b-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="d6c0b-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="d6c0b-126">파이프라인 실행이 ISO8601 형식으로 업데이트된 시간 또는 이전의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="d6c0b-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d6c0b-127">-PipelineName</span></span>
<span data-ttu-id="d6c0b-128">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-128">The pipeline name.</span></span>

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

### <span data-ttu-id="d6c0b-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d6c0b-129">-PipelineRunId</span></span>
<span data-ttu-id="d6c0b-130">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="d6c0b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c0b-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6c0b-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-132">The resource group name.</span></span>

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

### <span data-ttu-id="d6c0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c0b-133">CommonParameters</span></span>
<span data-ttu-id="d6c0b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c0b-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d6c0b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c0b-136">입력</span><span class="sxs-lookup"><span data-stu-id="d6c0b-136">INPUTS</span></span>

### <span data-ttu-id="d6c0b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d6c0b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d6c0b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d6c0b-138">System.String</span></span>

## <span data-ttu-id="d6c0b-139">출력</span><span class="sxs-lookup"><span data-stu-id="d6c0b-139">OUTPUTS</span></span>

### <span data-ttu-id="d6c0b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="d6c0b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="d6c0b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6c0b-141">NOTES</span></span>

## <span data-ttu-id="d6c0b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6c0b-142">RELATED LINKS</span></span>

[<span data-ttu-id="d6c0b-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d6c0b-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d6c0b-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d6c0b-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

