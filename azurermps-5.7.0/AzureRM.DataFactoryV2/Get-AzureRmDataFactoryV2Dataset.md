---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530546"
---
# <span data-ttu-id="d65a7-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d65a7-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="d65a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d65a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d65a7-103">Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d65a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d65a7-104">SYNTAX</span></span>

### <span data-ttu-id="d65a7-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d65a7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65a7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d65a7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65a7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d65a7-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d65a7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d65a7-108">DESCRIPTION</span></span>
<span data-ttu-id="d65a7-109">Get-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="d65a7-110">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="d65a7-111">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="d65a7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d65a7-112">EXAMPLES</span></span>

### <span data-ttu-id="d65a7-113">예제 1: 모든 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d65a7-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="d65a7-114">이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="d65a7-115">예제 2: 특정 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d65a7-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="d65a7-116">이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="d65a7-117">변수</span><span class="sxs-lookup"><span data-stu-id="d65a7-117">PARAMETERS</span></span>

### <span data-ttu-id="d65a7-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d65a7-118">-DataFactory</span></span>
<span data-ttu-id="d65a7-119">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="d65a7-120">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="d65a7-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d65a7-121">-DataFactoryName</span></span>
<span data-ttu-id="d65a7-122">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d65a7-123">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d65a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65a7-124">-DefaultProfile</span></span>
<span data-ttu-id="d65a7-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65a7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d65a7-126">-Name</span></span>
<span data-ttu-id="d65a7-127">정보를 가져올 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="d65a7-129">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d65a7-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d65a7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d65a7-131">-ResourceId</span></span>
<span data-ttu-id="d65a7-132">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-132">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65a7-133">CommonParameters</span></span>
<span data-ttu-id="d65a7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65a7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d65a7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65a7-136">입력</span><span class="sxs-lookup"><span data-stu-id="d65a7-136">INPUTS</span></span>

### <span data-ttu-id="d65a7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d65a7-137">System.String</span></span>
<span data-ttu-id="d65a7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d65a7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d65a7-139">출력</span><span class="sxs-lookup"><span data-stu-id="d65a7-139">OUTPUTS</span></span>

### <span data-ttu-id="d65a7-140">Ataset ' 1 [[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSD], Microsoft DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null])</span><span class="sxs-lookup"><span data-stu-id="d65a7-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d65a7-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="d65a7-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="d65a7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d65a7-142">NOTES</span></span>
<span data-ttu-id="d65a7-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d65a7-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d65a7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d65a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="d65a7-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d65a7-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="d65a7-146">제거-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d65a7-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
