---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: 6583da48324078d321630f23097ab3a00d8338d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701138"
---
# <span data-ttu-id="61a64-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="61a64-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="61a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a64-102">SYNOPSIS</span></span>
<span data-ttu-id="61a64-103">Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="61a64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61a64-104">SYNTAX</span></span>

### <span data-ttu-id="61a64-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="61a64-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61a64-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="61a64-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a64-107">설명은</span><span class="sxs-lookup"><span data-stu-id="61a64-107">DESCRIPTION</span></span>
<span data-ttu-id="61a64-108">**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="61a64-109">이미 존재 하는 파이프라인의 이름을 지정 하는 경우 cmdlet에서 파이프라인을 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="61a64-110">*Force* 매개 변수를 지정 하면 cmdlet이 확인 없이 기존 파이프라인을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="61a64-111">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="61a64-112">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-112">Create a data factory.</span></span> 
- <span data-ttu-id="61a64-113">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-113">Create linked services.</span></span> 
- <span data-ttu-id="61a64-114">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-114">Create datasets.</span></span> 
- <span data-ttu-id="61a64-115">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-115">Create a pipeline.</span></span>
<span data-ttu-id="61a64-116">이름이 같은 파이프라인이 데이터 팩터리에 이미 있는 경우이 cmdlet은 기존 파이프라인을 새 파이프라인으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="61a64-117">기존 파이프라인을 덮어쓰려고 한다는 것을 확인 한 경우 파이프라인 정의도 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="61a64-118">예제의</span><span class="sxs-lookup"><span data-stu-id="61a64-118">EXAMPLES</span></span>

### <span data-ttu-id="61a64-119">예제 1: 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="61a64-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="61a64-120">이 명령은 ADF 라는 data factory에 DPWikisample 이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="61a64-121">명령은 파일의 DPWikisample.js정보에 파이프라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="61a64-122">이 파일에는 파이프라인의 복사본 활동 및 HDInsight 활동과 같은 작업에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="61a64-123">변수</span><span class="sxs-lookup"><span data-stu-id="61a64-123">PARAMETERS</span></span>

### <span data-ttu-id="61a64-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="61a64-124">-DataFactory</span></span>
<span data-ttu-id="61a64-125">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="61a64-126">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61a64-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="61a64-127">-DataFactoryName</span></span>
<span data-ttu-id="61a64-128">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="61a64-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61a64-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a64-130">-DefaultProfile</span></span>
<span data-ttu-id="61a64-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="61a64-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61a64-132">-파일</span><span class="sxs-lookup"><span data-stu-id="61a64-132">-File</span></span>
<span data-ttu-id="61a64-133">파이프라인에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="61a64-134">-Force</span><span class="sxs-lookup"><span data-stu-id="61a64-134">-Force</span></span>
<span data-ttu-id="61a64-135">이 cmdlet이 확인을 묻지 않고 기존 파이프라인을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="61a64-136">-이름</span><span class="sxs-lookup"><span data-stu-id="61a64-136">-Name</span></span>
<span data-ttu-id="61a64-137">만들 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="61a64-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a64-138">-ResourceGroupName</span></span>
<span data-ttu-id="61a64-139">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61a64-140">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="61a64-141">-확인</span><span class="sxs-lookup"><span data-stu-id="61a64-141">-Confirm</span></span>
<span data-ttu-id="61a64-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a64-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a64-143">-WhatIf</span></span>
<span data-ttu-id="61a64-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a64-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a64-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a64-146">CommonParameters</span></span>
<span data-ttu-id="61a64-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a64-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a64-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a64-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a64-149">입력</span><span class="sxs-lookup"><span data-stu-id="61a64-149">INPUTS</span></span>

### <span data-ttu-id="61a64-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61a64-150">System.String</span></span>

### <span data-ttu-id="61a64-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="61a64-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="61a64-152">출력</span><span class="sxs-lookup"><span data-stu-id="61a64-152">OUTPUTS</span></span>

### <span data-ttu-id="61a64-153">DataFactories. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="61a64-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="61a64-154">상속자</span><span class="sxs-lookup"><span data-stu-id="61a64-154">NOTES</span></span>
* <span data-ttu-id="61a64-155">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="61a64-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61a64-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61a64-156">RELATED LINKS</span></span>

[<span data-ttu-id="61a64-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="61a64-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="61a64-158">제거-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="61a64-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="61a64-159">이력서-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="61a64-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="61a64-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="61a64-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="61a64-161">일시 중단-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="61a64-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


