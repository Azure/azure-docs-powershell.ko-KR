---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
ms.openlocfilehash: f4944e8413c686f7d6970050db19ddc69cc351d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530793"
---
# <span data-ttu-id="11718-101">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11718-101">New-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="11718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11718-102">SYNOPSIS</span></span>
<span data-ttu-id="11718-103">Data Factory에서 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11718-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11718-104">SYNTAX</span></span>

### <span data-ttu-id="11718-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="11718-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11718-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="11718-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11718-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11718-107">DESCRIPTION</span></span>
<span data-ttu-id="11718-108">**AzureRmDataFactoryDataset** Cmdlet은 Azure Data Factory에서 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-108">The **New-AzureRmDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="11718-109">이미 존재 하는 데이터 집합의 이름을 지정 하면이 cmdlet이 데이터 집합을 바꾸기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="11718-110">*Force* 매개 변수를 지정 하면 cmdlet은 확인 없이 기존 데이터 집합을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="11718-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="11718-111">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="11718-112">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-112">Create a data factory.</span></span> 
- <span data-ttu-id="11718-113">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-113">Create linked services.</span></span> 
- <span data-ttu-id="11718-114">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-114">Create datasets.</span></span> 
- <span data-ttu-id="11718-115">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-115">Create a pipeline.</span></span>

<span data-ttu-id="11718-116">데이터 팩터리에 동일한 이름을 가진 데이터 집합이 이미 있는 경우이 cmdlet은 기존 데이터 집합을 새 데이터 집합으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="11718-117">기존 데이터 집합을 덮어쓰려고 한다는 것을 확인 하면 데이터 집합 정의도 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11718-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="11718-118">예제의</span><span class="sxs-lookup"><span data-stu-id="11718-118">EXAMPLES</span></span>

### <span data-ttu-id="11718-119">예제 1: 데이터 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="11718-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="11718-120">이 명령은 WikiADF 이라는 data factory에 DA_WikipediaClickEvents 이라는 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="11718-121">명령은 파일의 DAWikipediaClickEvents.js정보를 기준으로 데이터 집합을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="11718-122">예제 2: 새 데이터 집합의 사용 가능성 보기</span><span class="sxs-lookup"><span data-stu-id="11718-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="11718-123">첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="11718-124">두 번째 명령은 표준 점 표기법을 사용 하 여 데이터 집합의 Availability 속성에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="11718-125">예제 3: 새 데이터 집합에 대 한 보기 위치</span><span class="sxs-lookup"><span data-stu-id="11718-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="11718-126">첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="11718-127">두 번째 명령은 데이터 집합의 Location 속성에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="11718-128">예제 4: 새 데이터 집합에 대 한 유효성 검사 규칙 보기</span><span class="sxs-lookup"><span data-stu-id="11718-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="11718-129">첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>

<span data-ttu-id="11718-130">두 번째 명령은 데이터 집합에 대 한 유효성 검사 규칙에 대 한 세부 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="11718-131">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="11718-132">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="11718-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="11718-133">변수</span><span class="sxs-lookup"><span data-stu-id="11718-133">PARAMETERS</span></span>

### <span data-ttu-id="11718-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="11718-134">-DataFactory</span></span>
<span data-ttu-id="11718-135">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="11718-136">이 cmdlet은이 매개 변수에서 지정 하는 데이터 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="11718-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="11718-137">-DataFactoryName</span></span>
<span data-ttu-id="11718-138">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="11718-139">이 cmdlet은이 매개 변수에서 지정 하는 데이터 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="11718-140">-파일</span><span class="sxs-lookup"><span data-stu-id="11718-140">-File</span></span>
<span data-ttu-id="11718-141">데이터 집합에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-141">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="11718-142">-Force</span><span class="sxs-lookup"><span data-stu-id="11718-142">-Force</span></span>
<span data-ttu-id="11718-143">이 cmdlet이 기존 데이터 집합을 확인 메시지 없이 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11718-143">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="11718-144">-이름</span><span class="sxs-lookup"><span data-stu-id="11718-144">-Name</span></span>
<span data-ttu-id="11718-145">만들 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-145">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="11718-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11718-146">-ResourceGroupName</span></span>
<span data-ttu-id="11718-147">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-147">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="11718-148">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11718-148">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11718-149">-확인</span><span class="sxs-lookup"><span data-stu-id="11718-149">-Confirm</span></span>
<span data-ttu-id="11718-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11718-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11718-151">-WhatIf</span></span>
<span data-ttu-id="11718-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11718-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11718-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11718-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11718-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11718-154">-DefaultProfile</span></span>
<span data-ttu-id="11718-155">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11718-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11718-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11718-156">CommonParameters</span></span>
<span data-ttu-id="11718-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11718-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11718-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11718-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11718-159">입력</span><span class="sxs-lookup"><span data-stu-id="11718-159">INPUTS</span></span>

## <span data-ttu-id="11718-160">출력</span><span class="sxs-lookup"><span data-stu-id="11718-160">OUTPUTS</span></span>

### <span data-ttu-id="11718-161">Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="11718-161">Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="11718-162">상속자</span><span class="sxs-lookup"><span data-stu-id="11718-162">NOTES</span></span>
* <span data-ttu-id="11718-163">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="11718-163">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="11718-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11718-164">RELATED LINKS</span></span>

[<span data-ttu-id="11718-165">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11718-165">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="11718-166">제거-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="11718-166">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


