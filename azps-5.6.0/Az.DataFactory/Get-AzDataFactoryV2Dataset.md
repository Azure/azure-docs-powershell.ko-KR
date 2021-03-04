---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 938b51b6025a420570ad62b4e9ce815fe832c4cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975275"
---
# <span data-ttu-id="1d60e-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1d60e-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="1d60e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d60e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d60e-103">Data Factory에서 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="1d60e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d60e-104">SYNTAX</span></span>

### <span data-ttu-id="1d60e-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d60e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d60e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1d60e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d60e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d60e-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d60e-108">설명</span><span class="sxs-lookup"><span data-stu-id="1d60e-108">DESCRIPTION</span></span>
<span data-ttu-id="1d60e-109">Get-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="1d60e-110">데이터 세트의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="1d60e-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 데이터 세트에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="1d60e-112">예제</span><span class="sxs-lookup"><span data-stu-id="1d60e-112">EXAMPLES</span></span>

### <span data-ttu-id="1d60e-113">예제 1: 모든 데이터 세트에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="1d60e-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1d60e-115">예제 2: 특정 데이터 세트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="1d60e-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="1d60e-116">이 명령은 WikiADF라는 데이터 팩터리에서 DAWikipediaClickEvents라는 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="1d60e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d60e-117">PARAMETERS</span></span>

### <span data-ttu-id="1d60e-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d60e-118">-DataFactory</span></span>
<span data-ttu-id="1d60e-119">PSDataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="1d60e-120">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d60e-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1d60e-121">-DataFactoryName</span></span>
<span data-ttu-id="1d60e-122">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1d60e-123">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d60e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d60e-124">-DefaultProfile</span></span>
<span data-ttu-id="1d60e-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d60e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1d60e-126">-Name</span></span>
<span data-ttu-id="1d60e-127">정보를 얻을 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d60e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d60e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d60e-129">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1d60e-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d60e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d60e-131">-ResourceId</span></span>
<span data-ttu-id="1d60e-132">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-132">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d60e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d60e-133">CommonParameters</span></span>
<span data-ttu-id="1d60e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d60e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d60e-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d60e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d60e-136">입력</span><span class="sxs-lookup"><span data-stu-id="1d60e-136">INPUTS</span></span>

### <span data-ttu-id="1d60e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1d60e-137">System.String</span></span>

### <span data-ttu-id="1d60e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1d60e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1d60e-139">출력</span><span class="sxs-lookup"><span data-stu-id="1d60e-139">OUTPUTS</span></span>

### <span data-ttu-id="1d60e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="1d60e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="1d60e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d60e-141">NOTES</span></span>
<span data-ttu-id="1d60e-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="1d60e-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1d60e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d60e-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d60e-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1d60e-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="1d60e-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1d60e-145">Remove-AzDataFactoryV2Dataset</span></span>]()
