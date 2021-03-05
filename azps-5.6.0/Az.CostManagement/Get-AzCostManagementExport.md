---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996814"
---
# <span data-ttu-id="57dd6-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="57dd6-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="57dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="57dd6-103">내보내기 이름으로 정의된 범위에 대한 내보내기 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="57dd6-104">구문</span><span class="sxs-lookup"><span data-stu-id="57dd6-104">SYNTAX</span></span>

### <span data-ttu-id="57dd6-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="57dd6-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="57dd6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="57dd6-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="57dd6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57dd6-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57dd6-108">설명</span><span class="sxs-lookup"><span data-stu-id="57dd6-108">DESCRIPTION</span></span>
<span data-ttu-id="57dd6-109">내보내기 이름으로 정의된 범위에 대한 내보내기 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="57dd6-110">예제</span><span class="sxs-lookup"><span data-stu-id="57dd6-110">EXAMPLES</span></span>

### <span data-ttu-id="57dd6-111">예제 1: 범위에 의해 모든 AzCostManagementExports를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="57dd6-112">범위에 의해 모든 AzCostManagementExports를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="57dd6-113">예제 2: 이름 및 범위로 AzCostManagementExport를 얻다</span><span class="sxs-lookup"><span data-stu-id="57dd6-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="57dd6-114">이름 및 범위로 AzCostManagementExport를 얻다</span><span class="sxs-lookup"><span data-stu-id="57dd6-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="57dd6-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57dd6-115">PARAMETERS</span></span>

### <span data-ttu-id="57dd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57dd6-116">-DefaultProfile</span></span>
<span data-ttu-id="57dd6-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57dd6-118">-확장</span><span class="sxs-lookup"><span data-stu-id="57dd6-118">-Expand</span></span>
<span data-ttu-id="57dd6-119">내보내기 내에서 속성을 확장하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="57dd6-120">현재 'runHistory'만 지원하며 내보내기의 마지막 10개 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="57dd6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57dd6-121">-InputObject</span></span>
<span data-ttu-id="57dd6-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="57dd6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57dd6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="57dd6-123">-Name</span></span>
<span data-ttu-id="57dd6-124">이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="57dd6-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dd6-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="57dd6-125">-Scope</span></span>
<span data-ttu-id="57dd6-126">이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57dd6-127">CommonParameters</span></span>
<span data-ttu-id="57dd6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57dd6-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57dd6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57dd6-130">입력</span><span class="sxs-lookup"><span data-stu-id="57dd6-130">INPUTS</span></span>

### <span data-ttu-id="57dd6-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="57dd6-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="57dd6-132">출력</span><span class="sxs-lookup"><span data-stu-id="57dd6-132">OUTPUTS</span></span>

### <span data-ttu-id="57dd6-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="57dd6-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="57dd6-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57dd6-134">NOTES</span></span>

<span data-ttu-id="57dd6-135">별칭</span><span class="sxs-lookup"><span data-stu-id="57dd6-135">ALIASES</span></span>

<span data-ttu-id="57dd6-136">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="57dd6-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57dd6-137">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57dd6-138">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57dd6-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57dd6-139">INPUTOBJECT <ICostManagementIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="57dd6-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57dd6-140">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="57dd6-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="57dd6-141">`[ExportName <String>]`: 이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="57dd6-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="57dd6-142">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대해 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="57dd6-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="57dd6-144">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="57dd6-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="57dd6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57dd6-146">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="57dd6-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="57dd6-147">여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}', ResourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위의 'providers/Microsoft.Billing/billingAccountId}/billingProfiles/{billingProfileId}' BillingProfile scope, 'providers/Microsoft.BillingAccountId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}'.Management/managementGroups/{managementGroupId}' for Management Group 범위, 'providers/Microsoft.CostManagement/externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptionName}'</span><span class="sxs-lookup"><span data-stu-id="57dd6-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="57dd6-148">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="57dd6-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="57dd6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57dd6-149">RELATED LINKS</span></span>

