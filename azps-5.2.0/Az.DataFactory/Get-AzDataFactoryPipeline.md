---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354549"
---
# <span data-ttu-id="f6696-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="f6696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6696-102">SYNOPSIS</span></span>
<span data-ttu-id="f6696-103">Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="f6696-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6696-104">SYNTAX</span></span>

### <span data-ttu-id="f6696-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6696-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6696-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f6696-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6696-107">설명</span><span class="sxs-lookup"><span data-stu-id="f6696-107">DESCRIPTION</span></span>
<span data-ttu-id="f6696-108">**Get-AzDataFactoryPipeline** cmdlet은 Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="f6696-109">파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="f6696-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="f6696-111">예제</span><span class="sxs-lookup"><span data-stu-id="f6696-111">EXAMPLES</span></span>

### <span data-ttu-id="f6696-112">예제 1: 모든 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f6696-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="f6696-113">이 명령은 WikiADF라는 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="f6696-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="f6696-115">두 번째 개체는 **DataFactory 개체를** 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="f6696-116">예제 2: 특정 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f6696-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="f6696-117">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="f6696-118">이 명령은 파이프라인 연산자를 사용하여 Format-List cmdlet에 해당 정보를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6696-119">이 cmdlet은 결과 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="f6696-120">자세한 내용은 `Get-Help Format-List` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="f6696-121">예제 3: 특정 파이프라인에 대한 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="f6696-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="f6696-122">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 **속성** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="f6696-123">예제 4: 특정 파이프라인에 대한 활동 보기</span><span class="sxs-lookup"><span data-stu-id="f6696-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="f6696-124">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="f6696-125">예제 5: 특정 파이프라인에 대한 런타임 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="f6696-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="f6696-126">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 **RuntimeInfo** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="f6696-127">예제 6: 첫 번째 활동에 대한 입력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="f6696-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="f6696-128">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 찍은 다음 표준 점 표시를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="f6696-129">이 명령은 **Format-List를** 사용하여 **작업** 배열의 첫 번째 요소에 대한 Inputs 속성을 표시됩니다. </span><span class="sxs-lookup"><span data-stu-id="f6696-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="f6696-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6696-130">PARAMETERS</span></span>

### <span data-ttu-id="f6696-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f6696-131">-DataFactory</span></span>
<span data-ttu-id="f6696-132">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f6696-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f6696-133">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6696-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f6696-134">-DataFactoryName</span></span>
<span data-ttu-id="f6696-135">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f6696-136">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6696-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6696-137">-DefaultProfile</span></span>
<span data-ttu-id="f6696-138">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f6696-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6696-139">-Name</span><span class="sxs-lookup"><span data-stu-id="f6696-139">-Name</span></span>
<span data-ttu-id="f6696-140">정보를 얻을 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="f6696-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6696-141">-ResourceGroupName</span></span>
<span data-ttu-id="f6696-142">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f6696-143">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6696-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6696-144">CommonParameters</span></span>
<span data-ttu-id="f6696-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6696-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6696-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6696-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6696-147">입력</span><span class="sxs-lookup"><span data-stu-id="f6696-147">INPUTS</span></span>

### <span data-ttu-id="f6696-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f6696-148">System.String</span></span>

### <span data-ttu-id="f6696-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f6696-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f6696-150">출력</span><span class="sxs-lookup"><span data-stu-id="f6696-150">OUTPUTS</span></span>

### <span data-ttu-id="f6696-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="f6696-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6696-152">NOTES</span></span>
* <span data-ttu-id="f6696-153">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="f6696-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f6696-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6696-154">RELATED LINKS</span></span>

[<span data-ttu-id="f6696-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="f6696-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="f6696-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="f6696-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f6696-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f6696-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6696-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


