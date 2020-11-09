---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306038"
---
# <span data-ttu-id="3a827-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3a827-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="3a827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a827-102">SYNOPSIS</span></span>
<span data-ttu-id="3a827-103">데이터 조각에 대 한 활성 기간을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="3a827-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a827-104">SYNTAX</span></span>

### <span data-ttu-id="3a827-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a827-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a827-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3a827-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a827-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a827-107">DESCRIPTION</span></span>
<span data-ttu-id="3a827-108">**AzDataFactoryPipelineActivePeriod** Cmdlet은 Azure data Factory의 파이프라인이 처리 하는 데이터 조각의 활성 기간을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="3a827-109">Set-AzDataFactorySliceStatus cmdlet을 사용 하 여 데이터 집합의 슬라이스 상태를 수정 하는 경우 조각의 시작 시간 및 종료 시간이 파이프라인의 활성 기간에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="3a827-110">파이프라인을 만든 후 데이터 처리가 발생 하는 기간을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="3a827-111">파이프라인의 활성 기간을 지정 하면 데이터 조각이 각 데이터 팩토리 데이터 집합에 대해 정의 된 **가용성** 속성에 따라 처리 되는 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="3a827-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3a827-112">EXAMPLES</span></span>

### <span data-ttu-id="3a827-113">예제 1: 활성 기간 구성</span><span class="sxs-lookup"><span data-stu-id="3a827-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="3a827-114">이 명령은 DPWikisample 이라는 파이프라인이 처리 하는 데이터 조각에 대 한 활성 기간을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="3a827-115">명령은 데이터 조각의 시작 지점과 끝 지점을 값으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="3a827-116">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="3a827-117">변수</span><span class="sxs-lookup"><span data-stu-id="3a827-117">PARAMETERS</span></span>

### <span data-ttu-id="3a827-118">-자동 해결</span><span class="sxs-lookup"><span data-stu-id="3a827-118">-AutoResolve</span></span>
<span data-ttu-id="3a827-119">이 cmdlet이 자동 해결을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-119">Indicates that this cmdlet uses auto resolve.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a827-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a827-120">-DataFactory</span></span>
<span data-ttu-id="3a827-121">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3a827-122">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인의 활성 기간을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a827-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3a827-123">-DataFactoryName</span></span>
<span data-ttu-id="3a827-124">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3a827-125">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인의 활성 기간을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a827-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a827-126">-DefaultProfile</span></span>
<span data-ttu-id="3a827-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a827-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a827-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="3a827-128">-EndDateTime</span></span>
<span data-ttu-id="3a827-129">시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="3a827-130">데이터 처리가 발생 하거나이 기간 내에 데이터 조각이 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="3a827-131">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="3a827-132">*Enddatetime* 은 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 2015-01-01z 2015-01-01T00:00:00z 2015-01-01t00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시) 기본 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="3a827-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="3a827-133">-ForceRecalculate</span></span>
<span data-ttu-id="3a827-134">이 cmdlet이 강제 다시 계산을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-134">Indicates that this cmdlet uses force recalculate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a827-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3a827-135">-PipelineName</span></span>
<span data-ttu-id="3a827-136">파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="3a827-137">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인의 활성 기간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a827-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a827-138">-ResourceGroupName</span></span>
<span data-ttu-id="3a827-139">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3a827-140">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인의 활성 기간을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a827-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="3a827-141">-StartDateTime</span></span>
<span data-ttu-id="3a827-142">시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="3a827-143">데이터 처리가 발생 하거나이 기간 내에 데이터 조각이 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="3a827-144">*StartDateTime* 는 ISO8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="3a827-145">-확인</span><span class="sxs-lookup"><span data-stu-id="3a827-145">-Confirm</span></span>
<span data-ttu-id="3a827-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a827-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a827-147">-WhatIf</span></span>
<span data-ttu-id="3a827-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a827-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a827-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a827-150">CommonParameters</span></span>
<span data-ttu-id="3a827-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a827-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a827-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a827-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a827-153">입력</span><span class="sxs-lookup"><span data-stu-id="3a827-153">INPUTS</span></span>

### <span data-ttu-id="3a827-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a827-154">System.String</span></span>

### <span data-ttu-id="3a827-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a827-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3a827-156">출력</span><span class="sxs-lookup"><span data-stu-id="3a827-156">OUTPUTS</span></span>

### <span data-ttu-id="3a827-157">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3a827-157">System.Boolean</span></span>

## <span data-ttu-id="3a827-158">상속자</span><span class="sxs-lookup"><span data-stu-id="3a827-158">NOTES</span></span>
* <span data-ttu-id="3a827-159">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="3a827-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3a827-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a827-160">RELATED LINKS</span></span>

[<span data-ttu-id="3a827-161">새로운 AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3a827-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="3a827-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="3a827-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


