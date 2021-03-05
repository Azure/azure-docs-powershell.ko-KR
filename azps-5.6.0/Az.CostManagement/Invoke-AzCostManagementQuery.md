---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: c1bc78747807d0f481c35fc75ff6fcfc80a83787
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972880"
---
# <span data-ttu-id="e1eea-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="e1eea-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="e1eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1eea-102">SYNOPSIS</span></span>
<span data-ttu-id="e1eea-103">정의된 범위에 대한 사용 현황 데이터를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="e1eea-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1eea-104">SYNTAX</span></span>

### <span data-ttu-id="e1eea-105">UsageExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1eea-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1eea-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="e1eea-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1eea-107">설명</span><span class="sxs-lookup"><span data-stu-id="e1eea-107">DESCRIPTION</span></span>
<span data-ttu-id="e1eea-108">정의된 범위에 대한 사용 현황 데이터를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="e1eea-109">예제</span><span class="sxs-lookup"><span data-stu-id="e1eea-109">EXAMPLES</span></span>

### <span data-ttu-id="e1eea-110">예제 1: 범위에 따라 AzCostManagementQuery 호출</span><span class="sxs-lookup"><span data-stu-id="e1eea-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="e1eea-111">범위에 따라 AzCostManagementQuery 호출</span><span class="sxs-lookup"><span data-stu-id="e1eea-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="e1eea-112">예제 2: 차원이 있는 범위로 AzCostManagementQuery 호출</span><span class="sxs-lookup"><span data-stu-id="e1eea-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="e1eea-113">차원을 사용하여 범위에 따라 AzCostManagementQuery 호출</span><span class="sxs-lookup"><span data-stu-id="e1eea-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="e1eea-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1eea-114">PARAMETERS</span></span>

### <span data-ttu-id="e1eea-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="e1eea-115">-ConfigurationColumn</span></span>
<span data-ttu-id="e1eea-116">쿼리에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="e1eea-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="e1eea-117">-DatasetAggregation</span></span>
<span data-ttu-id="e1eea-118">쿼리에 사용할 집계 식의 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="e1eea-119">-DatasetFilter</span></span>
<span data-ttu-id="e1eea-120">쿼리에 사용할 필터 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="e1eea-121">생성을 위해 DATASETFILTER 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e1eea-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="e1eea-122">-DatasetGranularity</span></span>
<span data-ttu-id="e1eea-123">쿼리의 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="e1eea-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="e1eea-124">-DatasetGrouping</span></span>
<span data-ttu-id="e1eea-125">쿼리에서 사용할 식에 따라 그룹 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="e1eea-126">생성을 위해 DATASETGROUPING 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e1eea-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1eea-127">-DefaultProfile</span></span>
<span data-ttu-id="e1eea-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1eea-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="e1eea-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="e1eea-130">이는 연결된 계정의 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대한 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="e1eea-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="e1eea-132">차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="e1eea-133">-Scope</span></span>
<span data-ttu-id="e1eea-134">여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}/'가 포함됩니다. 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccountId}' for Billing Account Scope 및 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccount scope,'providers/Microsoft.Management/managementGroups/{managementGroups}for Management Group scope, 청구프로필 범위에 대한 '공급자/Microsoft.Billing/billingAccountId}/{billingAccountId}/billingProfileId}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' /billingProfiles/{billingProfileId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}' 및 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' 파트너에 특정.</span><span class="sxs-lookup"><span data-stu-id="e1eea-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="e1eea-135">-Timeframe</span></span>
<span data-ttu-id="e1eea-136">쿼리에 대한 데이터를 끌어오기 위한 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="e1eea-137">-TimePeriodFrom</span></span>
<span data-ttu-id="e1eea-138">데이터를 끌어오는 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="e1eea-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="e1eea-139">-TimePeriodTo</span></span>
<span data-ttu-id="e1eea-140">데이터를 끌어오는 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="e1eea-141">-Type</span><span class="sxs-lookup"><span data-stu-id="e1eea-141">-Type</span></span>
<span data-ttu-id="e1eea-142">쿼리의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1eea-143">-확인</span><span class="sxs-lookup"><span data-stu-id="e1eea-143">-Confirm</span></span>
<span data-ttu-id="e1eea-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1eea-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1eea-145">-WhatIf</span></span>
<span data-ttu-id="e1eea-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1eea-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1eea-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1eea-148">CommonParameters</span></span>
<span data-ttu-id="e1eea-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1eea-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1eea-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1eea-151">입력</span><span class="sxs-lookup"><span data-stu-id="e1eea-151">INPUTS</span></span>

## <span data-ttu-id="e1eea-152">출력</span><span class="sxs-lookup"><span data-stu-id="e1eea-152">OUTPUTS</span></span>

### <span data-ttu-id="e1eea-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="e1eea-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="e1eea-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1eea-154">NOTES</span></span>

<span data-ttu-id="e1eea-155">별칭</span><span class="sxs-lookup"><span data-stu-id="e1eea-155">ALIASES</span></span>

<span data-ttu-id="e1eea-156">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e1eea-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1eea-157">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1eea-158">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1eea-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1eea-159">DATASETFILTER : 쿼리에 사용할 필터 <IQueryFilter> 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="e1eea-160">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="e1eea-161">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="e1eea-162">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="e1eea-163">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="e1eea-164">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="e1eea-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="e1eea-165">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="e1eea-166">`[Or <IQueryFilter[]>]`: 논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="e1eea-167">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="e1eea-168">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="e1eea-169">DATASETGROUPING <IQueryGrouping[]>: 쿼리에서 사용할 식에 따라 그룹 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="e1eea-170">`Name <String>`: 그룹화할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="e1eea-171">`Type <QueryColumnType>`: 그룹화할 열 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1eea-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="e1eea-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1eea-172">RELATED LINKS</span></span>

