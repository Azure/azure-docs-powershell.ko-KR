---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 45a291a5b1ac7fe9474d85f61d656def1fb5c787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696964"
---
# <span data-ttu-id="e0172-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e0172-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e0172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0172-102">SYNOPSIS</span></span>
<span data-ttu-id="e0172-103">Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="e0172-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0172-104">SYNTAX</span></span>

### <span data-ttu-id="e0172-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0172-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0172-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0172-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0172-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e0172-107">DESCRIPTION</span></span>
<span data-ttu-id="e0172-108">Set-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="e0172-109">이미 존재 하는 파이프라인의 이름을 지정 하는 경우 cmdlet에서 파이프라인을 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="e0172-110">Force 매개 변수를 지정 하면 cmdlet이 확인 없이 기존 파이프라인을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="e0172-111">다음 순서 대로 이러한 작업을 수행 합니다.--data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e0172-112">--연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-112">-- Create linked services.</span></span>
<span data-ttu-id="e0172-113">--데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-113">-- Create datasets.</span></span>
<span data-ttu-id="e0172-114">--파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-114">-- Create a pipeline.</span></span>
<span data-ttu-id="e0172-115">이름이 같은 파이프라인이 데이터 팩터리에 이미 있는 경우이 cmdlet은 기존 파이프라인을 새 파이프라인으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="e0172-116">기존 파이프라인을 덮어쓰려고 한다는 것을 확인 한 경우 파이프라인 정의도 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="e0172-117">예제의</span><span class="sxs-lookup"><span data-stu-id="e0172-117">EXAMPLES</span></span>

### <span data-ttu-id="e0172-118">예제 1: 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="e0172-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="e0172-119">이 명령은 ADF 라는 data factory에 DPWikisample 이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="e0172-120">명령은 파일의 DPWikisample.js정보에 파이프라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="e0172-121">이 파일에는 파이프라인의 복사본 활동 및 HDInsight 활동과 같은 작업에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="e0172-122">변수</span><span class="sxs-lookup"><span data-stu-id="e0172-122">PARAMETERS</span></span>

### <span data-ttu-id="e0172-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e0172-123">-DataFactoryName</span></span>
<span data-ttu-id="e0172-124">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e0172-125">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0172-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0172-126">-DefaultProfile</span></span>
<span data-ttu-id="e0172-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0172-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e0172-128">-DefinitionFile</span></span>
<span data-ttu-id="e0172-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-129">The JSON file path.</span></span>

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

### <span data-ttu-id="e0172-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e0172-130">-Force</span></span>
<span data-ttu-id="e0172-131">이 cmdlet이 확인을 묻지 않고 기존 파이프라인을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e0172-132">-이름</span><span class="sxs-lookup"><span data-stu-id="e0172-132">-Name</span></span>
<span data-ttu-id="e0172-133">만들 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="e0172-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0172-134">-ResourceGroupName</span></span>
<span data-ttu-id="e0172-135">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e0172-136">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0172-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0172-137">-ResourceId</span></span>
<span data-ttu-id="e0172-138">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e0172-139">-확인</span><span class="sxs-lookup"><span data-stu-id="e0172-139">-Confirm</span></span>
<span data-ttu-id="e0172-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0172-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0172-141">-WhatIf</span></span>
<span data-ttu-id="e0172-142">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e0172-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0172-143">CommonParameters</span></span>
<span data-ttu-id="e0172-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0172-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0172-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0172-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0172-146">입력</span><span class="sxs-lookup"><span data-stu-id="e0172-146">INPUTS</span></span>

### <span data-ttu-id="e0172-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0172-147">System.String</span></span>

## <span data-ttu-id="e0172-148">출력</span><span class="sxs-lookup"><span data-stu-id="e0172-148">OUTPUTS</span></span>

### <span data-ttu-id="e0172-149">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="e0172-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e0172-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e0172-150">NOTES</span></span>
<span data-ttu-id="e0172-151">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="e0172-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e0172-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0172-152">RELATED LINKS</span></span>

[<span data-ttu-id="e0172-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e0172-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e0172-154">제거-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e0172-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e0172-155">AzDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="e0172-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
