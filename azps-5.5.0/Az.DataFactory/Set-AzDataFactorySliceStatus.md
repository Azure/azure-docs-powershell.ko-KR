---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208704"
---
# <span data-ttu-id="1da19-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="1da19-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="1da19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da19-102">SYNOPSIS</span></span>
<span data-ttu-id="1da19-103">Azure Data Factory에서 데이터 세트에 대한 조각의 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="1da19-104">구문</span><span class="sxs-lookup"><span data-stu-id="1da19-104">SYNTAX</span></span>

### <span data-ttu-id="1da19-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1da19-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1da19-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1da19-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da19-107">설명</span><span class="sxs-lookup"><span data-stu-id="1da19-107">DESCRIPTION</span></span>
<span data-ttu-id="1da19-108">**Set-AzDataFactorySliceStatus** cmdlet은 Azure Data Factory의 데이터 세트에 대한 조각의 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="1da19-109">예제</span><span class="sxs-lookup"><span data-stu-id="1da19-109">EXAMPLES</span></span>

### <span data-ttu-id="1da19-110">예제 1: 모든 조각의 상태 설정</span><span class="sxs-lookup"><span data-stu-id="1da19-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="1da19-111">이 명령은 DAWikiAggregatedData라는 데이터 세트에 대한 모든 조각의 상태를 WikiADF라는 데이터 팩터리에서 Waiting으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="1da19-112">*UpdateType* 매개 변수의 값은 UpstreamInPipeline이기 때문에 명령은 데이터 세트 및 모든 종속 데이터 세트에 대한 각 조각의 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="1da19-113">종속 데이터 세트는 파이프라인의 활동에 대한 입력 데이터 세트로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="1da19-114">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="1da19-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="1da19-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1da19-115">PARAMETERS</span></span>

### <span data-ttu-id="1da19-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1da19-116">-DataFactory</span></span>
<span data-ttu-id="1da19-117">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1da19-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1da19-118">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각의 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1da19-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1da19-119">-DataFactoryName</span></span>
<span data-ttu-id="1da19-120">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1da19-121">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각의 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1da19-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="1da19-122">-DatasetName</span></span>
<span data-ttu-id="1da19-123">이 cmdlet이 조각을 수정하는 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="1da19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da19-124">-DefaultProfile</span></span>
<span data-ttu-id="1da19-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1da19-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1da19-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="1da19-126">-EndDateTime</span></span>
<span data-ttu-id="1da19-127">기간의 끝을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1da19-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="1da19-128">이 시간은 데이터 조각의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="1da19-129">**DateTime** 개체에 대한 자세한 내용은 .를 입력합니다. `Get-Help Get-Date`</span><span class="sxs-lookup"><span data-stu-id="1da19-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1da19-130">*EndDateTime은* 다음 예제와 같이 ISO8601 형식으로 지정해야 합니다. 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-0 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="1da19-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da19-131">-ResourceGroupName</span></span>
<span data-ttu-id="1da19-132">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1da19-133">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 조각의 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1da19-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="1da19-134">-StartDateTime</span></span>
<span data-ttu-id="1da19-135">기간의 시작을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1da19-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="1da19-136">이번은 데이터 조각의 시작입니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="1da19-137">-Status</span><span class="sxs-lookup"><span data-stu-id="1da19-137">-Status</span></span>
<span data-ttu-id="1da19-138">데이터 조각에 할당할 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="1da19-139">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1da19-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1da19-140">대기 중입니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-140">Waiting.</span></span>
<span data-ttu-id="1da19-141">데이터 조각이 처리되기 전에 유효성 검사 정책에 대한 유효성 검사를 기다리고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="1da19-142">준비되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-142">Ready.</span></span>
<span data-ttu-id="1da19-143">데이터 처리가 완료되어 데이터 조각이 준비되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="1da19-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="1da19-144">InProgress.</span></span>
<span data-ttu-id="1da19-145">데이터 처리가 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="1da19-146">실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-146">Failed.</span></span>
<span data-ttu-id="1da19-147">데이터 처리에 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-147">Data processing failed.</span></span>
- <span data-ttu-id="1da19-148">건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-148">Skipped.</span></span>
<span data-ttu-id="1da19-149">데이터 조각 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="1da19-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="1da19-150">-UpdateType</span></span>
<span data-ttu-id="1da19-151">조각에 대한 업데이트 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="1da19-152">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1da19-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1da19-153">개인.</span><span class="sxs-lookup"><span data-stu-id="1da19-153">Individual.</span></span>
<span data-ttu-id="1da19-154">지정된 시간 범위의 데이터 세트에 대한 각 조각의 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="1da19-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="1da19-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="1da19-156">파이프라인의 활동에 대한 입력 데이터 세트로 사용되는 데이터 세트 및 모든 종속 데이터 세트에 대한 각 조각의 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="1da19-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da19-157">CommonParameters</span></span>
<span data-ttu-id="1da19-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1da19-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da19-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1da19-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da19-160">입력</span><span class="sxs-lookup"><span data-stu-id="1da19-160">INPUTS</span></span>

### <span data-ttu-id="1da19-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1da19-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1da19-162">System.String</span><span class="sxs-lookup"><span data-stu-id="1da19-162">System.String</span></span>

## <span data-ttu-id="1da19-163">출력</span><span class="sxs-lookup"><span data-stu-id="1da19-163">OUTPUTS</span></span>

### <span data-ttu-id="1da19-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1da19-164">System.Boolean</span></span>

## <span data-ttu-id="1da19-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1da19-165">NOTES</span></span>
* <span data-ttu-id="1da19-166">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="1da19-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1da19-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1da19-167">RELATED LINKS</span></span>

[<span data-ttu-id="1da19-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="1da19-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


