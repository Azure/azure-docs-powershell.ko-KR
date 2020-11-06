---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: ce1d81fc0226c7c44682d67cb666e3e63dfd5816
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530378"
---
# <span data-ttu-id="172be-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="172be-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="172be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172be-102">SYNOPSIS</span></span>
<span data-ttu-id="172be-103">Azure Data Factory에서 데이터 집합의 슬라이스 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="172be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="172be-104">SYNTAX</span></span>

### <span data-ttu-id="172be-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="172be-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="172be-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="172be-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172be-107">설명은</span><span class="sxs-lookup"><span data-stu-id="172be-107">DESCRIPTION</span></span>
<span data-ttu-id="172be-108">**AzureRmDataFactorySliceStatus** Cmdlet은 Azure Data Factory에서 데이터 집합에 대 한 조각의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="172be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="172be-109">EXAMPLES</span></span>

### <span data-ttu-id="172be-110">예제 1: 모든 조각의 상태 설정</span><span class="sxs-lookup"><span data-stu-id="172be-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="172be-111">이 명령은 DAWikiAggregatedData 이라는 데이터 집합에 대 한 모든 조각의 상태를 WikiADF 이라는 data factory에서 대기 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="172be-112">*Updatetype* 매개 변수에는 UpstreamInPipeline 값이 있으므로이 명령은 데이터 집합 및 모든 종속 데이터 집합에 대 한 각 조각의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="172be-113">종속 데이터 집합은 파이프라인의 활동에 대 한 입력 데이터 집합으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="172be-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="172be-114">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="172be-115">변수</span><span class="sxs-lookup"><span data-stu-id="172be-115">PARAMETERS</span></span>

### <span data-ttu-id="172be-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="172be-116">-DataFactory</span></span>
<span data-ttu-id="172be-117">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="172be-118">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 조각의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="172be-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="172be-119">-DataFactoryName</span></span>
<span data-ttu-id="172be-120">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="172be-121">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 조각의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="172be-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="172be-122">-DatasetName</span></span>
<span data-ttu-id="172be-123">이 cmdlet이 조각을 수정 하는 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="172be-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172be-124">-DefaultProfile</span></span>
<span data-ttu-id="172be-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="172be-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="172be-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="172be-126">-EndDateTime</span></span>
<span data-ttu-id="172be-127">시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="172be-128">이 시간은 데이터 조각의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="172be-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="172be-129">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="172be-130">*Enddatetime* 은 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 2015-01-01z 2015-01-01T00:00:00z 2015-01-01t00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시) 기본 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="172be-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="172be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172be-131">-ResourceGroupName</span></span>
<span data-ttu-id="172be-132">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="172be-133">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 조각의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="172be-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="172be-134">-StartDateTime</span></span>
<span data-ttu-id="172be-135">시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="172be-136">이 시간은 데이터 조각의 시작 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="172be-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="172be-137">-상태</span><span class="sxs-lookup"><span data-stu-id="172be-137">-Status</span></span>
<span data-ttu-id="172be-138">데이터 조각에 할당할 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="172be-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="172be-140">기다립니다.</span><span class="sxs-lookup"><span data-stu-id="172be-140">Waiting.</span></span>
<span data-ttu-id="172be-141">데이터 조각이 처리 되기 전에 유효성 검사 정책에 대 한 유효성 검사를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="172be-142">수행할.</span><span class="sxs-lookup"><span data-stu-id="172be-142">Ready.</span></span>
<span data-ttu-id="172be-143">데이터 처리가 완료 되 고 데이터 조각이 준비 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="172be-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="172be-144">InProgress.</span></span>
<span data-ttu-id="172be-145">데이터 처리가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="172be-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="172be-146">못함.</span><span class="sxs-lookup"><span data-stu-id="172be-146">Failed.</span></span>
<span data-ttu-id="172be-147">데이터 처리에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-147">Data processing failed.</span></span>
- <span data-ttu-id="172be-148">건너뛰면.</span><span class="sxs-lookup"><span data-stu-id="172be-148">Skipped.</span></span>
<span data-ttu-id="172be-149">데이터 조각 처리를 건너뛰었습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="172be-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="172be-150">-UpdateType</span></span>
<span data-ttu-id="172be-151">조각에 대 한 업데이트 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="172be-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="172be-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="172be-153">개별.</span><span class="sxs-lookup"><span data-stu-id="172be-153">Individual.</span></span>
<span data-ttu-id="172be-154">지정 된 시간 범위에서 데이터 집합에 대 한 각 조각의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="172be-155">UpstreamInPipeline입니다.</span><span class="sxs-lookup"><span data-stu-id="172be-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="172be-156">파이프라인의 활동에 대 한 입력 데이터 집합으로 사용 되는 데이터 집합 및 모든 종속 데이터 집합에 대 한 각 조각의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="172be-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172be-157">CommonParameters</span></span>
<span data-ttu-id="172be-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="172be-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172be-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172be-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172be-160">입력</span><span class="sxs-lookup"><span data-stu-id="172be-160">INPUTS</span></span>

### <span data-ttu-id="172be-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="172be-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="172be-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="172be-162">System.String</span></span>

## <span data-ttu-id="172be-163">출력</span><span class="sxs-lookup"><span data-stu-id="172be-163">OUTPUTS</span></span>

### <span data-ttu-id="172be-164">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="172be-164">System.Boolean</span></span>

## <span data-ttu-id="172be-165">상속자</span><span class="sxs-lookup"><span data-stu-id="172be-165">NOTES</span></span>
* <span data-ttu-id="172be-166">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="172be-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="172be-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="172be-167">RELATED LINKS</span></span>

[<span data-ttu-id="172be-168">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="172be-168">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


