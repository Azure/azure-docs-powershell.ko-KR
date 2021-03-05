---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b059e48eda6367459bd90bd7ccdf93ea14387ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964923"
---
# <span data-ttu-id="c6341-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c6341-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c6341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6341-102">SYNOPSIS</span></span>
<span data-ttu-id="c6341-103">Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="c6341-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6341-104">SYNTAX</span></span>

### <span data-ttu-id="c6341-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c6341-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6341-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6341-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6341-107">설명</span><span class="sxs-lookup"><span data-stu-id="c6341-107">DESCRIPTION</span></span>
<span data-ttu-id="c6341-108">Set-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="c6341-109">이미 있는 파이프라인의 이름을 지정하면 cmdlet에서 파이프라인을 바꾸기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="c6341-110">Force 매개 변수를 지정하는 경우 cmdlet은 확인 없이 기존 파이프라인을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="c6341-111">다음 순서로 이러한 작업을 수행합니다. -- 데이터 팩터리 만들기.</span><span class="sxs-lookup"><span data-stu-id="c6341-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="c6341-112">-- 연결된 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-112">-- Create linked services.</span></span>
<span data-ttu-id="c6341-113">-- 데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-113">-- Create datasets.</span></span>
<span data-ttu-id="c6341-114">-- 파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-114">-- Create a pipeline.</span></span>
<span data-ttu-id="c6341-115">동일한 이름이 있는 파이프라인이 데이터 팩터리에 이미 있는 경우 이 cmdlet은 새 파이프라인을 사용하여 기존 파이프라인을 덮어써야 하는지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="c6341-116">기존 파이프라인을 덮어 우는 것이 확인되면 파이프라인 정의도 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="c6341-117">예제</span><span class="sxs-lookup"><span data-stu-id="c6341-117">EXAMPLES</span></span>

### <span data-ttu-id="c6341-118">예제 1: 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="c6341-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="c6341-119">이 명령은 ADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="c6341-120">명령은 파일에서 파이프라인을 DPWikisample.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="c6341-121">이 파일에는 파이프라인의 복사 작업 및 HDInsight 작업과 같은 활동에 대한 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="c6341-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6341-122">PARAMETERS</span></span>

### <span data-ttu-id="c6341-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6341-123">-DataFactoryName</span></span>
<span data-ttu-id="c6341-124">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c6341-125">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6341-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6341-126">-DefaultProfile</span></span>
<span data-ttu-id="c6341-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6341-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c6341-128">-DefinitionFile</span></span>
<span data-ttu-id="c6341-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-129">The JSON file path.</span></span>

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

### <span data-ttu-id="c6341-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c6341-130">-Force</span></span>
<span data-ttu-id="c6341-131">확인을 요청하지 않고 이 cmdlet이 기존 파이프라인을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c6341-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c6341-132">-Name</span></span>
<span data-ttu-id="c6341-133">만들 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6341-134">-ResourceGroupName</span></span>
<span data-ttu-id="c6341-135">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6341-136">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6341-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6341-137">-ResourceId</span></span>
<span data-ttu-id="c6341-138">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c6341-139">-확인</span><span class="sxs-lookup"><span data-stu-id="c6341-139">-Confirm</span></span>
<span data-ttu-id="c6341-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6341-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6341-141">-WhatIf</span></span>
<span data-ttu-id="c6341-142">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c6341-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6341-143">CommonParameters</span></span>
<span data-ttu-id="c6341-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6341-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6341-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c6341-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6341-146">입력</span><span class="sxs-lookup"><span data-stu-id="c6341-146">INPUTS</span></span>

### <span data-ttu-id="c6341-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c6341-147">System.String</span></span>

## <span data-ttu-id="c6341-148">출력</span><span class="sxs-lookup"><span data-stu-id="c6341-148">OUTPUTS</span></span>

### <span data-ttu-id="c6341-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c6341-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c6341-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6341-150">NOTES</span></span>
<span data-ttu-id="c6341-151">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="c6341-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6341-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6341-152">RELATED LINKS</span></span>

[<span data-ttu-id="c6341-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c6341-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c6341-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c6341-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c6341-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c6341-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
