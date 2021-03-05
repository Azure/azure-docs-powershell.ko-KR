---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010672"
---
# <span data-ttu-id="a58b6-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="a58b6-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="a58b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a58b6-103">내보내기 만들기 또는 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-103">The operation to create or update a export.</span></span>
<span data-ttu-id="a58b6-104">업데이트 작업은 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="a58b6-105">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="a58b6-106">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="a58b6-107">구문</span><span class="sxs-lookup"><span data-stu-id="a58b6-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a58b6-108">설명</span><span class="sxs-lookup"><span data-stu-id="a58b6-108">DESCRIPTION</span></span>
<span data-ttu-id="a58b6-109">내보내기 만들기 또는 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-109">The operation to create or update a export.</span></span>
<span data-ttu-id="a58b6-110">업데이트 작업은 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="a58b6-111">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="a58b6-112">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="a58b6-113">예제</span><span class="sxs-lookup"><span data-stu-id="a58b6-113">EXAMPLES</span></span>

### <span data-ttu-id="a58b6-114">예제 1: AzCostManagementExport 만들기</span><span class="sxs-lookup"><span data-stu-id="a58b6-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="a58b6-115">AzCostManagementExport 만들기</span><span class="sxs-lookup"><span data-stu-id="a58b6-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="a58b6-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a58b6-116">PARAMETERS</span></span>

### <span data-ttu-id="a58b6-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="a58b6-117">-ConfigurationColumn</span></span>
<span data-ttu-id="a58b6-118">내보내기에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="a58b6-119">제공되지 않은 경우 내보내기에는 사용 가능한 모든 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="a58b6-120">사용 가능한 열은 고객 채널에 따라 다를 수 있습니다(예제 참조).</span><span class="sxs-lookup"><span data-stu-id="a58b6-120">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="a58b6-121">-DataSetGranularity</span></span>
<span data-ttu-id="a58b6-122">내보내기에서 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="a58b6-123">현재 'Daily'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-123">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58b6-124">-DefaultProfile</span></span>
<span data-ttu-id="a58b6-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="a58b6-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="a58b6-127">내보내기에 대한 데이터를 끌어오기 위한 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="a58b6-128">사용자 지정의 경우 특정 기간을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-128">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="a58b6-129">-DefinitionType</span></span>
<span data-ttu-id="a58b6-130">내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-130">The type of the export.</span></span>
<span data-ttu-id="a58b6-131">'사용량'은 'ActualCost'에 해당하며, 아직 서비스 예약에 대한 요금 또는 상금에 대한 데이터를 제공하지 않는 내보내기에는 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="a58b6-132">-DestinationContainer</span></span>
<span data-ttu-id="a58b6-133">내보내기 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-133">The name of the container where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a58b6-134">-DestinationResourceId</span></span>
<span data-ttu-id="a58b6-135">내보내기 배달되는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-135">The resource id of the storage account where exports will be delivered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="a58b6-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="a58b6-137">내보내기 업로드할 디렉터리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-137">The name of the directory where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-138">-Format</span><span class="sxs-lookup"><span data-stu-id="a58b6-138">-Format</span></span>
<span data-ttu-id="a58b6-139">배달되는 내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-139">The format of the export being delivered.</span></span>
<span data-ttu-id="a58b6-140">현재 'Csv'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-140">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-141">-Name</span><span class="sxs-lookup"><span data-stu-id="a58b6-141">-Name</span></span>
<span data-ttu-id="a58b6-142">이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="a58b6-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="a58b6-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="a58b6-144">재발의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-144">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="a58b6-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="a58b6-146">재발의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-146">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="a58b6-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="a58b6-148">일정 재발.</span><span class="sxs-lookup"><span data-stu-id="a58b6-148">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="a58b6-149">-ScheduleStatus</span></span>
<span data-ttu-id="a58b6-150">내보내기 일정의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-150">The status of the export's schedule.</span></span>
<span data-ttu-id="a58b6-151">'비활성'인 경우 내보내기 일정이 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-151">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="a58b6-152">-Scope</span></span>
<span data-ttu-id="a58b6-153">이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="a58b6-154">-TimePeriodFrom</span></span>
<span data-ttu-id="a58b6-155">내보내기 데이터의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-155">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="a58b6-156">-TimePeriodTo</span></span>
<span data-ttu-id="a58b6-157">내보내기 데이터의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-157">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-158">-확인</span><span class="sxs-lookup"><span data-stu-id="a58b6-158">-Confirm</span></span>
<span data-ttu-id="a58b6-159">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58b6-160">-WhatIf</span></span>
<span data-ttu-id="a58b6-161">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58b6-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58b6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58b6-163">CommonParameters</span></span>
<span data-ttu-id="a58b6-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58b6-165">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a58b6-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58b6-166">입력</span><span class="sxs-lookup"><span data-stu-id="a58b6-166">INPUTS</span></span>

## <span data-ttu-id="a58b6-167">출력</span><span class="sxs-lookup"><span data-stu-id="a58b6-167">OUTPUTS</span></span>

### <span data-ttu-id="a58b6-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="a58b6-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="a58b6-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a58b6-169">NOTES</span></span>

<span data-ttu-id="a58b6-170">별칭</span><span class="sxs-lookup"><span data-stu-id="a58b6-170">ALIASES</span></span>

## <span data-ttu-id="a58b6-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a58b6-171">RELATED LINKS</span></span>

