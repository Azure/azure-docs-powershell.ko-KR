---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975312"
---
# <span data-ttu-id="67ed8-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="67ed8-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="67ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="67ed8-103">Azure Data Factory에서 데이터 세트에 대한 데이터 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="67ed8-104">구문</span><span class="sxs-lookup"><span data-stu-id="67ed8-104">SYNTAX</span></span>

### <span data-ttu-id="67ed8-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="67ed8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ed8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67ed8-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ed8-107">설명</span><span class="sxs-lookup"><span data-stu-id="67ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="67ed8-108">**Get-AzDataFactorySlice** cmdlet은 Azure Data Factory의 데이터 세트에 대한 데이터 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="67ed8-109">시작 시간 및 종료 시간을 지정하여 볼 데이터 조각 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="67ed8-110">데이터 조각의 상태는 다음 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="67ed8-111">pendingExecution.</span><span class="sxs-lookup"><span data-stu-id="67ed8-111">PendingExecution.</span></span>
<span data-ttu-id="67ed8-112">데이터 처리가 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-112">Data processing has not started.</span></span> 
- <span data-ttu-id="67ed8-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="67ed8-113">InProgress.</span></span>
<span data-ttu-id="67ed8-114">데이터 처리가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="67ed8-115">준비되었습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-115">Ready.</span></span>
<span data-ttu-id="67ed8-116">데이터 처리가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-116">Data processing is completed.</span></span>
<span data-ttu-id="67ed8-117">데이터 조각은 종속 조각을 사용할 준비가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="67ed8-118">실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-118">Failed.</span></span>
<span data-ttu-id="67ed8-119">조각을 생성하는 실행이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="67ed8-120">건너뛰기.</span><span class="sxs-lookup"><span data-stu-id="67ed8-120">Skip.</span></span>
<span data-ttu-id="67ed8-121">Data Factory는 조각의 처리를 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="67ed8-122">다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-122">Retry.</span></span>
<span data-ttu-id="67ed8-123">Data Factory는 조각을 생성하는 실행을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="67ed8-124">시간 외입니다. 데이터 처리 시간이 지날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="67ed8-125">보류 중인Validation입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-125">PendingValidation.</span></span>
<span data-ttu-id="67ed8-126">데이터 조각이 처리되기 전에 유효성 검사가 대기 중입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="67ed8-127">유효성 검사를 다시 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-127">Retry Validation.</span></span>
<span data-ttu-id="67ed8-128">Data Factory는 조각의 유효성 검사를 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="67ed8-129">유효성 검사에 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-129">Failed Validation.</span></span>
<span data-ttu-id="67ed8-130">조각의 유효성 검사가 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-130">Validation of the slice failed.</span></span>
<span data-ttu-id="67ed8-131">각 조각에 대해 Get-AzDataFactoryRun cmdlet을 사용하여 조각을 생성하는 실행에 대한 자세한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="67ed8-132">예제</span><span class="sxs-lookup"><span data-stu-id="67ed8-132">EXAMPLES</span></span>

### <span data-ttu-id="67ed8-133">예제 1: 데이터 세트에 대한 데이터 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="67ed8-134">이 명령은 WikiADF라는 데이터 팩터리에서 WikiAggregatedData라는 데이터 세트에 대한 모든 데이터 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="67ed8-135">명령은 StartDateTime 매개 변수가 지정한 시간 후에 생성되는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="67ed8-136">다음 예제 코드는 JSON(JavaScript 개체 표기법) 파일의 매시간 이 데이터 세트에 대한 가용성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="67ed8-137">가용성: {period: "Hour", periodMultiplier: 1 } 결과 중 일부는 준비되어 있으며 다른 결과는 pendingExecution입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="67ed8-138">준비된 조각이 이미 실행되었습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-138">Ready slices have already run.</span></span>
<span data-ttu-id="67ed8-139">보류 중인 조각은 cmdlet에서 지정하는 간격으로 각 시간의 Set-AzDataFactoryPipelineActivePeriod 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="67ed8-140">이 예제에서는 파이프라인 및 조각에 대한 시작 및 종료 기간 모두 1일(24시간)의 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="67ed8-141">예제 2</span><span class="sxs-lookup"><span data-stu-id="67ed8-141">Example 2</span></span>

<span data-ttu-id="67ed8-142">Azure Data Factory에서 데이터 세트에 대한 데이터 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="67ed8-143">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="67ed8-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="67ed8-144">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67ed8-144">PARAMETERS</span></span>

### <span data-ttu-id="67ed8-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67ed8-145">-DataFactory</span></span>
<span data-ttu-id="67ed8-146">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="67ed8-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="67ed8-147">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67ed8-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67ed8-148">-DataFactoryName</span></span>
<span data-ttu-id="67ed8-149">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="67ed8-150">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67ed8-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="67ed8-151">-DatasetName</span></span>
<span data-ttu-id="67ed8-152">이 cmdlet에서 조각을 얻을 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ed8-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ed8-153">-DefaultProfile</span></span>
<span data-ttu-id="67ed8-154">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67ed8-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67ed8-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="67ed8-155">-EndDateTime</span></span>
<span data-ttu-id="67ed8-156">기간의 끝을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="67ed8-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="67ed8-157">이 cmdlet은 이 매개 변수가 지정하기 전에 생성되는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="67ed8-158">**DateTime** 개체에 대한 자세한 내용은 `Get-Help Get-Date` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="67ed8-159">*EndDateTime은* 2015-01-01Z 2015-01-00:00Z 2015-01-01-0과 같이 ISO8601 형식으로 지정해야 합니다. 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed8-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ed8-160">-ResourceGroupName</span></span>
<span data-ttu-id="67ed8-161">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="67ed8-162">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="67ed8-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="67ed8-163">-StartDateTime</span></span>
<span data-ttu-id="67ed8-164">기간의 시작을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="67ed8-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="67ed8-165">이 cmdlet은 이 매개 변수가 지정한 시간 후에 생성되는 조각을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ed8-166">CommonParameters</span></span>
<span data-ttu-id="67ed8-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67ed8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ed8-168">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67ed8-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ed8-169">입력</span><span class="sxs-lookup"><span data-stu-id="67ed8-169">INPUTS</span></span>

### <span data-ttu-id="67ed8-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="67ed8-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="67ed8-171">System.String</span><span class="sxs-lookup"><span data-stu-id="67ed8-171">System.String</span></span>

## <span data-ttu-id="67ed8-172">출력</span><span class="sxs-lookup"><span data-stu-id="67ed8-172">OUTPUTS</span></span>

### <span data-ttu-id="67ed8-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="67ed8-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="67ed8-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67ed8-174">NOTES</span></span>
* <span data-ttu-id="67ed8-175">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="67ed8-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67ed8-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67ed8-176">RELATED LINKS</span></span>

[<span data-ttu-id="67ed8-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="67ed8-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="67ed8-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="67ed8-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="67ed8-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="67ed8-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


