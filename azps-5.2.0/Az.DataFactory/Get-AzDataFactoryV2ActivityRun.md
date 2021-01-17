---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354477"
---
# <span data-ttu-id="319e7-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="319e7-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="319e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="319e7-102">SYNOPSIS</span></span>
<span data-ttu-id="319e7-103">파이프라인 실행에 대한 활동 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="319e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="319e7-104">SYNTAX</span></span>

### <span data-ttu-id="319e7-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="319e7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="319e7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="319e7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="319e7-107">설명</span><span class="sxs-lookup"><span data-stu-id="319e7-107">DESCRIPTION</span></span>
<span data-ttu-id="319e7-108">**Get-AzDataFactoryV2ActivityRun** cmdlet은 지정된 시간 프레임에서 발생된 지정된 파이프라인 실행에 대한 Azure Data Factory의 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="319e7-109">또한 활동 이름, 실행을 실행한 연결된 서비스 이름 및 실행 상태에 대한 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="319e7-110">예제</span><span class="sxs-lookup"><span data-stu-id="319e7-110">EXAMPLES</span></span>

### <span data-ttu-id="319e7-111">예제 1: 파이프라인 실행에 대한 모든 작업 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="319e7-112">이 명령은 "2017-09-01"과 "2017-09-30" 사이에 발생된 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621"을 사용하여 파이프라인 실행의 모든 작업 실행에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="319e7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="319e7-113">PARAMETERS</span></span>

### <span data-ttu-id="319e7-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="319e7-114">-ActivityName</span></span>
<span data-ttu-id="319e7-115">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="319e7-116">-DataFactory</span></span>
<span data-ttu-id="319e7-117">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="319e7-118">-DataFactoryName</span></span>
<span data-ttu-id="319e7-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319e7-120">-DefaultProfile</span></span>
<span data-ttu-id="319e7-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="319e7-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="319e7-122">-PipelineRunId</span></span>
<span data-ttu-id="319e7-123">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="319e7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="319e7-126">-RunStartedAfter</span></span>
<span data-ttu-id="319e7-127">파이프라인 실행이 시작된 시간 또는 그 이후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="319e7-128">-RunStartedBefore</span></span>
<span data-ttu-id="319e7-129">파이프라인 실행이 시작된 시간 또는 이전 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-130">-Status</span><span class="sxs-lookup"><span data-stu-id="319e7-130">-Status</span></span>
<span data-ttu-id="319e7-131">파이프라인 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319e7-132">CommonParameters</span></span>
<span data-ttu-id="319e7-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="319e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319e7-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="319e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319e7-135">입력</span><span class="sxs-lookup"><span data-stu-id="319e7-135">INPUTS</span></span>

### <span data-ttu-id="319e7-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="319e7-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="319e7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="319e7-137">System.String</span></span>

## <span data-ttu-id="319e7-138">출력</span><span class="sxs-lookup"><span data-stu-id="319e7-138">OUTPUTS</span></span>

### <span data-ttu-id="319e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="319e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="319e7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="319e7-140">NOTES</span></span>

## <span data-ttu-id="319e7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="319e7-141">RELATED LINKS</span></span>

[<span data-ttu-id="319e7-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="319e7-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="319e7-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="319e7-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

