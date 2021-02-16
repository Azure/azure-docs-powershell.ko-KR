---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208765"
---
# <span data-ttu-id="90989-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="90989-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="90989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90989-102">SYNOPSIS</span></span>
<span data-ttu-id="90989-103">Azure Data Factory에서 데이터 세트의 데이터 조각에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="90989-104">구문</span><span class="sxs-lookup"><span data-stu-id="90989-104">SYNTAX</span></span>

### <span data-ttu-id="90989-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="90989-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90989-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="90989-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90989-107">설명</span><span class="sxs-lookup"><span data-stu-id="90989-107">DESCRIPTION</span></span>
<span data-ttu-id="90989-108">**Get-AzDataFactoryRun** cmdlet은 Azure Data Factory에서 데이터 세트의 데이터 조각에 대한 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90989-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="90989-109">데이터 팩터리의 데이터 세트는 시간 축에 대한 조각으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="90989-110">조각의 너비는 시간별 또는 매일 일정에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="90989-111">실행은 조각에 대한 처리 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="90989-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="90989-112">재시도의 경우 또는 실패로 인해 조각을 다시 실행하는 경우 조각에 대해 하나 이상의 실행이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90989-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="90989-113">조각은 시작 시간으로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="90989-114">조각의 시작 시간을 얻습니다. Get-AzDataFactorySlice cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="90989-115">예를 들어 다음 조각에 대해 실행하려면 시작 시간 2015-04-02T20:00:00을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="90989-116">ResourceGroupName : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2 014 8:00:00 PM 종료: 2014/5/3 오후 8:00:00 PM RetryCount : 0 상태 : Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="90989-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="90989-117">예제</span><span class="sxs-lookup"><span data-stu-id="90989-117">EXAMPLES</span></span>

### <span data-ttu-id="90989-118">예제 1: 데이터 세트 얻기</span><span class="sxs-lookup"><span data-stu-id="90989-118">Example 1: Get a dataset</span></span>
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

<span data-ttu-id="90989-119">이 명령은 2014년 5월 21일 오후 4시 GMT에서 시작하는 WikiADF라는 데이터 팩터리에서 DAWikiAggregatedData라는 데이터 세트의 조각에 대한 모든 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90989-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="90989-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90989-120">PARAMETERS</span></span>

### <span data-ttu-id="90989-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="90989-121">-DataFactory</span></span>
<span data-ttu-id="90989-122">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="90989-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="90989-123">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="90989-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="90989-124">-DataFactoryName</span></span>
<span data-ttu-id="90989-125">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="90989-126">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="90989-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="90989-127">-DatasetName</span></span>
<span data-ttu-id="90989-128">데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="90989-129">이 cmdlet은 이 매개 변수가 지정하는 데이터 세트에 속하는 조각에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="90989-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90989-130">-DefaultProfile</span></span>
<span data-ttu-id="90989-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90989-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90989-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90989-132">-ResourceGroupName</span></span>
<span data-ttu-id="90989-133">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="90989-134">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 조각에 대해 팩터리 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90989-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="90989-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="90989-135">-StartDateTime</span></span>
<span data-ttu-id="90989-136">기간의 시작을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="90989-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="90989-137">이 cmdlet은 이 기간과 일치하는 데이터 조각에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="90989-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="90989-138">*StartDateTime은* 다음 예제와 같이 ISO8601 형식으로 지정해야 합니다. 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-00 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="90989-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="90989-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90989-139">CommonParameters</span></span>
<span data-ttu-id="90989-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90989-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90989-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90989-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90989-142">입력</span><span class="sxs-lookup"><span data-stu-id="90989-142">INPUTS</span></span>

### <span data-ttu-id="90989-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="90989-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="90989-144">System.String</span><span class="sxs-lookup"><span data-stu-id="90989-144">System.String</span></span>

## <span data-ttu-id="90989-145">출력</span><span class="sxs-lookup"><span data-stu-id="90989-145">OUTPUTS</span></span>

### <span data-ttu-id="90989-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="90989-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="90989-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90989-147">NOTES</span></span>
* <span data-ttu-id="90989-148">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="90989-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90989-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90989-149">RELATED LINKS</span></span>

[<span data-ttu-id="90989-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="90989-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


