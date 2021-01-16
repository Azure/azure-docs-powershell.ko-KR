---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333650"
---
# <span data-ttu-id="19787-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="19787-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="19787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19787-102">SYNOPSIS</span></span>
<span data-ttu-id="19787-103">Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="19787-104">구문</span><span class="sxs-lookup"><span data-stu-id="19787-104">SYNTAX</span></span>

### <span data-ttu-id="19787-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="19787-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19787-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="19787-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19787-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19787-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19787-108">설명</span><span class="sxs-lookup"><span data-stu-id="19787-108">DESCRIPTION</span></span>
<span data-ttu-id="19787-109">이 Get-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="19787-110">파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="19787-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="19787-112">예제</span><span class="sxs-lookup"><span data-stu-id="19787-112">EXAMPLES</span></span>

### <span data-ttu-id="19787-113">예제 1: 모든 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="19787-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="19787-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="19787-115">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="19787-116">두 번째 개체는 DataFactory 개체를 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="19787-117">예제 2: 특정 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="19787-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="19787-118">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="19787-119">이 명령은 파이프라인 연산자를 사용하여 Format-List cmdlet에 해당 정보를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19787-120">이 Windows PowerShell 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="19787-121">자세한 내용은 서식 Get-Help 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="19787-122">예제 3: 특정 파이프라인에 대한 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="19787-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="19787-123">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 활동 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="19787-124">예제 4: 첫 번째 활동에 대한 입력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="19787-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="19787-125">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 활동 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="19787-126">명령은 Format-List cmdlet을 사용하여 Activities 배열의 첫 번째 요소의 Inputs 속성을 Format-List 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19787-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="19787-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19787-127">PARAMETERS</span></span>

### <span data-ttu-id="19787-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="19787-128">-DataFactory</span></span>
<span data-ttu-id="19787-129">PSDataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="19787-130">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="19787-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="19787-131">-DataFactoryName</span></span>
<span data-ttu-id="19787-132">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="19787-133">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="19787-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19787-134">-DefaultProfile</span></span>
<span data-ttu-id="19787-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19787-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19787-136">-Name</span><span class="sxs-lookup"><span data-stu-id="19787-136">-Name</span></span>
<span data-ttu-id="19787-137">정보를 얻을 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="19787-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19787-138">-ResourceGroupName</span></span>
<span data-ttu-id="19787-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="19787-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19787-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="19787-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19787-141">-ResourceId</span></span>
<span data-ttu-id="19787-142">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="19787-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="19787-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19787-143">CommonParameters</span></span>
<span data-ttu-id="19787-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19787-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19787-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="19787-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19787-146">입력</span><span class="sxs-lookup"><span data-stu-id="19787-146">INPUTS</span></span>

### <span data-ttu-id="19787-147">System.String</span><span class="sxs-lookup"><span data-stu-id="19787-147">System.String</span></span>

### <span data-ttu-id="19787-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="19787-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="19787-149">출력</span><span class="sxs-lookup"><span data-stu-id="19787-149">OUTPUTS</span></span>

### <span data-ttu-id="19787-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="19787-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="19787-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19787-151">NOTES</span></span>
<span data-ttu-id="19787-152">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="19787-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="19787-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19787-153">RELATED LINKS</span></span>

[<span data-ttu-id="19787-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="19787-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="19787-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="19787-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="19787-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="19787-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
