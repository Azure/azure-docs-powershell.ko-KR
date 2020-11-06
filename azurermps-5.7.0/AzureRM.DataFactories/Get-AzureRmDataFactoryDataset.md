---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 10e4af67d76e6c9d367de4d9b512d003e211ddae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531074"
---
# <span data-ttu-id="46c8b-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="46c8b-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="46c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="46c8b-103">Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46c8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46c8b-104">SYNTAX</span></span>

### <span data-ttu-id="46c8b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="46c8b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46c8b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="46c8b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46c8b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="46c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="46c8b-108">**AzureRmDataFactoryDataset** Cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="46c8b-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="46c8b-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="46c8b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="46c8b-111">EXAMPLES</span></span>

### <span data-ttu-id="46c8b-112">예제 1: 모든 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="46c8b-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="46c8b-113">이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="46c8b-114">예제 2: 특정 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="46c8b-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="46c8b-115">이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="46c8b-116">예제 3: 특정 데이터 집합의 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="46c8b-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="46c8b-117">이 명령은 WikiADF 이라는 data factory에서 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 데이터 집합과 연결 된 **위치** 를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="46c8b-118">또는 **AzureRmDataFactoryDataset** cmdlet의 출력을 변수에 할당 한 다음 점 표기법을 사용 하 여 해당 변수에 저장 된 dataset 개체와 연결 된 Location 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="46c8b-119">변수</span><span class="sxs-lookup"><span data-stu-id="46c8b-119">PARAMETERS</span></span>

### <span data-ttu-id="46c8b-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="46c8b-120">-DataFactory</span></span>
<span data-ttu-id="46c8b-121">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="46c8b-122">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="46c8b-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="46c8b-123">-DataFactoryName</span></span>
<span data-ttu-id="46c8b-124">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="46c8b-125">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="46c8b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c8b-126">-DefaultProfile</span></span>
<span data-ttu-id="46c8b-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46c8b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46c8b-128">-이름</span><span class="sxs-lookup"><span data-stu-id="46c8b-128">-Name</span></span>
<span data-ttu-id="46c8b-129">이 cmdlet에 대 한 정보를 가져오는 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c8b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c8b-130">-ResourceGroupName</span></span>
<span data-ttu-id="46c8b-131">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="46c8b-132">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="46c8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c8b-133">CommonParameters</span></span>
<span data-ttu-id="46c8b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c8b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c8b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c8b-136">입력</span><span class="sxs-lookup"><span data-stu-id="46c8b-136">INPUTS</span></span>

### <span data-ttu-id="46c8b-137">않아야</span><span class="sxs-lookup"><span data-stu-id="46c8b-137">None</span></span>
<span data-ttu-id="46c8b-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46c8b-139">출력</span><span class="sxs-lookup"><span data-stu-id="46c8b-139">OUTPUTS</span></span>

### <span data-ttu-id="46c8b-140">Ataset ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSD], WindowsAzure. 유틸리티, Version = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="46c8b-140">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="46c8b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="46c8b-141">NOTES</span></span>
* <span data-ttu-id="46c8b-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="46c8b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="46c8b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46c8b-143">RELATED LINKS</span></span>

[<span data-ttu-id="46c8b-144">새로운 AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="46c8b-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="46c8b-145">제거-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="46c8b-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)

