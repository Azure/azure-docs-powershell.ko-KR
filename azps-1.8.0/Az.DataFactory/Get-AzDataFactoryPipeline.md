---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701161"
---
# <span data-ttu-id="5ca26-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5ca26-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="5ca26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca26-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca26-103">Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="5ca26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ca26-104">SYNTAX</span></span>

### <span data-ttu-id="5ca26-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ca26-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca26-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5ca26-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca26-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5ca26-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca26-108">**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="5ca26-109">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="5ca26-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="5ca26-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5ca26-111">EXAMPLES</span></span>

### <span data-ttu-id="5ca26-112">예제 1: 모든 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="5ca26-113">이 명령은 WikiADF 이라는 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="5ca26-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="5ca26-115">두 번째는 **DataFactory** 개체를 매개 변수로 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="5ca26-116">예제 2: 특정 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="5ca26-117">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5ca26-118">이 명령은 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 해당 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5ca26-119">해당 cmdlet은 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="5ca26-120">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5ca26-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="5ca26-121">예제 3: 특정 파이프라인의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="5ca26-122">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **Properties** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="5ca26-123">예제 4: 특정 파이프라인에 대 한 활동 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="5ca26-124">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **작업** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="5ca26-125">예제 5: 특정 파이프라인에 대 한 런타임 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="5ca26-126">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **Runtimeinfo** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="5ca26-127">예제 6: 첫 번째 활동의 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ca26-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="5ca26-128">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **작업** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="5ca26-129">명령에 **서식 목록을** 사용 하 여 **활동** 배열의 첫 번째 요소의 **입력** 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="5ca26-130">변수</span><span class="sxs-lookup"><span data-stu-id="5ca26-130">PARAMETERS</span></span>

### <span data-ttu-id="5ca26-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5ca26-131">-DataFactory</span></span>
<span data-ttu-id="5ca26-132">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5ca26-133">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ca26-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5ca26-134">-DataFactoryName</span></span>
<span data-ttu-id="5ca26-135">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5ca26-136">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ca26-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca26-137">-DefaultProfile</span></span>
<span data-ttu-id="5ca26-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5ca26-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ca26-139">-이름</span><span class="sxs-lookup"><span data-stu-id="5ca26-139">-Name</span></span>
<span data-ttu-id="5ca26-140">정보를 가져올 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="5ca26-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca26-141">-ResourceGroupName</span></span>
<span data-ttu-id="5ca26-142">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5ca26-143">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ca26-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca26-144">CommonParameters</span></span>
<span data-ttu-id="5ca26-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca26-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca26-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca26-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca26-147">입력</span><span class="sxs-lookup"><span data-stu-id="5ca26-147">INPUTS</span></span>

### <span data-ttu-id="5ca26-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ca26-148">System.String</span></span>

### <span data-ttu-id="5ca26-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ca26-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5ca26-150">출력</span><span class="sxs-lookup"><span data-stu-id="5ca26-150">OUTPUTS</span></span>

### <span data-ttu-id="5ca26-151">DataFactories. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="5ca26-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="5ca26-152">상속자</span><span class="sxs-lookup"><span data-stu-id="5ca26-152">NOTES</span></span>
* <span data-ttu-id="5ca26-153">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="5ca26-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ca26-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ca26-154">RELATED LINKS</span></span>

[<span data-ttu-id="5ca26-155">새로운 AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5ca26-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="5ca26-156">제거-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5ca26-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="5ca26-157">이력서-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5ca26-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="5ca26-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="5ca26-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="5ca26-159">일시 중단-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5ca26-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


