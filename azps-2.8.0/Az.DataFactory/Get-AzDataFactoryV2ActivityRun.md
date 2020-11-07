---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5f6c56fac892e2c3e9c1546dac226c5d81ddb99e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697068"
---
# <span data-ttu-id="c19ff-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="c19ff-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="c19ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c19ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c19ff-103">파이프라인 실행에 대 한 작업 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="c19ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c19ff-104">SYNTAX</span></span>

### <span data-ttu-id="c19ff-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c19ff-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c19ff-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c19ff-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c19ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c19ff-107">DESCRIPTION</span></span>
<span data-ttu-id="c19ff-108">**AzDataFactoryV2ActivityRun** cmdlet은 지정 된 기간에 발생 한 지정한 파이프라인 실행에 대 한 Azure Data Factory의 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="c19ff-109">또한 활동 이름, 실행을 실행 한 연결 된 서비스 이름 및 실행 상태에 대 한 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="c19ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c19ff-110">EXAMPLES</span></span>

### <span data-ttu-id="c19ff-111">예제 1: 파이프라인 실행에 대 한 모든 작업 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="c19ff-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="c19ff-112">이 명령은 "2017-09-01" 및 "2017-09-30" 사이에서 발생 하는 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621"로 실행 되는 파이프라인의 모든 작업 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="c19ff-113">변수</span><span class="sxs-lookup"><span data-stu-id="c19ff-113">PARAMETERS</span></span>

### <span data-ttu-id="c19ff-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="c19ff-114">-ActivityName</span></span>
<span data-ttu-id="c19ff-115">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-115">The name of the activity.</span></span>

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

### <span data-ttu-id="c19ff-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c19ff-116">-DataFactory</span></span>
<span data-ttu-id="c19ff-117">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-117">The data factory object.</span></span>

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

### <span data-ttu-id="c19ff-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c19ff-118">-DataFactoryName</span></span>
<span data-ttu-id="c19ff-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-119">The data factory name.</span></span>

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

### <span data-ttu-id="c19ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19ff-120">-DefaultProfile</span></span>
<span data-ttu-id="c19ff-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c19ff-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c19ff-122">-PipelineRunId</span></span>
<span data-ttu-id="c19ff-123">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="c19ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="c19ff-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-125">The resource group name.</span></span>

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

### <span data-ttu-id="c19ff-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c19ff-126">-RunStartedAfter</span></span>
<span data-ttu-id="c19ff-127">파이프라인 실행이 시작 될 때 또는 그 뒤의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="c19ff-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c19ff-128">-RunStartedBefore</span></span>
<span data-ttu-id="c19ff-129">파이프라인 실행이 시작 될 때 까지의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="c19ff-130">-상태</span><span class="sxs-lookup"><span data-stu-id="c19ff-130">-Status</span></span>
<span data-ttu-id="c19ff-131">파이프라인의 상태가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="c19ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19ff-132">CommonParameters</span></span>
<span data-ttu-id="c19ff-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c19ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19ff-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19ff-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19ff-135">입력</span><span class="sxs-lookup"><span data-stu-id="c19ff-135">INPUTS</span></span>

### <span data-ttu-id="c19ff-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c19ff-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="c19ff-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c19ff-137">System.String</span></span>

## <span data-ttu-id="c19ff-138">출력</span><span class="sxs-lookup"><span data-stu-id="c19ff-138">OUTPUTS</span></span>

### <span data-ttu-id="c19ff-139">DataFactoryV2. PSActivityRun.</span><span class="sxs-lookup"><span data-stu-id="c19ff-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="c19ff-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c19ff-140">NOTES</span></span>

## <span data-ttu-id="c19ff-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c19ff-141">RELATED LINKS</span></span>

[<span data-ttu-id="c19ff-142">AzDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="c19ff-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c19ff-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c19ff-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

