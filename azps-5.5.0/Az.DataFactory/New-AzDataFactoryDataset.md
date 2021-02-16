---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208741"
---
# <span data-ttu-id="02afe-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="02afe-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="02afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02afe-102">SYNOPSIS</span></span>
<span data-ttu-id="02afe-103">Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="02afe-104">구문</span><span class="sxs-lookup"><span data-stu-id="02afe-104">SYNTAX</span></span>

### <span data-ttu-id="02afe-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="02afe-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02afe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="02afe-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02afe-107">설명</span><span class="sxs-lookup"><span data-stu-id="02afe-107">DESCRIPTION</span></span>
<span data-ttu-id="02afe-108">**New-AzDataFactoryDataset** cmdlet은 Azure Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="02afe-109">이미 존재하는 데이터 세트의 이름을 지정하는 경우 이 cmdlet은 데이터 세트를 바꾸기 전에 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="02afe-110">Force 매개 *변수를 지정하면* cmdlet이 확인 없이 기존 데이터 세트를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="02afe-111">다음 순서로 이러한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="02afe-112">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="02afe-112">Create a data factory.</span></span> 
- <span data-ttu-id="02afe-113">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-113">Create linked services.</span></span> 
- <span data-ttu-id="02afe-114">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-114">Create datasets.</span></span> 
- <span data-ttu-id="02afe-115">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-115">Create a pipeline.</span></span>
<span data-ttu-id="02afe-116">동일한 이름의 데이터 세트가 데이터 팩터리에 이미 있는 경우 이 cmdlet은 기존 데이터 세트를 새 데이터 세트로 덮어써야 하는지 여부를 확인하라는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="02afe-117">기존 데이터 세트를 덮어들이는 것이 확인되면 데이터 세트 정의도 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="02afe-118">예제</span><span class="sxs-lookup"><span data-stu-id="02afe-118">EXAMPLES</span></span>

### <span data-ttu-id="02afe-119">예제 1: 데이터 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="02afe-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="02afe-120">이 명령은 WikiADF라는 DA_WikipediaClickEvents 팩터리에 이름의 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="02afe-121">이 명령은 데이터 세트를 on 파일의 DAWikipediaClickEvents.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="02afe-122">예제 2: 새 데이터 세트의 가용성 보기</span><span class="sxs-lookup"><span data-stu-id="02afe-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="02afe-123">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="02afe-124">두 번째 명령은 표준 점 표시를 사용하여 데이터 세트의 가용성 속성에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="02afe-125">예제 3: 새 데이터 세트의 위치 보기</span><span class="sxs-lookup"><span data-stu-id="02afe-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="02afe-126">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="02afe-127">두 번째 명령은 데이터 세트의 Location 속성에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="02afe-128">예제 4: 새 데이터 세트에 대한 유효성 검사 규칙 보기</span><span class="sxs-lookup"><span data-stu-id="02afe-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="02afe-129">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="02afe-130">두 번째 명령은 데이터 세트에 대한 유효성 검사 규칙에 대한 세부 정보를 확인한 다음, 파이프라인 연산자를 사용하여 Format-List cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02afe-131">이 Windows PowerShell 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="02afe-132">자세한 내용은 `Get-Help Format-List` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="02afe-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02afe-133">PARAMETERS</span></span>

### <span data-ttu-id="02afe-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="02afe-134">-DataFactory</span></span>
<span data-ttu-id="02afe-135">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="02afe-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="02afe-136">이 cmdlet은 데이터 팩터리에서 이 매개 변수가 지정하는 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02afe-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="02afe-137">-DataFactoryName</span></span>
<span data-ttu-id="02afe-138">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="02afe-139">이 cmdlet은 데이터 팩터리에서 이 매개 변수가 지정하는 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02afe-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02afe-140">-DefaultProfile</span></span>
<span data-ttu-id="02afe-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="02afe-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02afe-142">-File</span><span class="sxs-lookup"><span data-stu-id="02afe-142">-File</span></span>
<span data-ttu-id="02afe-143">데이터 세트에 대한 설명이 포함된 JSON(JavaScript Object Notation) 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02afe-144">-Force</span><span class="sxs-lookup"><span data-stu-id="02afe-144">-Force</span></span>
<span data-ttu-id="02afe-145">확인 메시지를 표시하지 않고 이 cmdlet이 기존 데이터 세트를 대체하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02afe-146">-Name</span><span class="sxs-lookup"><span data-stu-id="02afe-146">-Name</span></span>
<span data-ttu-id="02afe-147">만들 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="02afe-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02afe-148">-ResourceGroupName</span></span>
<span data-ttu-id="02afe-149">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="02afe-150">이 cmdlet은 이 매개 변수가 지정하는 그룹에 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="02afe-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02afe-151">-Confirm</span></span>
<span data-ttu-id="02afe-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02afe-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02afe-153">-WhatIf</span></span>
<span data-ttu-id="02afe-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="02afe-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02afe-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02afe-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02afe-156">CommonParameters</span></span>
<span data-ttu-id="02afe-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02afe-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02afe-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="02afe-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02afe-159">입력</span><span class="sxs-lookup"><span data-stu-id="02afe-159">INPUTS</span></span>

### <span data-ttu-id="02afe-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="02afe-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="02afe-161">System.String</span><span class="sxs-lookup"><span data-stu-id="02afe-161">System.String</span></span>

## <span data-ttu-id="02afe-162">출력</span><span class="sxs-lookup"><span data-stu-id="02afe-162">OUTPUTS</span></span>

### <span data-ttu-id="02afe-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="02afe-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="02afe-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02afe-164">NOTES</span></span>
* <span data-ttu-id="02afe-165">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="02afe-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="02afe-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02afe-166">RELATED LINKS</span></span>

[<span data-ttu-id="02afe-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="02afe-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="02afe-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="02afe-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


