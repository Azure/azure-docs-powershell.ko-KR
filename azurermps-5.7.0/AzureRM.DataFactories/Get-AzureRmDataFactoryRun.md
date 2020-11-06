---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: a430156dcd49e9bfd69766ab4cfe112c60aef549
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531060"
---
# <span data-ttu-id="70623-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="70623-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="70623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70623-102">SYNOPSIS</span></span>
<span data-ttu-id="70623-103">Azure Data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70623-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70623-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70623-104">SYNTAX</span></span>

### <span data-ttu-id="70623-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="70623-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70623-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="70623-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70623-107">설명은</span><span class="sxs-lookup"><span data-stu-id="70623-107">DESCRIPTION</span></span>
<span data-ttu-id="70623-108">**AzureRmDataFactoryRun** Cmdlet은 Azure data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70623-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="70623-109">Data factory의 데이터 집합은 시간 축을 기준으로 분할 영역으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="70623-110">조각의 너비는 일정에 따라 매시간 또는 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70623-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="70623-111">실행은 조각의 처리 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="70623-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="70623-112">다시 시도 하는 경우 또는 오류가 발생 하 여 조각을 실행 하는 경우 조각에 대해 하나 이상의 실행이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70623-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="70623-113">조각은 시작 시간으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="70623-114">조각의 시작 시간을 얻으려면 Get-AzureRmDataFactorySlice cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="70623-115">예를 들어 다음 조각의 실행을 가져오려면 시작 시간 2015-04-02 T20:00:00을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="70623-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset 시작: 5/2/2014 8:00:00 PM 끝: 5/3/2014 8:00:00 PM RetryCount: 0 상태: 준비 LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="70623-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="70623-117">예제의</span><span class="sxs-lookup"><span data-stu-id="70623-117">EXAMPLES</span></span>

### <span data-ttu-id="70623-118">예제 1: 데이터 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="70623-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="70623-119">이 명령은 05/21/2014의 오후 4 시 GMT에서 시작 하는 WikiADF 라는 data factory의 DAWikiAggregatedData 이라는 데이터 집합의 조각에 대 한 모든 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70623-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="70623-120">변수</span><span class="sxs-lookup"><span data-stu-id="70623-120">PARAMETERS</span></span>

### <span data-ttu-id="70623-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="70623-121">-DataFactory</span></span>
<span data-ttu-id="70623-122">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="70623-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70623-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="70623-124">-DataFactoryName</span></span>
<span data-ttu-id="70623-125">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="70623-126">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="70623-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="70623-127">-DatasetName</span></span>
<span data-ttu-id="70623-128">데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="70623-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 슬라이스에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70623-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70623-130">-DefaultProfile</span></span>
<span data-ttu-id="70623-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70623-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70623-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70623-132">-ResourceGroupName</span></span>
<span data-ttu-id="70623-133">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="70623-134">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 슬라이스에 대 한 팩토리 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70623-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="70623-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="70623-135">-StartDateTime</span></span>
<span data-ttu-id="70623-136">시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="70623-137">이 cmdlet은이 기간에 일치 하는 데이터 조각에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70623-137">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="70623-138">*StartDateTime* 는 다음 예와 같이 ISO8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="70623-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시)</span><span class="sxs-lookup"><span data-stu-id="70623-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="70623-140">기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="70623-140">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="70623-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70623-141">CommonParameters</span></span>
<span data-ttu-id="70623-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70623-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70623-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70623-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70623-144">입력</span><span class="sxs-lookup"><span data-stu-id="70623-144">INPUTS</span></span>

### <span data-ttu-id="70623-145">않아야</span><span class="sxs-lookup"><span data-stu-id="70623-145">None</span></span>
<span data-ttu-id="70623-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70623-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70623-147">출력</span><span class="sxs-lookup"><span data-stu-id="70623-147">OUTPUTS</span></span>

### <span data-ttu-id="70623-148">System.webserver. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDAtaslice 2, WindowsAzure. 유틸리티, 버전 = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="70623-148">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="70623-149">상속자</span><span class="sxs-lookup"><span data-stu-id="70623-149">NOTES</span></span>
* <span data-ttu-id="70623-150">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="70623-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="70623-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70623-151">RELATED LINKS</span></span>

[<span data-ttu-id="70623-152">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="70623-152">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


