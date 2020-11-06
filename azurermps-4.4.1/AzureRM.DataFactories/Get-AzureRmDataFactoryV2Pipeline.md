---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e0abd64298d74c52f2081e6d36f42b1ad2dee913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527683"
---
# <span data-ttu-id="d3c4d-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c4d-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="d3c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c4d-103">Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3c4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3c4d-104">SYNTAX</span></span>

### <span data-ttu-id="d3c4d-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3c4d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c4d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3c4d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3c4d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d3c4d-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c4d-108">Get-AzureRmDataFactoryV2Pipeline cmdlet은 Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="d3c4d-109">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="d3c4d-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="d3c4d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d3c4d-111">EXAMPLES</span></span>

### <span data-ttu-id="d3c4d-112">예제 1: 모든 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3c4d-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="d3c4d-113">이 명령은 WikiADF 이라는 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="d3c4d-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="d3c4d-115">두 번째는 DataFactory 개체를 매개 변수로 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="d3c4d-116">예제 2: 특정 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3c4d-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="d3c4d-117">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d3c4d-118">이 명령은 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 해당 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3c4d-119">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d3c4d-120">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="d3c4d-121">예제 3: 특정 파이프라인의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3c4d-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="d3c4d-122">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="d3c4d-123">예제 6: 첫 번째 활동의 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3c4d-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="d3c4d-124">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="d3c4d-125">이 명령은 Format-List cmdlet을 사용 하 여 활동 배열의 첫 번째 요소의 입력 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="d3c4d-126">변수</span><span class="sxs-lookup"><span data-stu-id="d3c4d-126">PARAMETERS</span></span>

### <span data-ttu-id="d3c4d-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3c4d-127">-DataFactory</span></span>
<span data-ttu-id="d3c4d-128">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="d3c4d-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3c4d-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3c4d-130">-DataFactoryName</span></span>
<span data-ttu-id="d3c4d-131">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d3c4d-132">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3c4d-133">-이름</span><span class="sxs-lookup"><span data-stu-id="d3c4d-133">-Name</span></span>
<span data-ttu-id="d3c4d-134">정보를 가져올 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="d3c4d-136">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d3c4d-137">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3c4d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c4d-138">-DefaultProfile</span></span>
<span data-ttu-id="d3c4d-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c4d-140">CommonParameters</span></span>
<span data-ttu-id="d3c4d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c4d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c4d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c4d-143">입력</span><span class="sxs-lookup"><span data-stu-id="d3c4d-143">INPUTS</span></span>

### <span data-ttu-id="d3c4d-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3c4d-144">System.String</span></span>
<span data-ttu-id="d3c4d-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3c4d-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d3c4d-146">출력</span><span class="sxs-lookup"><span data-stu-id="d3c4d-146">OUTPUTS</span></span>

### <span data-ttu-id="d3c4d-147">DataFactoryV2 ' 1 [[Microsoft Azure. PSPipeline, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d3c4d-148">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="d3c4d-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="d3c4d-149">상속자</span><span class="sxs-lookup"><span data-stu-id="d3c4d-149">NOTES</span></span>
<span data-ttu-id="d3c4d-150">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d3c4d-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3c4d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3c4d-151">RELATED LINKS</span></span>

[<span data-ttu-id="d3c4d-152">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c4d-152">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d3c4d-153">제거-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c4d-153">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d3c4d-154">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="d3c4d-154">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
