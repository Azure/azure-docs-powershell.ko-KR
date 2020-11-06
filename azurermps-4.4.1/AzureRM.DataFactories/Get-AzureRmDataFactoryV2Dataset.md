---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528220"
---
# <span data-ttu-id="b8ad5-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8ad5-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="b8ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ad5-103">Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ad5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8ad5-104">SYNTAX</span></span>

### <span data-ttu-id="b8ad5-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8ad5-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8ad5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8ad5-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ad5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8ad5-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ad5-108">Get-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="b8ad5-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="b8ad5-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="b8ad5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b8ad5-111">EXAMPLES</span></span>

### <span data-ttu-id="b8ad5-112">예제 1: 모든 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8ad5-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="b8ad5-113">이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b8ad5-114">예제 2: 특정 데이터 집합에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8ad5-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="b8ad5-115">이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="b8ad5-116">변수</span><span class="sxs-lookup"><span data-stu-id="b8ad5-116">PARAMETERS</span></span>

### <span data-ttu-id="b8ad5-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8ad5-117">-DataFactory</span></span>
<span data-ttu-id="b8ad5-118">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b8ad5-119">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="b8ad5-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8ad5-120">-DataFactoryName</span></span>
<span data-ttu-id="b8ad5-121">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b8ad5-122">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8ad5-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b8ad5-123">-Name</span></span>
<span data-ttu-id="b8ad5-124">정보를 가져올 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ad5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ad5-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8ad5-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b8ad5-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8ad5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ad5-128">-DefaultProfile</span></span>
<span data-ttu-id="b8ad5-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ad5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ad5-130">CommonParameters</span></span>
<span data-ttu-id="b8ad5-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ad5-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ad5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ad5-133">입력</span><span class="sxs-lookup"><span data-stu-id="b8ad5-133">INPUTS</span></span>

### <span data-ttu-id="b8ad5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8ad5-134">System.String</span></span>
<span data-ttu-id="b8ad5-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b8ad5-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b8ad5-136">출력</span><span class="sxs-lookup"><span data-stu-id="b8ad5-136">OUTPUTS</span></span>

### <span data-ttu-id="b8ad5-137">Ataset ' 1 [[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSD], Microsoft DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null])</span><span class="sxs-lookup"><span data-stu-id="b8ad5-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b8ad5-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="b8ad5-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="b8ad5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b8ad5-139">NOTES</span></span>
<span data-ttu-id="b8ad5-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="b8ad5-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8ad5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8ad5-141">RELATED LINKS</span></span>

[<span data-ttu-id="b8ad5-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8ad5-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="b8ad5-143">제거-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8ad5-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
