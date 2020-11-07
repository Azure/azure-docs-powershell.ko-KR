---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: fe5359740975776e5796dce2a6d4959ed289cae6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868789"
---
# <span data-ttu-id="32252-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="32252-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="32252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32252-102">SYNOPSIS</span></span>
<span data-ttu-id="32252-103">Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="32252-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32252-104">SYNTAX</span></span>

### <span data-ttu-id="32252-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="32252-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32252-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="32252-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32252-107">설명은</span><span class="sxs-lookup"><span data-stu-id="32252-107">DESCRIPTION</span></span>
<span data-ttu-id="32252-108">**AzDataFactoryDataset** Cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="32252-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="32252-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="32252-111">예제의</span><span class="sxs-lookup"><span data-stu-id="32252-111">EXAMPLES</span></span>

### <span data-ttu-id="32252-112">예제 1: 모든 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="32252-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="32252-113">이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="32252-114">예제 2: 특정 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="32252-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="32252-115">이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="32252-116">예제 3: 특정 데이터 집합의 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="32252-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="32252-117">이 명령은 WikiADF 이라는 data factory에서 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 데이터 집합과 연결 된 **위치** 를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="32252-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="32252-118">또는 **AzDataFactoryDataset** cmdlet의 출력을 변수에 할당 한 다음 점 표기법을 사용 하 여 해당 변수에 저장 된 dataset 개체와 연결 된 Location 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="32252-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="32252-119">변수</span><span class="sxs-lookup"><span data-stu-id="32252-119">PARAMETERS</span></span>

### <span data-ttu-id="32252-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="32252-120">-DataFactory</span></span>
<span data-ttu-id="32252-121">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32252-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="32252-122">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="32252-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="32252-123">-DataFactoryName</span></span>
<span data-ttu-id="32252-124">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32252-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="32252-125">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="32252-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32252-126">-DefaultProfile</span></span>
<span data-ttu-id="32252-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32252-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32252-128">-이름</span><span class="sxs-lookup"><span data-stu-id="32252-128">-Name</span></span>
<span data-ttu-id="32252-129">이 cmdlet에 대 한 정보를 가져오는 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32252-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32252-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32252-130">-ResourceGroupName</span></span>
<span data-ttu-id="32252-131">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32252-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="32252-132">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32252-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="32252-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32252-133">CommonParameters</span></span>
<span data-ttu-id="32252-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32252-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32252-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32252-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32252-136">입력</span><span class="sxs-lookup"><span data-stu-id="32252-136">INPUTS</span></span>

### <span data-ttu-id="32252-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="32252-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="32252-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32252-138">System.String</span></span>

## <span data-ttu-id="32252-139">출력</span><span class="sxs-lookup"><span data-stu-id="32252-139">OUTPUTS</span></span>

### <span data-ttu-id="32252-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="32252-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="32252-141">상속자</span><span class="sxs-lookup"><span data-stu-id="32252-141">NOTES</span></span>
* <span data-ttu-id="32252-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="32252-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="32252-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32252-143">RELATED LINKS</span></span>

[<span data-ttu-id="32252-144">새로운 AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="32252-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="32252-145">제거-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="32252-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


