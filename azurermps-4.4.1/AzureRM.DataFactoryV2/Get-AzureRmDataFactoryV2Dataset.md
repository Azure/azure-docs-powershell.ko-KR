---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537339"
---
# <span data-ttu-id="42b99-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="42b99-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="42b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42b99-102">SYNOPSIS</span></span>
<span data-ttu-id="42b99-103">Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42b99-104">SYNTAX</span></span>

### <span data-ttu-id="42b99-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="42b99-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="42b99-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="42b99-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="42b99-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42b99-107">DESCRIPTION</span></span>
<span data-ttu-id="42b99-108">Get-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="42b99-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="42b99-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="42b99-111">예제의</span><span class="sxs-lookup"><span data-stu-id="42b99-111">EXAMPLES</span></span>

### <span data-ttu-id="42b99-112">예제 1: 모든 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="42b99-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="42b99-113">이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="42b99-114">예제 2: 특정 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="42b99-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="42b99-115">이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="42b99-116">변수</span><span class="sxs-lookup"><span data-stu-id="42b99-116">PARAMETERS</span></span>

### <span data-ttu-id="42b99-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="42b99-117">-DataFactory</span></span>
<span data-ttu-id="42b99-118">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="42b99-119">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="42b99-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="42b99-120">-DataFactoryName</span></span>
<span data-ttu-id="42b99-121">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="42b99-122">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="42b99-123">-이름</span><span class="sxs-lookup"><span data-stu-id="42b99-123">-Name</span></span>
<span data-ttu-id="42b99-124">정보를 가져올 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b99-125">-ResourceGroupName</span></span>
<span data-ttu-id="42b99-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="42b99-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42b99-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="42b99-128">입력</span><span class="sxs-lookup"><span data-stu-id="42b99-128">INPUTS</span></span>

### <span data-ttu-id="42b99-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42b99-129">System.String</span></span>
<span data-ttu-id="42b99-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="42b99-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="42b99-131">출력</span><span class="sxs-lookup"><span data-stu-id="42b99-131">OUTPUTS</span></span>

### <span data-ttu-id="42b99-132">Ataset ' 1 [[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSD], Microsoft DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null])</span><span class="sxs-lookup"><span data-stu-id="42b99-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="42b99-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="42b99-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="42b99-134">상속자</span><span class="sxs-lookup"><span data-stu-id="42b99-134">NOTES</span></span>
<span data-ttu-id="42b99-135">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="42b99-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="42b99-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42b99-136">RELATED LINKS</span></span>
[<span data-ttu-id="42b99-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="42b99-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="42b99-138">제거-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="42b99-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
