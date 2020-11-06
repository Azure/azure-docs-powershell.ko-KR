---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ae640ffb0f595419bba57ff92d7789692af55d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527668"
---
# <span data-ttu-id="3f8e1-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="3f8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8e1-103">Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f8e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f8e1-104">SYNTAX</span></span>

### <span data-ttu-id="3f8e1-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f8e1-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f8e1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3f8e1-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f8e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3f8e1-107">DESCRIPTION</span></span>
<span data-ttu-id="3f8e1-108">**AzureRmDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="3f8e1-109">이미 존재 하는 파이프라인의 이름을 지정 하는 경우 cmdlet에서 파이프라인을 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="3f8e1-110">*Force* 매개 변수를 지정 하면 cmdlet이 확인 없이 기존 파이프라인을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="3f8e1-111">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="3f8e1-112">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-112">Create a data factory.</span></span> 
- <span data-ttu-id="3f8e1-113">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-113">Create linked services.</span></span> 
- <span data-ttu-id="3f8e1-114">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-114">Create datasets.</span></span> 
- <span data-ttu-id="3f8e1-115">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-115">Create a pipeline.</span></span>

<span data-ttu-id="3f8e1-116">이름이 같은 파이프라인이 데이터 팩터리에 이미 있는 경우이 cmdlet은 기존 파이프라인을 새 파이프라인으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="3f8e1-117">기존 파이프라인을 덮어쓰려고 한다는 것을 확인 한 경우 파이프라인 정의도 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="3f8e1-118">예제의</span><span class="sxs-lookup"><span data-stu-id="3f8e1-118">EXAMPLES</span></span>

### <span data-ttu-id="3f8e1-119">예제 1: 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="3f8e1-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="3f8e1-120">이 명령은 ADF 라는 data factory에 DPWikisample 이라는 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="3f8e1-121">명령은 파일의 DPWikisample.js정보에 파이프라인을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="3f8e1-122">이 파일에는 파이프라인의 복사본 활동 및 HDInsight 활동과 같은 작업에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="3f8e1-123">변수</span><span class="sxs-lookup"><span data-stu-id="3f8e1-123">PARAMETERS</span></span>

### <span data-ttu-id="3f8e1-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f8e1-124">-DataFactory</span></span>
<span data-ttu-id="3f8e1-125">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3f8e1-126">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f8e1-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3f8e1-127">-DataFactoryName</span></span>
<span data-ttu-id="3f8e1-128">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3f8e1-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f8e1-130">-파일</span><span class="sxs-lookup"><span data-stu-id="3f8e1-130">-File</span></span>
<span data-ttu-id="3f8e1-131">파이프라인에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="3f8e1-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3f8e1-132">-Force</span></span>
<span data-ttu-id="3f8e1-133">이 cmdlet이 확인을 묻지 않고 기존 파이프라인을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-133">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3f8e1-134">-이름</span><span class="sxs-lookup"><span data-stu-id="3f8e1-134">-Name</span></span>
<span data-ttu-id="3f8e1-135">만들 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-135">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="3f8e1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8e1-136">-ResourceGroupName</span></span>
<span data-ttu-id="3f8e1-137">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3f8e1-138">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-138">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f8e1-139">-확인</span><span class="sxs-lookup"><span data-stu-id="3f8e1-139">-Confirm</span></span>
<span data-ttu-id="3f8e1-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f8e1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f8e1-141">-WhatIf</span></span>
<span data-ttu-id="3f8e1-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f8e1-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f8e1-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8e1-144">-DefaultProfile</span></span>
<span data-ttu-id="3f8e1-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f8e1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8e1-146">CommonParameters</span></span>
<span data-ttu-id="3f8e1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f8e1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8e1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8e1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8e1-149">입력</span><span class="sxs-lookup"><span data-stu-id="3f8e1-149">INPUTS</span></span>

## <span data-ttu-id="3f8e1-150">출력</span><span class="sxs-lookup"><span data-stu-id="3f8e1-150">OUTPUTS</span></span>

### <span data-ttu-id="3f8e1-151">WindowsAzure. 유틸리티. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-151">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="3f8e1-152">상속자</span><span class="sxs-lookup"><span data-stu-id="3f8e1-152">NOTES</span></span>
* <span data-ttu-id="3f8e1-153">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="3f8e1-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3f8e1-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f8e1-154">RELATED LINKS</span></span>

[<span data-ttu-id="3f8e1-155">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-155">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3f8e1-156">제거-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3f8e1-157">이력서-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3f8e1-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3f8e1-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="3f8e1-159">일시 중단-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f8e1-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


