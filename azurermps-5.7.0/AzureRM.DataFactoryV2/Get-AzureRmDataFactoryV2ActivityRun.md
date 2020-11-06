---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 300aad37f2dede64a4adebc4f1a9d9eb9cc43743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526867"
---
# <span data-ttu-id="eb2c8-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="eb2c8-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="eb2c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2c8-103">파이프라인 실행에 대 한 작업 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb2c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb2c8-104">SYNTAX</span></span>

### <span data-ttu-id="eb2c8-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb2c8-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb2c8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb2c8-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb2c8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb2c8-107">DESCRIPTION</span></span>
<span data-ttu-id="eb2c8-108">**AzureRmDataFactoryV2ActivityRun** cmdlet은 지정 된 기간에 발생 한 지정한 파이프라인 실행에 대 한 Azure Data Factory의 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="eb2c8-109">또한 활동 이름, 실행을 실행 한 연결 된 서비스 이름 및 실행 상태에 대 한 필터를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="eb2c8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eb2c8-110">EXAMPLES</span></span>

### <span data-ttu-id="eb2c8-111">예제 1: 파이프라인 실행에 대 한 모든 작업 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="eb2c8-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="eb2c8-112">이 명령은 "2017-09-01" 및 "2017-09-30" 사이에서 발생 하는 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621"로 실행 되는 파이프라인의 모든 작업 실행에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="eb2c8-113">변수</span><span class="sxs-lookup"><span data-stu-id="eb2c8-113">PARAMETERS</span></span>

### <span data-ttu-id="eb2c8-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="eb2c8-114">-ActivityName</span></span>
<span data-ttu-id="eb2c8-115">활동의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-115">The name of the activity.</span></span>

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

### <span data-ttu-id="eb2c8-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb2c8-116">-DataFactory</span></span>
<span data-ttu-id="eb2c8-117">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-117">The data factory object.</span></span>

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

### <span data-ttu-id="eb2c8-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="eb2c8-118">-DataFactoryName</span></span>
<span data-ttu-id="eb2c8-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-119">The data factory name.</span></span>

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

### <span data-ttu-id="eb2c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2c8-120">-DefaultProfile</span></span>
<span data-ttu-id="eb2c8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2c8-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="eb2c8-122">-LinkedServiceName</span></span>
<span data-ttu-id="eb2c8-123">연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-123">The linked service name.</span></span>

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

### <span data-ttu-id="eb2c8-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="eb2c8-124">-PipelineRunId</span></span>
<span data-ttu-id="eb2c8-125">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="eb2c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb2c8-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-127">The resource group name.</span></span>

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

### <span data-ttu-id="eb2c8-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="eb2c8-128">-RunStartedAfter</span></span>
<span data-ttu-id="eb2c8-129">파이프라인 실행이 시작 될 때 또는 그 뒤의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="eb2c8-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="eb2c8-130">-RunStartedBefore</span></span>
<span data-ttu-id="eb2c8-131">파이프라인 실행이 시작 될 때 까지의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="eb2c8-132">-상태</span><span class="sxs-lookup"><span data-stu-id="eb2c8-132">-Status</span></span>
<span data-ttu-id="eb2c8-133">파이프라인의 상태가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="eb2c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2c8-134">CommonParameters</span></span>
<span data-ttu-id="eb2c8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2c8-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb2c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2c8-137">입력</span><span class="sxs-lookup"><span data-stu-id="eb2c8-137">INPUTS</span></span>

### <span data-ttu-id="eb2c8-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb2c8-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="eb2c8-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb2c8-139">System.String</span></span>

## <span data-ttu-id="eb2c8-140">출력</span><span class="sxs-lookup"><span data-stu-id="eb2c8-140">OUTPUTS</span></span>

### <span data-ttu-id="eb2c8-141">DataFactoryV2 ' 1 [[Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]) 목록 ' ' '을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="eb2c8-142">DataFactoryV2. PSActivityRun.</span><span class="sxs-lookup"><span data-stu-id="eb2c8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="eb2c8-143">상속자</span><span class="sxs-lookup"><span data-stu-id="eb2c8-143">NOTES</span></span>

## <span data-ttu-id="eb2c8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb2c8-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb2c8-145">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="eb2c8-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="eb2c8-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="eb2c8-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

