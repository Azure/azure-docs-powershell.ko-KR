---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495651"
---
# <span data-ttu-id="c0712-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0712-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="c0712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0712-102">SYNOPSIS</span></span>
<span data-ttu-id="c0712-103">Data Factory의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="c0712-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0712-104">SYNTAX</span></span>

### <span data-ttu-id="c0712-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0712-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0712-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c0712-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0712-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0712-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0712-108">설명</span><span class="sxs-lookup"><span data-stu-id="c0712-108">DESCRIPTION</span></span>
<span data-ttu-id="c0712-109">Get-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="c0712-110">데이터 세트의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="c0712-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="c0712-112">예제</span><span class="sxs-lookup"><span data-stu-id="c0712-112">EXAMPLES</span></span>

### <span data-ttu-id="c0712-113">예제 1: 모든 데이터 세트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="c0712-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="c0712-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c0712-115">예제 2: 특정 데이터 세트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="c0712-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="c0712-116">이 명령은 WikiADF라는 데이터 팩터리의 DAWikipediaClickEvents라는 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="c0712-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0712-117">PARAMETERS</span></span>

### <span data-ttu-id="c0712-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c0712-118">-DataFactory</span></span>
<span data-ttu-id="c0712-119">PSDataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="c0712-120">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0712-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0712-121">-DataFactoryName</span></span>
<span data-ttu-id="c0712-122">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c0712-123">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0712-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0712-124">-DefaultProfile</span></span>
<span data-ttu-id="c0712-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0712-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c0712-126">-Name</span></span>
<span data-ttu-id="c0712-127">정보를 얻을 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="c0712-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0712-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0712-129">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c0712-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0712-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0712-131">-ResourceId</span></span>
<span data-ttu-id="c0712-132">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c0712-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0712-133">CommonParameters</span></span>
<span data-ttu-id="c0712-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0712-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0712-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0712-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0712-136">입력</span><span class="sxs-lookup"><span data-stu-id="c0712-136">INPUTS</span></span>

### <span data-ttu-id="c0712-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c0712-137">System.String</span></span>

### <span data-ttu-id="c0712-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c0712-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c0712-139">출력</span><span class="sxs-lookup"><span data-stu-id="c0712-139">OUTPUTS</span></span>

### <span data-ttu-id="c0712-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c0712-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="c0712-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0712-141">NOTES</span></span>
<span data-ttu-id="c0712-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="c0712-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c0712-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0712-143">RELATED LINKS</span></span>

[<span data-ttu-id="c0712-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0712-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="c0712-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0712-145">Remove-AzDataFactoryV2Dataset</span></span>]()
