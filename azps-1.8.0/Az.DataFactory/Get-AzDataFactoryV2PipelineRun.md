---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: eba11e68d23c852426a7d4541359874bd813fc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701150"
---
# <span data-ttu-id="4fb72-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4fb72-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="4fb72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb72-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb72-103">파이프라인 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4fb72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fb72-104">SYNTAX</span></span>

### <span data-ttu-id="4fb72-105">ByFactoryNameByRunId (기본값)</span><span class="sxs-lookup"><span data-stu-id="4fb72-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb72-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="4fb72-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb72-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="4fb72-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fb72-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="4fb72-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb72-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4fb72-109">DESCRIPTION</span></span>
<span data-ttu-id="4fb72-110">**Get-AzDataFactoryV2PipelineRun** 명령은 지정 된 파이프라인에 대 한 실행 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4fb72-111">PipelineRunId가 지정 된 경우 해당 ID를 사용 하 여 실행에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4fb72-112">PipelineRunId가 지정 되지 않은 경우에는 LastUpdatedAfter 및 LastUpdatedBefore 값 사이에 발생 한 지정 된 파이프라인의 모든 실행에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="4fb72-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4fb72-113">EXAMPLES</span></span>

### <span data-ttu-id="4fb72-114">예제 1: pipline run에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4fb72-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="4fb72-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 인 파이프라인 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4fb72-116">변수</span><span class="sxs-lookup"><span data-stu-id="4fb72-116">PARAMETERS</span></span>

### <span data-ttu-id="4fb72-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fb72-117">-DataFactory</span></span>
<span data-ttu-id="4fb72-118">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-118">The data factory object.</span></span>

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

### <span data-ttu-id="4fb72-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4fb72-119">-DataFactoryName</span></span>
<span data-ttu-id="4fb72-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-120">The data factory name.</span></span>

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

### <span data-ttu-id="4fb72-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb72-121">-DefaultProfile</span></span>
<span data-ttu-id="4fb72-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb72-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="4fb72-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="4fb72-124">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 후</span><span class="sxs-lookup"><span data-stu-id="4fb72-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="4fb72-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="4fb72-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="4fb72-126">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 이전입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="4fb72-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4fb72-127">-PipelineName</span></span>
<span data-ttu-id="4fb72-128">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-128">The pipeline name.</span></span>

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

### <span data-ttu-id="4fb72-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4fb72-129">-PipelineRunId</span></span>
<span data-ttu-id="4fb72-130">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="4fb72-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb72-131">-ResourceGroupName</span></span>
<span data-ttu-id="4fb72-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-132">The resource group name.</span></span>

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

### <span data-ttu-id="4fb72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb72-133">CommonParameters</span></span>
<span data-ttu-id="4fb72-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb72-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb72-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb72-136">입력</span><span class="sxs-lookup"><span data-stu-id="4fb72-136">INPUTS</span></span>

### <span data-ttu-id="4fb72-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4fb72-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="4fb72-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fb72-138">System.String</span></span>

## <span data-ttu-id="4fb72-139">출력</span><span class="sxs-lookup"><span data-stu-id="4fb72-139">OUTPUTS</span></span>

### <span data-ttu-id="4fb72-140">DataFactoryV2. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="4fb72-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4fb72-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4fb72-141">NOTES</span></span>

## <span data-ttu-id="4fb72-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fb72-142">RELATED LINKS</span></span>

[<span data-ttu-id="4fb72-143">AzDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="4fb72-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4fb72-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4fb72-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

