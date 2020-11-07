---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2000e489dcb5a0bab384ac0aad8a1ffbe53aba15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711590"
---
# <span data-ttu-id="a9eea-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a9eea-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="a9eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eea-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eea-103">파이프라인 실행에 대 한 작업 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9eea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9eea-104">SYNTAX</span></span>

### <span data-ttu-id="a9eea-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9eea-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="a9eea-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9eea-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-DataFactory] <PSDataFactory>
```


## <span data-ttu-id="a9eea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a9eea-107">DESCRIPTION</span></span>

<span data-ttu-id="a9eea-108">**AzureRmDataFactoryV2ActivityRun** cmdlet은 지정 된 기간에 발생 한 지정한 파이프라인 실행에 대 한 Azure Data Factory의 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="a9eea-109">또한 활동 이름, 실행을 실행 한 연결 된 서비스 이름 및 실행 상태에 대 한 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="a9eea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a9eea-110">EXAMPLES</span></span>

### <span data-ttu-id="a9eea-111">예제 1: 파이프라인 실행에 대 한 모든 작업 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9eea-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}

```

<span data-ttu-id="a9eea-112">이 명령은 "2017-09-01" 및 "2017-09-30" 사이에서 발생 하는 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621"로 실행 되는 파이프라인의 모든 작업 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="a9eea-113">변수</span><span class="sxs-lookup"><span data-stu-id="a9eea-113">PARAMETERS</span></span>

### <span data-ttu-id="a9eea-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="a9eea-114">-ActivityName</span></span>
<span data-ttu-id="a9eea-115">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a9eea-116">-DataFactory</span></span>
<span data-ttu-id="a9eea-117">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9eea-118">-DataFactoryName</span></span>
<span data-ttu-id="a9eea-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-120">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="a9eea-120">-LinkedServiceName</span></span>
<span data-ttu-id="a9eea-121">연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-121">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a9eea-122">-PipelineRunId</span></span>
<span data-ttu-id="a9eea-123">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-123">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9eea-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9eea-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a9eea-126">-RunStartedAfter</span></span>
<span data-ttu-id="a9eea-127">파이프라인 실행이 시작 될 때 또는 그 뒤의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a9eea-128">-RunStartedBefore</span></span>
<span data-ttu-id="a9eea-129">파이프라인 실행이 시작 될 때 까지의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eea-130">-상태</span><span class="sxs-lookup"><span data-stu-id="a9eea-130">-Status</span></span>
<span data-ttu-id="a9eea-131">파이프라인의 상태가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-131">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a9eea-132">입력</span><span class="sxs-lookup"><span data-stu-id="a9eea-132">INPUTS</span></span>

### <span data-ttu-id="a9eea-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9eea-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="a9eea-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9eea-134">System.String</span></span>


## <span data-ttu-id="a9eea-135">출력</span><span class="sxs-lookup"><span data-stu-id="a9eea-135">OUTPUTS</span></span>

### <span data-ttu-id="a9eea-136">DataFactoryV2 ' 1 [[Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]) 목록 ' ' '을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eea-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a9eea-137">DataFactoryV2. PSActivityRun.</span><span class="sxs-lookup"><span data-stu-id="a9eea-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>


## <span data-ttu-id="a9eea-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a9eea-138">NOTES</span></span>

## <span data-ttu-id="a9eea-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9eea-139">RELATED LINKS</span></span>
[<span data-ttu-id="a9eea-140">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="a9eea-140">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a9eea-141">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a9eea-141">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

