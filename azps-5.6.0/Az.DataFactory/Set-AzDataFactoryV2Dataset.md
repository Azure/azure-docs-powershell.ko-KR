---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006955"
---
# <span data-ttu-id="9e8a5-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9e8a5-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="9e8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8a5-103">Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="9e8a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e8a5-104">SYNTAX</span></span>

### <span data-ttu-id="9e8a5-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9e8a5-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e8a5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e8a5-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e8a5-107">설명</span><span class="sxs-lookup"><span data-stu-id="9e8a5-107">DESCRIPTION</span></span>
<span data-ttu-id="9e8a5-108">Set-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="9e8a5-109">이미 있는 데이터 세트의 이름을 지정하는 경우 이 cmdlet은 데이터 세트를 바꾸기 전에 확인을 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="9e8a5-110">Force 매개 변수를 지정하는 경우 cmdlet은 확인 없이 기존 데이터 세트를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="9e8a5-111">다음 순서로 이러한 작업을 수행합니다. -- 데이터 팩터리 만들기.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="9e8a5-112">-- 연결된 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-112">-- Create linked services.</span></span>
<span data-ttu-id="9e8a5-113">-- 데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-113">-- Create datasets.</span></span>
<span data-ttu-id="9e8a5-114">-- 파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-114">-- Create a pipeline.</span></span>
<span data-ttu-id="9e8a5-115">동일한 이름의 데이터 세트가 데이터 팩터리에 이미 있는 경우 이 cmdlet은 새 데이터 세트로 기존 데이터 세트를 덮어써야 하는지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="9e8a5-116">기존 데이터 세트를 덮어 우는 것이 확인되면 데이터 세트 정의도 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="9e8a5-117">예제</span><span class="sxs-lookup"><span data-stu-id="9e8a5-117">EXAMPLES</span></span>

### <span data-ttu-id="9e8a5-118">예제 1: 데이터 세트 만들기</span><span class="sxs-lookup"><span data-stu-id="9e8a5-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="9e8a5-119">이 명령은 WikiADF라는 DA_WikipediaClickEvents 팩터리에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="9e8a5-120">명령은 데이터 세트를 on 파일의 DAWikipediaClickEvents.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="9e8a5-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e8a5-121">PARAMETERS</span></span>

### <span data-ttu-id="9e8a5-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e8a5-122">-DataFactoryName</span></span>
<span data-ttu-id="9e8a5-123">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9e8a5-124">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e8a5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e8a5-125">-DefaultProfile</span></span>
<span data-ttu-id="9e8a5-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e8a5-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9e8a5-127">-DefinitionFile</span></span>
<span data-ttu-id="9e8a5-128">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8a5-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9e8a5-129">-Force</span></span>
<span data-ttu-id="9e8a5-130">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9e8a5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9e8a5-131">-Name</span></span>
<span data-ttu-id="9e8a5-132">만들 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8a5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e8a5-133">-ResourceGroupName</span></span>
<span data-ttu-id="9e8a5-134">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9e8a5-135">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e8a5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e8a5-136">-ResourceId</span></span>
<span data-ttu-id="9e8a5-137">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9e8a5-138">-확인</span><span class="sxs-lookup"><span data-stu-id="9e8a5-138">-Confirm</span></span>
<span data-ttu-id="9e8a5-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8a5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e8a5-140">-WhatIf</span></span>
<span data-ttu-id="9e8a5-141">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8a5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8a5-142">CommonParameters</span></span>
<span data-ttu-id="9e8a5-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8a5-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e8a5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8a5-145">입력</span><span class="sxs-lookup"><span data-stu-id="9e8a5-145">INPUTS</span></span>

### <span data-ttu-id="9e8a5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9e8a5-146">System.String</span></span>

## <span data-ttu-id="9e8a5-147">출력</span><span class="sxs-lookup"><span data-stu-id="9e8a5-147">OUTPUTS</span></span>

### <span data-ttu-id="9e8a5-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="9e8a5-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="9e8a5-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e8a5-149">NOTES</span></span>
<span data-ttu-id="9e8a5-150">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="9e8a5-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9e8a5-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e8a5-151">RELATED LINKS</span></span>

[<span data-ttu-id="9e8a5-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9e8a5-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="9e8a5-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9e8a5-153">Remove-AzDataFactoryV2Dataset</span></span>]()
