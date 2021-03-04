---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975408"
---
# <span data-ttu-id="32453-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="32453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32453-102">SYNOPSIS</span></span>
<span data-ttu-id="32453-103">Azure Data Factory에서 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="32453-104">구문</span><span class="sxs-lookup"><span data-stu-id="32453-104">SYNTAX</span></span>

### <span data-ttu-id="32453-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="32453-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32453-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="32453-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32453-107">설명</span><span class="sxs-lookup"><span data-stu-id="32453-107">DESCRIPTION</span></span>
<span data-ttu-id="32453-108">**Get-AzDataFactoryPipeline** cmdlet은 Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="32453-109">파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="32453-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 파이프라인에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="32453-111">예제</span><span class="sxs-lookup"><span data-stu-id="32453-111">EXAMPLES</span></span>

### <span data-ttu-id="32453-112">예제 1: 모든 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="32453-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="32453-113">이 명령은 WikiADF라는 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="32453-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="32453-115">두 번째 개체는 **DataFactory 개체를** 매개 변수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="32453-116">예제 2: 특정 파이프라인에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="32453-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="32453-117">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="32453-118">명령은 파이프라인 연산자를 사용하여 해당 Format-List cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="32453-119">이 cmdlet은 결과를 서식 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="32453-120">자세한 내용은 `Get-Help Format-List` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="32453-121">예제 3: 특정 파이프라인에 대한 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="32453-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="32453-122">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음 표준 점표를 사용하여 해당 파이프라인과 연결된 **속성** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="32453-123">예제 4: 특정 파이프라인에 대한 활동 보기</span><span class="sxs-lookup"><span data-stu-id="32453-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="32453-124">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음, 표준 점표를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="32453-125">예제 5: 특정 파이프라인에 대한 런타임 정보 보기</span><span class="sxs-lookup"><span data-stu-id="32453-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="32453-126">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음 표준 점표를 사용하여 해당 파이프라인과 연결된 **RuntimeInfo** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="32453-127">예제 6: 첫 번째 활동에 대한 입력에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="32453-128">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음, 표준 점표를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32453-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="32453-129">명령은 **서식** 목록 을 사용하여 활동  배열의 첫 번째 요소의 **Inputs 속성을 표시합니다.**</span><span class="sxs-lookup"><span data-stu-id="32453-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="32453-130">매개 변수</span><span class="sxs-lookup"><span data-stu-id="32453-130">PARAMETERS</span></span>

### <span data-ttu-id="32453-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="32453-131">-DataFactory</span></span>
<span data-ttu-id="32453-132">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="32453-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="32453-133">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="32453-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="32453-134">-DataFactoryName</span></span>
<span data-ttu-id="32453-135">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="32453-136">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="32453-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32453-137">-DefaultProfile</span></span>
<span data-ttu-id="32453-138">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32453-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32453-139">-Name</span><span class="sxs-lookup"><span data-stu-id="32453-139">-Name</span></span>
<span data-ttu-id="32453-140">정보를 얻을 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="32453-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32453-141">-ResourceGroupName</span></span>
<span data-ttu-id="32453-142">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="32453-143">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="32453-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32453-144">CommonParameters</span></span>
<span data-ttu-id="32453-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32453-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32453-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32453-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32453-147">입력</span><span class="sxs-lookup"><span data-stu-id="32453-147">INPUTS</span></span>

### <span data-ttu-id="32453-148">System.String</span><span class="sxs-lookup"><span data-stu-id="32453-148">System.String</span></span>

### <span data-ttu-id="32453-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="32453-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="32453-150">출력</span><span class="sxs-lookup"><span data-stu-id="32453-150">OUTPUTS</span></span>

### <span data-ttu-id="32453-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="32453-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32453-152">NOTES</span></span>
* <span data-ttu-id="32453-153">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="32453-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="32453-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32453-154">RELATED LINKS</span></span>

[<span data-ttu-id="32453-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="32453-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="32453-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="32453-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="32453-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="32453-159">suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="32453-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


