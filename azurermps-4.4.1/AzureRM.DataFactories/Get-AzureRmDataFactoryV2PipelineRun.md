---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 0ecc2025a5c1b1a3ad1c27a8c2a926c6ef0402b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527688"
---
# <span data-ttu-id="2d2fc-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2d2fc-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="2d2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2fc-103">파이프라인 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d2fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d2fc-104">SYNTAX</span></span>

### <span data-ttu-id="2d2fc-105">ByFactoryNameByRunId (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2fc-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="2d2fc-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2fc-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="2d2fc-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2fc-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="2d2fc-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d2fc-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2d2fc-109">DESCRIPTION</span></span>
<span data-ttu-id="2d2fc-110">**Get-AzureRmDataFactoryV2PipelineRun** 명령은 지정 된 파이프라인에 대 한 실행 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="2d2fc-111">PipelineRunId가 지정 된 경우 해당 ID를 사용 하 여 실행에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="2d2fc-112">PipelineRunId가 지정 되지 않은 경우에는 LastUpdatedAfter 및 LastUpdatedBefore 값 사이에 발생 한 지정 된 파이프라인의 모든 실행에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="2d2fc-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2d2fc-113">EXAMPLES</span></span>

### <span data-ttu-id="2d2fc-114">예제 1: pipline run에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d2fc-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="2d2fc-115">이 명령은 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 인 파이프라인 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="2d2fc-116">변수</span><span class="sxs-lookup"><span data-stu-id="2d2fc-116">PARAMETERS</span></span>

### <span data-ttu-id="2d2fc-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d2fc-117">-DataFactory</span></span>
<span data-ttu-id="2d2fc-118">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-118">The data factory object.</span></span>

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

### <span data-ttu-id="2d2fc-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2d2fc-119">-DataFactoryName</span></span>
<span data-ttu-id="2d2fc-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-120">The data factory name.</span></span>

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

### <span data-ttu-id="2d2fc-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="2d2fc-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="2d2fc-122">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 후</span><span class="sxs-lookup"><span data-stu-id="2d2fc-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="2d2fc-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="2d2fc-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="2d2fc-124">ISO8601 format에서 파이프라인 실행이 업데이트 된 시간 또는 그 이전입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="2d2fc-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2d2fc-125">-PipelineName</span></span>
<span data-ttu-id="2d2fc-126">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-126">The pipeline name.</span></span>

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

### <span data-ttu-id="2d2fc-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2d2fc-127">-PipelineRunId</span></span>
<span data-ttu-id="2d2fc-128">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-128">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="2d2fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d2fc-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-130">The resource group name.</span></span>

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

### <span data-ttu-id="2d2fc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2fc-131">-DefaultProfile</span></span>
<span data-ttu-id="2d2fc-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2fc-133">CommonParameters</span></span>
<span data-ttu-id="2d2fc-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2fc-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2fc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2fc-136">입력</span><span class="sxs-lookup"><span data-stu-id="2d2fc-136">INPUTS</span></span>

### <span data-ttu-id="2d2fc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2d2fc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="2d2fc-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d2fc-138">System.String</span></span>

## <span data-ttu-id="2d2fc-139">출력</span><span class="sxs-lookup"><span data-stu-id="2d2fc-139">OUTPUTS</span></span>

### <span data-ttu-id="2d2fc-140">DataFactoryV2 ' 1 [[Microsoft Azure. PSPipelineRun, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2d2fc-141">DataFactoryV2. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="2d2fc-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2d2fc-142">NOTES</span></span>

## <span data-ttu-id="2d2fc-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d2fc-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d2fc-144">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="2d2fc-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="2d2fc-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="2d2fc-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

