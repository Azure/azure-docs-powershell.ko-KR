---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525204"
---
# <span data-ttu-id="d11db-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="d11db-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="d11db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d11db-102">SYNOPSIS</span></span>
<span data-ttu-id="d11db-103">Azure Data Factory에서 dataset에 대 한 데이터 조각을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d11db-104">SYNTAX</span></span>

### <span data-ttu-id="d11db-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d11db-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d11db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d11db-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11db-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d11db-107">DESCRIPTION</span></span>
<span data-ttu-id="d11db-108">**AzureRmDataFactorySlice** Cmdlet은 Azure data Factory에서 dataset에 대 한 데이터 조각을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="d11db-109">시작 시간 및 종료 시간을 지정 하 여 표시할 데이터 조각의 범위를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="d11db-110">데이터 조각의 상태는 다음 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="d11db-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="d11db-111">PendingExecution.</span></span>
<span data-ttu-id="d11db-112">데이터 처리가 시작 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-112">Data processing has not started.</span></span> 
- <span data-ttu-id="d11db-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="d11db-113">InProgress.</span></span>
<span data-ttu-id="d11db-114">데이터 처리가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="d11db-115">수행할.</span><span class="sxs-lookup"><span data-stu-id="d11db-115">Ready.</span></span>
<span data-ttu-id="d11db-116">데이터 처리가 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-116">Data processing is completed.</span></span>
<span data-ttu-id="d11db-117">데이터 조각이 종속 슬라이스에 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="d11db-118">못함.</span><span class="sxs-lookup"><span data-stu-id="d11db-118">Failed.</span></span>
<span data-ttu-id="d11db-119">조각을 생성 하는 실행에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="d11db-120">[.</span><span class="sxs-lookup"><span data-stu-id="d11db-120">Skip.</span></span>
<span data-ttu-id="d11db-121">데이터 팩토리는 조각의 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="d11db-122">재시도.</span><span class="sxs-lookup"><span data-stu-id="d11db-122">Retry.</span></span>
<span data-ttu-id="d11db-123">데이터 팩토리는 조각을 생성 하는 실행을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="d11db-124">시간이 초과 되었습니다. 데이터 처리 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="d11db-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="d11db-125">PendingValidation.</span></span>
<span data-ttu-id="d11db-126">데이터 조각이 처리 되기 전에 유효성 검사를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="d11db-127">유효성 검사를 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-127">Retry Validation.</span></span>
<span data-ttu-id="d11db-128">데이터 팩토리는 조각의 유효성 검사를 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="d11db-129">유효성 검사에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-129">Failed Validation.</span></span>
<span data-ttu-id="d11db-130">조각의 유효성 검사에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-130">Validation of the slice failed.</span></span>

<span data-ttu-id="d11db-131">각 조각에 대해 Get-AzureRmDataFactoryRun cmdlet을 사용 하 여 조각을 생성 하는 실행에 대 한 자세한 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="d11db-132">예제의</span><span class="sxs-lookup"><span data-stu-id="d11db-132">EXAMPLES</span></span>

### <span data-ttu-id="d11db-133">예제 1: 데이터 집합에 대 한 데이터 조각 가져오기</span><span class="sxs-lookup"><span data-stu-id="d11db-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="d11db-134">이 명령은 WikiADF 이라는 data factory의 WikiAggregatedData 이라는 데이터 집합에 대 한 모든 데이터 조각을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="d11db-135">명령은 StartDateTime 매개 변수에서 지정 된 시간 후에 생성 되는 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="d11db-136">다음 예제 코드에서는 JSON (JavaScript 개체 표기) 파일에서 각 시간에 대해이 데이터 집합의 가용성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="d11db-137">준비 된 슬라이스가 이미 실행 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-137">Ready slices have already run.</span></span>
<span data-ttu-id="d11db-138">보류 중인 슬라이스가 Set-AzureRmDataFactoryPipelineActivePeriod cmdlet에서 지정 하는 간격으로 각 시간 끝에 실행 되기를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="d11db-139">이 예제에서는 파이프라인의 시작 및 종료 기간과 두 조각의 값이 모두 1 일 (24 시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="d11db-140">변수</span><span class="sxs-lookup"><span data-stu-id="d11db-140">PARAMETERS</span></span>

### <span data-ttu-id="d11db-141">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d11db-141">-DataFactory</span></span>
<span data-ttu-id="d11db-142">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d11db-143">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-144">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d11db-144">-DataFactoryName</span></span>
<span data-ttu-id="d11db-145">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d11db-146">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-147">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d11db-147">-DatasetName</span></span>
<span data-ttu-id="d11db-148">이 cmdlet이 조각을 가져오는 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11db-149">-DefaultProfile</span></span>
<span data-ttu-id="d11db-150">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d11db-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-151">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d11db-151">-EndDateTime</span></span>
<span data-ttu-id="d11db-152">시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-152">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d11db-153">이 cmdlet은이 매개 변수에서 지정 하는 시간 전에 생성 된 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-153">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="d11db-154">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-154">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="d11db-155">*Enddatetime* 은 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-155">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="d11db-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시)</span><span class="sxs-lookup"><span data-stu-id="d11db-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="d11db-157">기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-157">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11db-158">-ResourceGroupName</span></span>
<span data-ttu-id="d11db-159">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d11db-160">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-160">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-161">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d11db-161">-StartDateTime</span></span>
<span data-ttu-id="d11db-162">시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-162">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d11db-163">이 cmdlet은이 매개 변수에서 지정 된 시간 후에 생성 되는 슬라이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-163">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11db-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11db-164">CommonParameters</span></span>
<span data-ttu-id="d11db-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11db-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11db-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11db-167">입력</span><span class="sxs-lookup"><span data-stu-id="d11db-167">INPUTS</span></span>

### <span data-ttu-id="d11db-168">않아야</span><span class="sxs-lookup"><span data-stu-id="d11db-168">None</span></span>
<span data-ttu-id="d11db-169">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-169">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d11db-170">출력</span><span class="sxs-lookup"><span data-stu-id="d11db-170">OUTPUTS</span></span>

### <span data-ttu-id="d11db-171">AtaSlice ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSD], WindowsAzure. 유틸리티, Version = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11db-171">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d11db-172">상속자</span><span class="sxs-lookup"><span data-stu-id="d11db-172">NOTES</span></span>
* <span data-ttu-id="d11db-173">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d11db-173">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d11db-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d11db-174">RELATED LINKS</span></span>

[<span data-ttu-id="d11db-175">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="d11db-175">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="d11db-176">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="d11db-176">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="d11db-177">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d11db-177">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


