---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 5cbb353a0a6349842878ef787b75c1ce34b1cfd3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964928"
---
# <span data-ttu-id="f2df1-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f2df1-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="f2df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2df1-102">SYNOPSIS</span></span>
<span data-ttu-id="f2df1-103">데이터 조각에 대한 활성 기간을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="f2df1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2df1-104">SYNTAX</span></span>

### <span data-ttu-id="f2df1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f2df1-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2df1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f2df1-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2df1-107">설명</span><span class="sxs-lookup"><span data-stu-id="f2df1-107">DESCRIPTION</span></span>
<span data-ttu-id="f2df1-108">**Set-AzDataFactoryPipelineActivePeriod** cmdlet은 Azure Data Factory의 파이프라인에서 처리되는 데이터 조각에 대한 활성 기간을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="f2df1-109">Set-AzDataFactorySliceStatus cmdlet을 사용하여 데이터 세트에 대한 조각의 상태를 수정하는 경우 조각의 시작 시간 및 종료 시간이 파이프라인의 활성 기간에 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="f2df1-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="f2df1-110">파이프라인을 만든 후 데이터 처리가 발생하는 기간을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="f2df1-111">파이프라인에 대한 활성 기간을 지정하면 각 Data Factory 데이터 세트에 대해  정의된 가용성 속성을 기반으로 데이터 조각이 처리되는 기간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="f2df1-112">예제</span><span class="sxs-lookup"><span data-stu-id="f2df1-112">EXAMPLES</span></span>

### <span data-ttu-id="f2df1-113">예제 1: 활성 기간 구성</span><span class="sxs-lookup"><span data-stu-id="f2df1-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="f2df1-114">이 명령은 DPWikisample이라는 파이프라인이 프로세스하는 데이터 조각에 대한 활성 기간을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="f2df1-115">명령은 데이터 조각의 시작 및 끝점을 값으로 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="f2df1-116">명령은 값의 $True.</span><span class="sxs-lookup"><span data-stu-id="f2df1-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="f2df1-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2df1-117">PARAMETERS</span></span>

### <span data-ttu-id="f2df1-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="f2df1-118">-AutoResolve</span></span>
<span data-ttu-id="f2df1-119">이 cmdlet에서 자동 확인을 사용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="f2df1-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f2df1-120">-DataFactory</span></span>
<span data-ttu-id="f2df1-121">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f2df1-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f2df1-122">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인의 활성 기간을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2df1-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f2df1-123">-DataFactoryName</span></span>
<span data-ttu-id="f2df1-124">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f2df1-125">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인의 활성 기간을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2df1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2df1-126">-DefaultProfile</span></span>
<span data-ttu-id="f2df1-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2df1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2df1-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="f2df1-128">-EndDateTime</span></span>
<span data-ttu-id="f2df1-129">기간의 끝을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f2df1-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f2df1-130">데이터 처리가 발생하거나 데이터 조각이 이 기간 내에 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="f2df1-131">**DateTime** 개체에 대한 자세한 내용은 `Get-Help Get-Date` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f2df1-132">*EndDateTime은* 2015-01-01Z 2015-01-00:00Z 2015-01-01-0과 같이 ISO8601 형식으로 지정해야 합니다. 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="f2df1-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="f2df1-133">-ForceRecalculate</span></span>
<span data-ttu-id="f2df1-134">이 cmdlet에서 힘 재계산을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="f2df1-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f2df1-135">-PipelineName</span></span>
<span data-ttu-id="f2df1-136">파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="f2df1-137">이 cmdlet은 이 매개 변수가 지정하는 파이프라인에 대한 활성 기간을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2df1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2df1-138">-ResourceGroupName</span></span>
<span data-ttu-id="f2df1-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f2df1-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인의 활성 기간을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2df1-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="f2df1-141">-StartDateTime</span></span>
<span data-ttu-id="f2df1-142">기간의 시작을 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f2df1-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f2df1-143">데이터 처리가 발생하거나 데이터 조각이 이 기간 내에 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="f2df1-144">*StartDateTime은* ISO8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="f2df1-145">-확인</span><span class="sxs-lookup"><span data-stu-id="f2df1-145">-Confirm</span></span>
<span data-ttu-id="f2df1-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2df1-147">-WhatIf</span></span>
<span data-ttu-id="f2df1-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2df1-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2df1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2df1-150">CommonParameters</span></span>
<span data-ttu-id="f2df1-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2df1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2df1-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2df1-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2df1-153">입력</span><span class="sxs-lookup"><span data-stu-id="f2df1-153">INPUTS</span></span>

### <span data-ttu-id="f2df1-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f2df1-154">System.String</span></span>

### <span data-ttu-id="f2df1-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f2df1-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f2df1-156">출력</span><span class="sxs-lookup"><span data-stu-id="f2df1-156">OUTPUTS</span></span>

### <span data-ttu-id="f2df1-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2df1-157">System.Boolean</span></span>

## <span data-ttu-id="f2df1-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2df1-158">NOTES</span></span>
* <span data-ttu-id="f2df1-159">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="f2df1-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f2df1-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2df1-160">RELATED LINKS</span></span>

[<span data-ttu-id="f2df1-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f2df1-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="f2df1-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="f2df1-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


