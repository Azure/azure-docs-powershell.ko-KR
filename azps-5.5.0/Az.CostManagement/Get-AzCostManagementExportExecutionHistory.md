---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181212"
---
# <span data-ttu-id="65f39-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="65f39-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="65f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f39-102">SYNOPSIS</span></span>
<span data-ttu-id="65f39-103">정의된 범위 및 내보내기 이름에 대한 내보내기 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="65f39-104">구문</span><span class="sxs-lookup"><span data-stu-id="65f39-104">SYNTAX</span></span>

### <span data-ttu-id="65f39-105">Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="65f39-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="65f39-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65f39-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="65f39-107">설명</span><span class="sxs-lookup"><span data-stu-id="65f39-107">DESCRIPTION</span></span>
<span data-ttu-id="65f39-108">정의된 범위 및 내보내기 이름에 대한 내보내기 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="65f39-109">예제</span><span class="sxs-lookup"><span data-stu-id="65f39-109">EXAMPLES</span></span>

### <span data-ttu-id="65f39-110">예제 1: AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="65f39-111">ExportName 및 Scope로 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="65f39-112">예제 2: InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="65f39-113">InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="65f39-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65f39-114">PARAMETERS</span></span>

### <span data-ttu-id="65f39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f39-115">-DefaultProfile</span></span>
<span data-ttu-id="65f39-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f39-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="65f39-117">-ExportName</span></span>
<span data-ttu-id="65f39-118">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-118">Export Name.</span></span>

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

### <span data-ttu-id="65f39-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65f39-119">-InputObject</span></span>
<span data-ttu-id="65f39-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="65f39-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65f39-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="65f39-121">-Scope</span></span>
<span data-ttu-id="65f39-122">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="65f39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f39-123">CommonParameters</span></span>
<span data-ttu-id="65f39-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f39-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65f39-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f39-126">입력</span><span class="sxs-lookup"><span data-stu-id="65f39-126">INPUTS</span></span>

### <span data-ttu-id="65f39-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="65f39-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="65f39-128">출력</span><span class="sxs-lookup"><span data-stu-id="65f39-128">OUTPUTS</span></span>

### <span data-ttu-id="65f39-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="65f39-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="65f39-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65f39-130">NOTES</span></span>

<span data-ttu-id="65f39-131">별칭</span><span class="sxs-lookup"><span data-stu-id="65f39-131">ALIASES</span></span>

<span data-ttu-id="65f39-132">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="65f39-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65f39-133">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65f39-134">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65f39-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65f39-135">INPUTOBJECT: <ICostManagementIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="65f39-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65f39-136">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="65f39-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="65f39-137">`[ExportName <String>]`: 이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="65f39-138">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}'이고 차원/쿼리 작업에 사용되는 통합 계정의 경우 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="65f39-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="65f39-140">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합된 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="65f39-141">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="65f39-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65f39-142">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="65f39-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="65f39-143">여기에는 구독 범위의 'subscriptions/{subscriptionId}', resourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 청구 계정 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}'이 포함됩니다. Department 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccounts/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft 관리 그룹 범위에 대한 관리/managementGroups/{managementGroupId}', 외부 청구 계정 범위에 대한 'providers/Microsoft.CostManagement/externalBillingAccountName}', 외부 구독 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}'.</span><span class="sxs-lookup"><span data-stu-id="65f39-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="65f39-144">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="65f39-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="65f39-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65f39-145">RELATED LINKS</span></span>

