---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495727"
---
# <span data-ttu-id="bd3cb-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="bd3cb-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="bd3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3cb-103">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-103">The operation to create or update a export.</span></span>
<span data-ttu-id="bd3cb-104">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bd3cb-105">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bd3cb-106">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bd3cb-107">구문</span><span class="sxs-lookup"><span data-stu-id="bd3cb-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd3cb-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd3cb-108">DESCRIPTION</span></span>
<span data-ttu-id="bd3cb-109">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-109">The operation to create or update a export.</span></span>
<span data-ttu-id="bd3cb-110">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bd3cb-111">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bd3cb-112">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bd3cb-113">예제</span><span class="sxs-lookup"><span data-stu-id="bd3cb-113">EXAMPLES</span></span>

### <span data-ttu-id="bd3cb-114">예제 1: AzCostManagementExport 만들기</span><span class="sxs-lookup"><span data-stu-id="bd3cb-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="bd3cb-115">AzCostManagementExport 만들기</span><span class="sxs-lookup"><span data-stu-id="bd3cb-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="bd3cb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd3cb-116">PARAMETERS</span></span>

### <span data-ttu-id="bd3cb-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="bd3cb-117">-ConfigurationColumn</span></span>
<span data-ttu-id="bd3cb-118">내보내기에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="bd3cb-119">제공되지 않은 경우 내보내기에는 사용 가능한 모든 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="bd3cb-120">사용 가능한 열은 고객 채널에 따라 다를 수 있습니다(예제 참조).</span><span class="sxs-lookup"><span data-stu-id="bd3cb-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="bd3cb-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="bd3cb-121">-DataSetGranularity</span></span>
<span data-ttu-id="bd3cb-122">내보내기 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="bd3cb-123">현재는 '매일'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="bd3cb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd3cb-124">-DefaultProfile</span></span>
<span data-ttu-id="bd3cb-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd3cb-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="bd3cb-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="bd3cb-127">내보내기 데이터를 끌어오는 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="bd3cb-128">사용자 지정인 경우 특정 기간을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="bd3cb-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="bd3cb-129">-DefinitionType</span></span>
<span data-ttu-id="bd3cb-130">내보내기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-130">The type of the export.</span></span>
<span data-ttu-id="bd3cb-131">'Usage'는 'ActualCost'에 해당하며 서비스 예약에 대한 요금 또는 상금에 대한 데이터를 아직 제공하지 않는 내보내기에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="bd3cb-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="bd3cb-132">-DestinationContainer</span></span>
<span data-ttu-id="bd3cb-133">내보내기 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="bd3cb-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="bd3cb-134">-DestinationResourceId</span></span>
<span data-ttu-id="bd3cb-135">내보내기 배달될 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="bd3cb-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="bd3cb-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="bd3cb-137">내보내기 업로드할 디렉터리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="bd3cb-138">-Format</span><span class="sxs-lookup"><span data-stu-id="bd3cb-138">-Format</span></span>
<span data-ttu-id="bd3cb-139">배달되는 내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-139">The format of the export being delivered.</span></span>
<span data-ttu-id="bd3cb-140">현재는 'Csv'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="bd3cb-141">-Name</span><span class="sxs-lookup"><span data-stu-id="bd3cb-141">-Name</span></span>
<span data-ttu-id="bd3cb-142">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-142">Export Name.</span></span>

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

### <span data-ttu-id="bd3cb-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bd3cb-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="bd3cb-144">재발의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="bd3cb-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bd3cb-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="bd3cb-146">재발의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="bd3cb-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="bd3cb-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="bd3cb-148">일정 재발입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="bd3cb-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="bd3cb-149">-ScheduleStatus</span></span>
<span data-ttu-id="bd3cb-150">내보내기 일정의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-150">The status of the export's schedule.</span></span>
<span data-ttu-id="bd3cb-151">'비활성'인 경우 내보내기 일정이 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="bd3cb-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="bd3cb-152">-Scope</span></span>
<span data-ttu-id="bd3cb-153">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="bd3cb-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bd3cb-154">-TimePeriodFrom</span></span>
<span data-ttu-id="bd3cb-155">데이터 내보내기 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-155">The start date for export data.</span></span>

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

### <span data-ttu-id="bd3cb-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bd3cb-156">-TimePeriodTo</span></span>
<span data-ttu-id="bd3cb-157">내보내기 데이터의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-157">The end date for export data.</span></span>

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

### <span data-ttu-id="bd3cb-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd3cb-158">-Confirm</span></span>
<span data-ttu-id="bd3cb-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd3cb-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd3cb-160">-WhatIf</span></span>
<span data-ttu-id="bd3cb-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd3cb-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd3cb-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd3cb-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3cb-163">CommonParameters</span></span>
<span data-ttu-id="bd3cb-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3cb-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd3cb-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3cb-166">입력</span><span class="sxs-lookup"><span data-stu-id="bd3cb-166">INPUTS</span></span>

## <span data-ttu-id="bd3cb-167">출력</span><span class="sxs-lookup"><span data-stu-id="bd3cb-167">OUTPUTS</span></span>

### <span data-ttu-id="bd3cb-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="bd3cb-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="bd3cb-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd3cb-169">NOTES</span></span>

<span data-ttu-id="bd3cb-170">별칭</span><span class="sxs-lookup"><span data-stu-id="bd3cb-170">ALIASES</span></span>

## <span data-ttu-id="bd3cb-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd3cb-171">RELATED LINKS</span></span>

