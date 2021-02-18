---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181057"
---
# <span data-ttu-id="4879a-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="4879a-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="4879a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4879a-102">SYNOPSIS</span></span>
<span data-ttu-id="4879a-103">Azure Data Factory의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="4879a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4879a-104">SYNTAX</span></span>

### <span data-ttu-id="4879a-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4879a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4879a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4879a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4879a-107">설명</span><span class="sxs-lookup"><span data-stu-id="4879a-107">DESCRIPTION</span></span>
<span data-ttu-id="4879a-108">**Get-AzDataFactoryDataset** cmdlet은 Azure Data Factory의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="4879a-109">데이터 세트의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="4879a-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="4879a-111">예제</span><span class="sxs-lookup"><span data-stu-id="4879a-111">EXAMPLES</span></span>

### <span data-ttu-id="4879a-112">예제 1: 모든 데이터 세트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="4879a-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="4879a-113">이 명령은 WikiADF라는 데이터 팩터리의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="4879a-114">예제 2: 특정 데이터 세트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="4879a-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="4879a-115">이 명령은 WikiADF라는 데이터 팩터리의 DAWikipediaClickEvents라는 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="4879a-116">예제 3: 특정 데이터 세트의 위치 얻기</span><span class="sxs-lookup"><span data-stu-id="4879a-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="4879a-117">이 명령은 WikiADF라는 데이터 팩터리에서 DAWikipediaClickEvents라는 데이터 세트에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 데이터 세트와 연결된 위치를 찍습니다. </span><span class="sxs-lookup"><span data-stu-id="4879a-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="4879a-118">**또는 Get-AzDataFactoryDataset** cmdlet의 출력을 변수에 할당한 다음 점 표시를 사용하여 해당 변수에 저장된 데이터 세트 개체와 연결된 Location 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="4879a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4879a-119">PARAMETERS</span></span>

### <span data-ttu-id="4879a-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-120">-DataFactory</span></span>
<span data-ttu-id="4879a-121">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="4879a-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4879a-122">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4879a-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4879a-123">-DataFactoryName</span></span>
<span data-ttu-id="4879a-124">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4879a-125">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4879a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4879a-126">-DefaultProfile</span></span>
<span data-ttu-id="4879a-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4879a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4879a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4879a-128">-Name</span></span>
<span data-ttu-id="4879a-129">이 cmdlet에서 정보를 얻을 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="4879a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4879a-130">-ResourceGroupName</span></span>
<span data-ttu-id="4879a-131">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4879a-132">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4879a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4879a-133">CommonParameters</span></span>
<span data-ttu-id="4879a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4879a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4879a-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4879a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4879a-136">입력</span><span class="sxs-lookup"><span data-stu-id="4879a-136">INPUTS</span></span>

### <span data-ttu-id="4879a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4879a-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4879a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4879a-138">System.String</span></span>

## <span data-ttu-id="4879a-139">출력</span><span class="sxs-lookup"><span data-stu-id="4879a-139">OUTPUTS</span></span>

### <span data-ttu-id="4879a-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="4879a-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="4879a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4879a-141">NOTES</span></span>
* <span data-ttu-id="4879a-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="4879a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4879a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4879a-143">RELATED LINKS</span></span>

[<span data-ttu-id="4879a-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="4879a-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="4879a-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="4879a-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


