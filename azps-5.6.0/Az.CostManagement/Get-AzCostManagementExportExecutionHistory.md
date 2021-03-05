---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009675"
---
# <span data-ttu-id="7e273-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="7e273-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="7e273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e273-102">SYNOPSIS</span></span>
<span data-ttu-id="7e273-103">정의된 범위 및 내보내기 이름에 대한 내보내기의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="7e273-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e273-104">SYNTAX</span></span>

### <span data-ttu-id="7e273-105">Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e273-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e273-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7e273-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e273-107">설명</span><span class="sxs-lookup"><span data-stu-id="7e273-107">DESCRIPTION</span></span>
<span data-ttu-id="7e273-108">정의된 범위 및 내보내기 이름에 대한 내보내기의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="7e273-109">예제</span><span class="sxs-lookup"><span data-stu-id="7e273-109">EXAMPLES</span></span>

### <span data-ttu-id="7e273-110">예제 1: AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="7e273-111">ExportName 및 Scope에 의해 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="7e273-112">예제 2: InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="7e273-113">InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="7e273-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e273-114">PARAMETERS</span></span>

### <span data-ttu-id="7e273-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e273-115">-DefaultProfile</span></span>
<span data-ttu-id="7e273-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e273-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="7e273-117">-ExportName</span></span>
<span data-ttu-id="7e273-118">이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="7e273-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e273-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e273-119">-InputObject</span></span>
<span data-ttu-id="7e273-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7e273-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e273-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="7e273-121">-Scope</span></span>
<span data-ttu-id="7e273-122">이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e273-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e273-123">CommonParameters</span></span>
<span data-ttu-id="7e273-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e273-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e273-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e273-126">입력</span><span class="sxs-lookup"><span data-stu-id="7e273-126">INPUTS</span></span>

### <span data-ttu-id="7e273-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="7e273-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="7e273-128">출력</span><span class="sxs-lookup"><span data-stu-id="7e273-128">OUTPUTS</span></span>

### <span data-ttu-id="7e273-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="7e273-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="7e273-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e273-130">NOTES</span></span>

<span data-ttu-id="7e273-131">별칭</span><span class="sxs-lookup"><span data-stu-id="7e273-131">ALIASES</span></span>

<span data-ttu-id="7e273-132">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7e273-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e273-133">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e273-134">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e273-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e273-135">INPUTOBJECT <ICostManagementIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e273-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e273-136">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="7e273-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="7e273-137">`[ExportName <String>]`: 이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="7e273-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="7e273-138">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대해 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="7e273-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="7e273-140">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="7e273-141">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7e273-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e273-142">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7e273-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="7e273-143">여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}', ResourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위의 'providers/Microsoft.Billing/billingAccountId}/billingProfiles/{billingProfileId}' BillingProfile scope, 'providers/Microsoft.BillingAccountId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}'.Management/managementGroups/{managementGroupId}' for Management Group 범위, 'providers/Microsoft.CostManagement/externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptionName}'</span><span class="sxs-lookup"><span data-stu-id="7e273-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="7e273-144">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="7e273-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="7e273-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e273-145">RELATED LINKS</span></span>

