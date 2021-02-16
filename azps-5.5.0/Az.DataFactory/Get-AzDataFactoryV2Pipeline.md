---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188625"
---
# <span data-ttu-id="82516-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82516-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="82516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82516-102">SYNOPSIS</span></span>
<span data-ttu-id="82516-103">Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="82516-104">구문</span><span class="sxs-lookup"><span data-stu-id="82516-104">SYNTAX</span></span>

### <span data-ttu-id="82516-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="82516-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82516-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82516-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82516-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82516-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82516-108">설명</span><span class="sxs-lookup"><span data-stu-id="82516-108">DESCRIPTION</span></span>
<span data-ttu-id="82516-109">이 Get-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="82516-110">파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="82516-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="82516-112">예제</span><span class="sxs-lookup"><span data-stu-id="82516-112">EXAMPLES</span></span>

### <span data-ttu-id="82516-113">예제 1: 모든 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="82516-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="82516-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="82516-115">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="82516-116">두 번째 개체는 DataFactory 개체를 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="82516-117">예제 2: 특정 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="82516-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="82516-118">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="82516-119">이 명령은 파이프라인 연산자를 사용하여 Format-List cmdlet에 해당 정보를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="82516-120">이 Windows PowerShell 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="82516-121">자세한 내용은 서식 Get-Help 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="82516-122">예제 3: 특정 파이프라인에 대한 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="82516-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="82516-123">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 활동 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="82516-124">예제 4: 첫 번째 활동에 대한 입력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="82516-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="82516-125">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 활동 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="82516-126">명령은 Format-List cmdlet을 사용하여 Activities 배열의 첫 번째 요소의 Inputs 속성을 Format-List 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82516-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="82516-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82516-127">PARAMETERS</span></span>

### <span data-ttu-id="82516-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="82516-128">-DataFactory</span></span>
<span data-ttu-id="82516-129">PSDataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="82516-130">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82516-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82516-131">-DataFactoryName</span></span>
<span data-ttu-id="82516-132">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="82516-133">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82516-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82516-134">-DefaultProfile</span></span>
<span data-ttu-id="82516-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82516-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82516-136">-Name</span><span class="sxs-lookup"><span data-stu-id="82516-136">-Name</span></span>
<span data-ttu-id="82516-137">정보를 얻을 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="82516-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82516-138">-ResourceGroupName</span></span>
<span data-ttu-id="82516-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="82516-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82516-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82516-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82516-141">-ResourceId</span></span>
<span data-ttu-id="82516-142">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82516-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="82516-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82516-143">CommonParameters</span></span>
<span data-ttu-id="82516-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82516-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82516-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82516-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82516-146">입력</span><span class="sxs-lookup"><span data-stu-id="82516-146">INPUTS</span></span>

### <span data-ttu-id="82516-147">System.String</span><span class="sxs-lookup"><span data-stu-id="82516-147">System.String</span></span>

### <span data-ttu-id="82516-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="82516-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="82516-149">출력</span><span class="sxs-lookup"><span data-stu-id="82516-149">OUTPUTS</span></span>

### <span data-ttu-id="82516-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="82516-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="82516-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82516-151">NOTES</span></span>
<span data-ttu-id="82516-152">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="82516-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="82516-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82516-153">RELATED LINKS</span></span>

[<span data-ttu-id="82516-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82516-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="82516-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82516-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="82516-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82516-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
