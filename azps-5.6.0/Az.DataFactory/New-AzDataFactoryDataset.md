---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: b78d1ef78d7da1f8ad035951174578766de6a4a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975003"
---
# <span data-ttu-id="8b5d8-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8b5d8-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="8b5d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5d8-103">Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="8b5d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b5d8-104">SYNTAX</span></span>

### <span data-ttu-id="8b5d8-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b5d8-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b5d8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8b5d8-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="8b5d8-107">DESCRIPTION</span></span>
<span data-ttu-id="8b5d8-108">**New-AzDataFactoryDataset** cmdlet은 Azure Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="8b5d8-109">이미 있는 데이터 세트의 이름을 지정하는 경우 이 cmdlet은 데이터 세트를 바꾸기 전에 확인을 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="8b5d8-110">Force 매개 *변수를 지정하는* 경우 cmdlet은 확인 없이 기존 데이터 세트를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="8b5d8-111">다음 순서대로 이러한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="8b5d8-112">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="8b5d8-112">Create a data factory.</span></span> 
- <span data-ttu-id="8b5d8-113">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-113">Create linked services.</span></span> 
- <span data-ttu-id="8b5d8-114">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-114">Create datasets.</span></span> 
- <span data-ttu-id="8b5d8-115">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-115">Create a pipeline.</span></span>
<span data-ttu-id="8b5d8-116">동일한 이름의 데이터 세트가 데이터 팩터리에 이미 있는 경우 이 cmdlet은 새 데이터 세트로 기존 데이터 세트를 덮어써야 하는지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="8b5d8-117">기존 데이터 세트를 덮어 우는 것이 확인되면 데이터 세트 정의도 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="8b5d8-118">예제</span><span class="sxs-lookup"><span data-stu-id="8b5d8-118">EXAMPLES</span></span>

### <span data-ttu-id="8b5d8-119">예제 1: 데이터 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="8b5d8-119">Example 1: Create a dataset</span></span>
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

<span data-ttu-id="8b5d8-120">이 명령은 WikiADF라는 DA_WikipediaClickEvents 팩터리에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="8b5d8-121">명령은 데이터 세트를 on 파일의 DAWikipediaClickEvents.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="8b5d8-122">예제 2: 새 데이터 세트의 가용성 보기</span><span class="sxs-lookup"><span data-stu-id="8b5d8-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="8b5d8-123">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 데이터 세트라는 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="8b5d8-124">두 번째 명령은 표준 점표를 사용하여 데이터 세트의 가용성 속성에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="8b5d8-125">예제 3: 새 데이터 세트의 위치 보기</span><span class="sxs-lookup"><span data-stu-id="8b5d8-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="8b5d8-126">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 데이터 세트라는 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="8b5d8-127">두 번째 명령은 데이터 세트의 위치 속성에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="8b5d8-128">예제 4: 새 데이터 세트에 대한 유효성 검사 규칙 보기</span><span class="sxs-lookup"><span data-stu-id="8b5d8-128">Example 4: View validation rules for a new dataset</span></span>
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

<span data-ttu-id="8b5d8-129">첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 데이터 세트라는 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="8b5d8-130">두 번째 명령은 데이터 세트에 대한 유효성 검사 규칙에 대한 세부 정보를 얻은 다음 파이프라인 연산자를 사용하여 Format-List cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b5d8-131">cmdlet이 Windows PowerShell 서식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="8b5d8-132">자세한 내용은 `Get-Help Format-List` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="8b5d8-133">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b5d8-133">PARAMETERS</span></span>

### <span data-ttu-id="8b5d8-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b5d8-134">-DataFactory</span></span>
<span data-ttu-id="8b5d8-135">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="8b5d8-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8b5d8-136">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b5d8-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b5d8-137">-DataFactoryName</span></span>
<span data-ttu-id="8b5d8-138">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8b5d8-139">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b5d8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5d8-140">-DefaultProfile</span></span>
<span data-ttu-id="8b5d8-141">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8b5d8-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b5d8-142">-File</span><span class="sxs-lookup"><span data-stu-id="8b5d8-142">-File</span></span>
<span data-ttu-id="8b5d8-143">데이터 세트에 대한 설명이 포함된 JSON(JavaScript 개체 표기)파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="8b5d8-144">-Force</span><span class="sxs-lookup"><span data-stu-id="8b5d8-144">-Force</span></span>
<span data-ttu-id="8b5d8-145">확인을 요청하지 않고 이 cmdlet이 기존 데이터 세트를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8b5d8-146">-Name</span><span class="sxs-lookup"><span data-stu-id="8b5d8-146">-Name</span></span>
<span data-ttu-id="8b5d8-147">만들 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="8b5d8-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5d8-148">-ResourceGroupName</span></span>
<span data-ttu-id="8b5d8-149">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8b5d8-150">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b5d8-151">-확인</span><span class="sxs-lookup"><span data-stu-id="8b5d8-151">-Confirm</span></span>
<span data-ttu-id="8b5d8-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5d8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5d8-153">-WhatIf</span></span>
<span data-ttu-id="8b5d8-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5d8-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5d8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5d8-156">CommonParameters</span></span>
<span data-ttu-id="8b5d8-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5d8-158">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5d8-159">입력</span><span class="sxs-lookup"><span data-stu-id="8b5d8-159">INPUTS</span></span>

### <span data-ttu-id="8b5d8-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8b5d8-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8b5d8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8b5d8-161">System.String</span></span>

## <span data-ttu-id="8b5d8-162">출력</span><span class="sxs-lookup"><span data-stu-id="8b5d8-162">OUTPUTS</span></span>

### <span data-ttu-id="8b5d8-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8b5d8-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="8b5d8-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b5d8-164">NOTES</span></span>
* <span data-ttu-id="8b5d8-165">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="8b5d8-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8b5d8-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b5d8-166">RELATED LINKS</span></span>

[<span data-ttu-id="8b5d8-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8b5d8-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="8b5d8-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8b5d8-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


