---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306329"
---
# <span data-ttu-id="528d4-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="528d4-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="528d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="528d4-102">SYNOPSIS</span></span>
<span data-ttu-id="528d4-103">Azure Data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="528d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="528d4-104">SYNTAX</span></span>

### <span data-ttu-id="528d4-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="528d4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="528d4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="528d4-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="528d4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="528d4-107">DESCRIPTION</span></span>
<span data-ttu-id="528d4-108">**AzDataFactoryRun** Cmdlet은 Azure data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="528d4-109">Data factory의 데이터 집합은 시간 축을 기준으로 분할 영역으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="528d4-110">조각의 너비는 일정에 따라 매시간 또는 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="528d4-111">실행은 조각의 처리 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="528d4-112">다시 시도 하는 경우 또는 오류가 발생 하 여 조각을 실행 하는 경우 조각에 대해 하나 이상의 실행이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="528d4-113">조각은 시작 시간으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="528d4-114">조각의 시작 시간을 얻으려면 Get-AzDataFactorySlice cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="528d4-115">예를 들어 다음 조각의 실행을 가져오려면 시작 시간 2015-04-02 T20:00:00을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="528d4-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset 시작: 5/2/2014 8:00:00 PM 끝: 5/3/2014 8:00:00 PM RetryCount: 0 상태: 준비 LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="528d4-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="528d4-117">예제의</span><span class="sxs-lookup"><span data-stu-id="528d4-117">EXAMPLES</span></span>

### <span data-ttu-id="528d4-118">예제 1: 데이터 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="528d4-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="528d4-119">이 명령은 05/21/2014의 오후 4 시 GMT에서 시작 하는 WikiADF 라는 data factory의 DAWikiAggregatedData 이라는 데이터 집합의 조각에 대 한 모든 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="528d4-120">변수</span><span class="sxs-lookup"><span data-stu-id="528d4-120">PARAMETERS</span></span>

### <span data-ttu-id="528d4-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="528d4-121">-DataFactory</span></span>
<span data-ttu-id="528d4-122">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="528d4-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="528d4-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="528d4-124">-DataFactoryName</span></span>
<span data-ttu-id="528d4-125">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="528d4-126">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="528d4-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="528d4-127">-DatasetName</span></span>
<span data-ttu-id="528d4-128">데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="528d4-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="528d4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528d4-130">-DefaultProfile</span></span>
<span data-ttu-id="528d4-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="528d4-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="528d4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="528d4-132">-ResourceGroupName</span></span>
<span data-ttu-id="528d4-133">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="528d4-134">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 슬라이스에 대 한 팩토리 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="528d4-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="528d4-135">-StartDateTime</span></span>
<span data-ttu-id="528d4-136">시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="528d4-137">이 cmdlet은이 기간에 일치 하는 데이터 조각에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="528d4-138">*StartDateTime* 는 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 2015-01-01z 2015-01-01T00:00:00z 2015-01-01t00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시) 기본 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="528d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528d4-139">CommonParameters</span></span>
<span data-ttu-id="528d4-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="528d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528d4-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="528d4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528d4-142">입력</span><span class="sxs-lookup"><span data-stu-id="528d4-142">INPUTS</span></span>

### <span data-ttu-id="528d4-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="528d4-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="528d4-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="528d4-144">System.String</span></span>

## <span data-ttu-id="528d4-145">출력</span><span class="sxs-lookup"><span data-stu-id="528d4-145">OUTPUTS</span></span>

### <span data-ttu-id="528d4-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="528d4-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="528d4-147">상속자</span><span class="sxs-lookup"><span data-stu-id="528d4-147">NOTES</span></span>
* <span data-ttu-id="528d4-148">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="528d4-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="528d4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="528d4-149">RELATED LINKS</span></span>

[<span data-ttu-id="528d4-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="528d4-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


