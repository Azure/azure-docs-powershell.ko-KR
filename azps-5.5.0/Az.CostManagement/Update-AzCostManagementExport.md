---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181156"
---
# <span data-ttu-id="28b9d-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="28b9d-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="28b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="28b9d-103">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-103">The operation to create or update a export.</span></span>
<span data-ttu-id="28b9d-104">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="28b9d-105">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="28b9d-106">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="28b9d-107">구문</span><span class="sxs-lookup"><span data-stu-id="28b9d-107">SYNTAX</span></span>

### <span data-ttu-id="28b9d-108">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="28b9d-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28b9d-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="28b9d-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28b9d-110">설명</span><span class="sxs-lookup"><span data-stu-id="28b9d-110">DESCRIPTION</span></span>
<span data-ttu-id="28b9d-111">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-111">The operation to create or update a export.</span></span>
<span data-ttu-id="28b9d-112">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="28b9d-113">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="28b9d-114">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="28b9d-115">예제</span><span class="sxs-lookup"><span data-stu-id="28b9d-115">EXAMPLES</span></span>

### <span data-ttu-id="28b9d-116">예제 1: 범위 및 이름으로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="28b9d-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="28b9d-117">범위 및 이름으로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="28b9d-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="28b9d-118">예제 2: InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="28b9d-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="28b9d-119">InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="28b9d-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="28b9d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28b9d-120">PARAMETERS</span></span>

### <span data-ttu-id="28b9d-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="28b9d-121">-ConfigurationColumn</span></span>
<span data-ttu-id="28b9d-122">내보내기에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="28b9d-123">제공되지 않은 경우 내보내기에는 사용 가능한 모든 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="28b9d-124">사용 가능한 열은 고객 채널에 따라 다를 수 있습니다(예제 참조).</span><span class="sxs-lookup"><span data-stu-id="28b9d-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="28b9d-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="28b9d-125">-DataSetGranularity</span></span>
<span data-ttu-id="28b9d-126">내보내기 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="28b9d-127">현재는 '매일'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="28b9d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b9d-128">-DefaultProfile</span></span>
<span data-ttu-id="28b9d-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b9d-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="28b9d-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="28b9d-131">내보내기 데이터를 끌어오는 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="28b9d-132">사용자 지정인 경우 특정 기간을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="28b9d-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="28b9d-133">-DefinitionType</span></span>
<span data-ttu-id="28b9d-134">내보내기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-134">The type of the export.</span></span>
<span data-ttu-id="28b9d-135">'Usage'는 'ActualCost'에 해당하며 서비스 예약에 대한 요금 또는 상금에 대한 데이터를 아직 제공하지 않는 내보내기에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="28b9d-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="28b9d-136">-DestinationContainer</span></span>
<span data-ttu-id="28b9d-137">내보내기 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="28b9d-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="28b9d-138">-DestinationResourceId</span></span>
<span data-ttu-id="28b9d-139">내보내기 배달될 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="28b9d-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="28b9d-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="28b9d-141">내보내기 업로드할 디렉터리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="28b9d-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="28b9d-142">-ETag</span></span>
<span data-ttu-id="28b9d-143">리소스의 eTag입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-143">eTag of the resource.</span></span>
<span data-ttu-id="28b9d-144">동시 업데이트 시나리오를 처리하기 위해 이 필드는 사용자가 최신 버전을 업데이트하는지 여부를 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="28b9d-145">-Format</span><span class="sxs-lookup"><span data-stu-id="28b9d-145">-Format</span></span>
<span data-ttu-id="28b9d-146">배달되는 내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-146">The format of the export being delivered.</span></span>
<span data-ttu-id="28b9d-147">현재는 'Csv'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="28b9d-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28b9d-148">-InputObject</span></span>
<span data-ttu-id="28b9d-149">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="28b9d-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b9d-150">-Name</span><span class="sxs-lookup"><span data-stu-id="28b9d-150">-Name</span></span>
<span data-ttu-id="28b9d-151">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b9d-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="28b9d-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="28b9d-153">재발의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="28b9d-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="28b9d-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="28b9d-155">재발의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="28b9d-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="28b9d-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="28b9d-157">일정 재발입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="28b9d-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="28b9d-158">-ScheduleStatus</span></span>
<span data-ttu-id="28b9d-159">내보내기 일정의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-159">The status of the export's schedule.</span></span>
<span data-ttu-id="28b9d-160">'비활성'인 경우 내보내기 일정이 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="28b9d-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="28b9d-161">-Scope</span></span>
<span data-ttu-id="28b9d-162">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b9d-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="28b9d-163">-TimePeriodFrom</span></span>
<span data-ttu-id="28b9d-164">데이터 내보내기 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-164">The start date for export data.</span></span>

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

### <span data-ttu-id="28b9d-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="28b9d-165">-TimePeriodTo</span></span>
<span data-ttu-id="28b9d-166">내보내기 데이터의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-166">The end date for export data.</span></span>

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

### <span data-ttu-id="28b9d-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28b9d-167">-Confirm</span></span>
<span data-ttu-id="28b9d-168">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b9d-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b9d-169">-WhatIf</span></span>
<span data-ttu-id="28b9d-170">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28b9d-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b9d-171">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b9d-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b9d-172">CommonParameters</span></span>
<span data-ttu-id="28b9d-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b9d-174">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28b9d-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b9d-175">입력</span><span class="sxs-lookup"><span data-stu-id="28b9d-175">INPUTS</span></span>

### <span data-ttu-id="28b9d-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="28b9d-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="28b9d-177">출력</span><span class="sxs-lookup"><span data-stu-id="28b9d-177">OUTPUTS</span></span>

### <span data-ttu-id="28b9d-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="28b9d-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="28b9d-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28b9d-179">NOTES</span></span>

<span data-ttu-id="28b9d-180">별칭</span><span class="sxs-lookup"><span data-stu-id="28b9d-180">ALIASES</span></span>

<span data-ttu-id="28b9d-181">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="28b9d-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28b9d-182">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28b9d-183">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28b9d-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28b9d-184">INPUTOBJECT: <ICostManagementIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="28b9d-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28b9d-185">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="28b9d-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="28b9d-186">`[ExportName <String>]`: 이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="28b9d-187">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}'이고 차원/쿼리 작업에 사용되는 통합 계정의 경우 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="28b9d-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="28b9d-189">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합된 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="28b9d-190">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="28b9d-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28b9d-191">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="28b9d-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="28b9d-192">여기에는 구독 범위의 'subscriptions/{subscriptionId}', resourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 청구 계정 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}'이 포함됩니다. Department 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccounts/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft 관리 그룹 범위에 대한 관리/managementGroups/{managementGroupId}', 외부 청구 계정 범위에 대한 'providers/Microsoft.CostManagement/externalBillingAccountName}', 외부 구독 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}'.</span><span class="sxs-lookup"><span data-stu-id="28b9d-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="28b9d-193">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="28b9d-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="28b9d-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28b9d-194">RELATED LINKS</span></span>

