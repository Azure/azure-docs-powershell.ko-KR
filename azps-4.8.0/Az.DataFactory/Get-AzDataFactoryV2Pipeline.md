---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214180"
---
# <span data-ttu-id="0e833-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e833-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0e833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e833-102">SYNOPSIS</span></span>
<span data-ttu-id="0e833-103">Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="0e833-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e833-104">SYNTAX</span></span>

### <span data-ttu-id="0e833-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e833-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e833-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0e833-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e833-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e833-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e833-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0e833-108">DESCRIPTION</span></span>
<span data-ttu-id="0e833-109">Get-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="0e833-110">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="0e833-111">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="0e833-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0e833-112">EXAMPLES</span></span>

### <span data-ttu-id="0e833-113">예제 1: 모든 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e833-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="0e833-114">이 명령은 WikiADF 이라는 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="0e833-115">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="0e833-116">두 번째는 DataFactory 개체를 매개 변수로 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="0e833-117">예제 2: 특정 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e833-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0e833-118">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="0e833-119">이 명령은 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 해당 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0e833-120">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0e833-121">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="0e833-122">예제 3: 특정 파이프라인의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e833-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="0e833-123">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="0e833-124">예제 4: 첫 번째 활동의 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e833-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="0e833-125">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="0e833-126">이 명령은 Format-List cmdlet을 사용 하 여 활동 배열의 첫 번째 요소의 입력 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="0e833-127">변수</span><span class="sxs-lookup"><span data-stu-id="0e833-127">PARAMETERS</span></span>

### <span data-ttu-id="0e833-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e833-128">-DataFactory</span></span>
<span data-ttu-id="0e833-129">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="0e833-130">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e833-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0e833-131">-DataFactoryName</span></span>
<span data-ttu-id="0e833-132">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0e833-133">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e833-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e833-134">-DefaultProfile</span></span>
<span data-ttu-id="0e833-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e833-136">-이름</span><span class="sxs-lookup"><span data-stu-id="0e833-136">-Name</span></span>
<span data-ttu-id="0e833-137">정보를 가져올 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e833-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e833-138">-ResourceGroupName</span></span>
<span data-ttu-id="0e833-139">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0e833-140">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e833-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e833-141">-ResourceId</span></span>
<span data-ttu-id="0e833-142">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0e833-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e833-143">CommonParameters</span></span>
<span data-ttu-id="0e833-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e833-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e833-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e833-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e833-146">입력</span><span class="sxs-lookup"><span data-stu-id="0e833-146">INPUTS</span></span>

### <span data-ttu-id="0e833-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e833-147">System.String</span></span>

### <span data-ttu-id="0e833-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0e833-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0e833-149">출력</span><span class="sxs-lookup"><span data-stu-id="0e833-149">OUTPUTS</span></span>

### <span data-ttu-id="0e833-150">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="0e833-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="0e833-151">상속자</span><span class="sxs-lookup"><span data-stu-id="0e833-151">NOTES</span></span>
<span data-ttu-id="0e833-152">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="0e833-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0e833-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e833-153">RELATED LINKS</span></span>

[<span data-ttu-id="0e833-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e833-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0e833-155">제거-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e833-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0e833-156">AzDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="0e833-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
