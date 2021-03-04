---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952747"
---
# <span data-ttu-id="8cc4a-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="8cc4a-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="8cc4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc4a-103">내보내기 만들기 또는 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-103">The operation to create or update a export.</span></span>
<span data-ttu-id="8cc4a-104">업데이트 작업은 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="8cc4a-105">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="8cc4a-106">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="8cc4a-107">구문</span><span class="sxs-lookup"><span data-stu-id="8cc4a-107">SYNTAX</span></span>

### <span data-ttu-id="8cc4a-108">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="8cc4a-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8cc4a-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8cc4a-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8cc4a-110">설명</span><span class="sxs-lookup"><span data-stu-id="8cc4a-110">DESCRIPTION</span></span>
<span data-ttu-id="8cc4a-111">내보내기 만들기 또는 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-111">The operation to create or update a export.</span></span>
<span data-ttu-id="8cc4a-112">업데이트 작업은 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="8cc4a-113">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="8cc4a-114">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="8cc4a-115">예제</span><span class="sxs-lookup"><span data-stu-id="8cc4a-115">EXAMPLES</span></span>

### <span data-ttu-id="8cc4a-116">예제 1: 범위 및 이름에 의해 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="8cc4a-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="8cc4a-117">범위 및 이름에 의해 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="8cc4a-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="8cc4a-118">예제 2: InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="8cc4a-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="8cc4a-119">InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="8cc4a-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="8cc4a-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cc4a-120">PARAMETERS</span></span>

### <span data-ttu-id="8cc4a-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="8cc4a-121">-ConfigurationColumn</span></span>
<span data-ttu-id="8cc4a-122">내보내기에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="8cc4a-123">제공되지 않은 경우 내보내기에는 사용 가능한 모든 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="8cc4a-124">사용 가능한 열은 고객 채널에 따라 다를 수 있습니다(예제 참조).</span><span class="sxs-lookup"><span data-stu-id="8cc4a-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="8cc4a-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="8cc4a-125">-DataSetGranularity</span></span>
<span data-ttu-id="8cc4a-126">내보내기에서 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="8cc4a-127">현재 'Daily'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="8cc4a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc4a-128">-DefaultProfile</span></span>
<span data-ttu-id="8cc4a-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc4a-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="8cc4a-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="8cc4a-131">내보내기에 대한 데이터를 끌어오기 위한 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="8cc4a-132">사용자 지정의 경우 특정 기간을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="8cc4a-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="8cc4a-133">-DefinitionType</span></span>
<span data-ttu-id="8cc4a-134">내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-134">The type of the export.</span></span>
<span data-ttu-id="8cc4a-135">'사용량'은 'ActualCost'에 해당하며, 아직 서비스 예약에 대한 요금 또는 상금에 대한 데이터를 제공하지 않는 내보내기에는 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="8cc4a-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="8cc4a-136">-DestinationContainer</span></span>
<span data-ttu-id="8cc4a-137">내보내기 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="8cc4a-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8cc4a-138">-DestinationResourceId</span></span>
<span data-ttu-id="8cc4a-139">내보내기 배달되는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="8cc4a-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="8cc4a-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="8cc4a-141">내보내기 업로드할 디렉터리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="8cc4a-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="8cc4a-142">-ETag</span></span>
<span data-ttu-id="8cc4a-143">리소스의 eTag입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-143">eTag of the resource.</span></span>
<span data-ttu-id="8cc4a-144">동시 업데이트 시나리오를 처리하기 위해 이 필드는 사용자가 최신 버전을 업데이트하는지 여부를 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="8cc4a-145">-Format</span><span class="sxs-lookup"><span data-stu-id="8cc4a-145">-Format</span></span>
<span data-ttu-id="8cc4a-146">배달되는 내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-146">The format of the export being delivered.</span></span>
<span data-ttu-id="8cc4a-147">현재 'Csv'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="8cc4a-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cc4a-148">-InputObject</span></span>
<span data-ttu-id="8cc4a-149">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8cc4a-150">-Name</span><span class="sxs-lookup"><span data-stu-id="8cc4a-150">-Name</span></span>
<span data-ttu-id="8cc4a-151">이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-151">Export Name.</span></span>

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

### <span data-ttu-id="8cc4a-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="8cc4a-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="8cc4a-153">재발의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="8cc4a-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="8cc4a-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="8cc4a-155">재발의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="8cc4a-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="8cc4a-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="8cc4a-157">일정 재발.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="8cc4a-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="8cc4a-158">-ScheduleStatus</span></span>
<span data-ttu-id="8cc4a-159">내보내기 일정의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-159">The status of the export's schedule.</span></span>
<span data-ttu-id="8cc4a-160">'비활성'인 경우 내보내기 일정이 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="8cc4a-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="8cc4a-161">-Scope</span></span>
<span data-ttu-id="8cc4a-162">이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="8cc4a-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="8cc4a-163">-TimePeriodFrom</span></span>
<span data-ttu-id="8cc4a-164">내보내기 데이터의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-164">The start date for export data.</span></span>

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

### <span data-ttu-id="8cc4a-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="8cc4a-165">-TimePeriodTo</span></span>
<span data-ttu-id="8cc4a-166">내보내기 데이터의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-166">The end date for export data.</span></span>

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

### <span data-ttu-id="8cc4a-167">-확인</span><span class="sxs-lookup"><span data-stu-id="8cc4a-167">-Confirm</span></span>
<span data-ttu-id="8cc4a-168">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc4a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc4a-169">-WhatIf</span></span>
<span data-ttu-id="8cc4a-170">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc4a-171">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc4a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc4a-172">CommonParameters</span></span>
<span data-ttu-id="8cc4a-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc4a-174">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cc4a-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc4a-175">입력</span><span class="sxs-lookup"><span data-stu-id="8cc4a-175">INPUTS</span></span>

### <span data-ttu-id="8cc4a-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="8cc4a-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="8cc4a-177">출력</span><span class="sxs-lookup"><span data-stu-id="8cc4a-177">OUTPUTS</span></span>

### <span data-ttu-id="8cc4a-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="8cc4a-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="8cc4a-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8cc4a-179">NOTES</span></span>

<span data-ttu-id="8cc4a-180">별칭</span><span class="sxs-lookup"><span data-stu-id="8cc4a-180">ALIASES</span></span>

<span data-ttu-id="8cc4a-181">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8cc4a-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8cc4a-182">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8cc4a-183">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8cc4a-184">INPUTOBJECT <ICostManagementIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cc4a-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8cc4a-185">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="8cc4a-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="8cc4a-186">`[ExportName <String>]`: 이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="8cc4a-187">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대해 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="8cc4a-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="8cc4a-189">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="8cc4a-190">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8cc4a-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8cc4a-191">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc4a-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="8cc4a-192">여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}', ResourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위의 'providers/Microsoft.Billing/billingAccountId}/billingProfiles/{billingProfileId}' BillingProfile scope, 'providers/Microsoft.BillingAccountId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}'.Management/managementGroups/{managementGroupId}' for Management Group 범위, 'providers/Microsoft.CostManagement/externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptionName}'</span><span class="sxs-lookup"><span data-stu-id="8cc4a-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="8cc4a-193">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="8cc4a-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="8cc4a-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cc4a-194">RELATED LINKS</span></span>

