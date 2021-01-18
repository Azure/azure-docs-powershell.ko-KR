---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493535"
---
# <span data-ttu-id="bab3c-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="bab3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab3c-102">SYNOPSIS</span></span>
<span data-ttu-id="bab3c-103">Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="bab3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="bab3c-104">SYNTAX</span></span>

### <span data-ttu-id="bab3c-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bab3c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bab3c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bab3c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab3c-107">설명</span><span class="sxs-lookup"><span data-stu-id="bab3c-107">DESCRIPTION</span></span>
<span data-ttu-id="bab3c-108">**New-AzDataFactoryPipeline** cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="bab3c-109">이미 있는 파이프라인의 이름을 지정하는 경우 cmdlet은 파이프라인을 바꾸기 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="bab3c-110">Force 매개 *변수를 지정하면* cmdlet이 확인 없이 기존 파이프라인을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="bab3c-111">다음 순서로 이러한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="bab3c-112">데이터 팩터리 만들기</span><span class="sxs-lookup"><span data-stu-id="bab3c-112">Create a data factory.</span></span> 
- <span data-ttu-id="bab3c-113">연결된 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-113">Create linked services.</span></span> 
- <span data-ttu-id="bab3c-114">데이터 세트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-114">Create datasets.</span></span> 
- <span data-ttu-id="bab3c-115">파이프라인을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-115">Create a pipeline.</span></span>
<span data-ttu-id="bab3c-116">동일한 이름의 파이프라인이 데이터 팩터리에 이미 있는 경우 이 cmdlet은 새 파이프라인으로 기존 파이프라인을 덮어써야 하는지 여부를 확인하라는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="bab3c-117">기존 파이프라인을 덮어들이는 것이 확인되면 파이프라인 정의도 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="bab3c-118">예제</span><span class="sxs-lookup"><span data-stu-id="bab3c-118">EXAMPLES</span></span>

### <span data-ttu-id="bab3c-119">예제 1: 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="bab3c-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="bab3c-120">이 명령은 ADF라는 데이터 팩터리에 DPWikisample이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="bab3c-121">이 명령은 파이프라인의 파일 DPWikisample.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="bab3c-122">이 파일에는 파이프라인의 복사 작업 및 HDInsight 작업과 같은 활동에 대한 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="bab3c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bab3c-123">PARAMETERS</span></span>

### <span data-ttu-id="bab3c-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bab3c-124">-DataFactory</span></span>
<span data-ttu-id="bab3c-125">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="bab3c-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bab3c-126">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bab3c-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bab3c-127">-DataFactoryName</span></span>
<span data-ttu-id="bab3c-128">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bab3c-129">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bab3c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab3c-130">-DefaultProfile</span></span>
<span data-ttu-id="bab3c-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bab3c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bab3c-132">-File</span><span class="sxs-lookup"><span data-stu-id="bab3c-132">-File</span></span>
<span data-ttu-id="bab3c-133">파이프라인에 대한 설명이 포함된 JSON(JavaScript Object Notation) 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="bab3c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="bab3c-134">-Force</span></span>
<span data-ttu-id="bab3c-135">확인 메시지를 표시하지 않고 이 cmdlet이 기존 파이프라인을 대체하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bab3c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="bab3c-136">-Name</span></span>
<span data-ttu-id="bab3c-137">만들 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab3c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab3c-138">-ResourceGroupName</span></span>
<span data-ttu-id="bab3c-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bab3c-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bab3c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bab3c-141">-Confirm</span></span>
<span data-ttu-id="bab3c-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bab3c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab3c-143">-WhatIf</span></span>
<span data-ttu-id="bab3c-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bab3c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab3c-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bab3c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab3c-146">CommonParameters</span></span>
<span data-ttu-id="bab3c-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bab3c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab3c-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bab3c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab3c-149">입력</span><span class="sxs-lookup"><span data-stu-id="bab3c-149">INPUTS</span></span>

### <span data-ttu-id="bab3c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="bab3c-150">System.String</span></span>

### <span data-ttu-id="bab3c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bab3c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="bab3c-152">출력</span><span class="sxs-lookup"><span data-stu-id="bab3c-152">OUTPUTS</span></span>

### <span data-ttu-id="bab3c-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="bab3c-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bab3c-154">NOTES</span></span>
* <span data-ttu-id="bab3c-155">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="bab3c-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bab3c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bab3c-156">RELATED LINKS</span></span>

[<span data-ttu-id="bab3c-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="bab3c-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="bab3c-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="bab3c-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="bab3c-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="bab3c-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bab3c-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


