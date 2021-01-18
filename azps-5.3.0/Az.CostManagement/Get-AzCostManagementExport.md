---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495733"
---
# <span data-ttu-id="1f921-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1f921-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="1f921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f921-102">SYNOPSIS</span></span>
<span data-ttu-id="1f921-103">내보내기 이름으로 정의된 범위에 대한 내보내기 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="1f921-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f921-104">SYNTAX</span></span>

### <span data-ttu-id="1f921-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f921-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f921-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1f921-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f921-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f921-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f921-108">설명</span><span class="sxs-lookup"><span data-stu-id="1f921-108">DESCRIPTION</span></span>
<span data-ttu-id="1f921-109">내보내기 이름으로 정의된 범위에 대한 내보내기 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="1f921-110">예제</span><span class="sxs-lookup"><span data-stu-id="1f921-110">EXAMPLES</span></span>

### <span data-ttu-id="1f921-111">예제 1: 범위에 의해 모든 AzCostManagementExports를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="1f921-112">범위에 의해 모든 AzCostManagementExports를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="1f921-113">예제 2: AzCostManagementExport by Name 및 scope</span><span class="sxs-lookup"><span data-stu-id="1f921-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="1f921-114">이름 및 범위로 AzCostManagementExport를 Get</span><span class="sxs-lookup"><span data-stu-id="1f921-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="1f921-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f921-115">PARAMETERS</span></span>

### <span data-ttu-id="1f921-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f921-116">-DefaultProfile</span></span>
<span data-ttu-id="1f921-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f921-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="1f921-118">-Expand</span></span>
<span data-ttu-id="1f921-119">내보내기 내에서 속성을 확장하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="1f921-120">현재 'runHistory'만 지원하며 내보내기 마지막 10개 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="1f921-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f921-121">-InputObject</span></span>
<span data-ttu-id="1f921-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1f921-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f921-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f921-123">-Name</span></span>
<span data-ttu-id="1f921-124">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-124">Export Name.</span></span>

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

### <span data-ttu-id="1f921-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="1f921-125">-Scope</span></span>
<span data-ttu-id="1f921-126">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="1f921-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f921-127">CommonParameters</span></span>
<span data-ttu-id="1f921-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f921-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f921-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f921-130">입력</span><span class="sxs-lookup"><span data-stu-id="1f921-130">INPUTS</span></span>

### <span data-ttu-id="1f921-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="1f921-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="1f921-132">출력</span><span class="sxs-lookup"><span data-stu-id="1f921-132">OUTPUTS</span></span>

### <span data-ttu-id="1f921-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="1f921-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="1f921-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f921-134">NOTES</span></span>

<span data-ttu-id="1f921-135">별칭</span><span class="sxs-lookup"><span data-stu-id="1f921-135">ALIASES</span></span>

<span data-ttu-id="1f921-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1f921-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f921-137">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f921-138">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f921-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f921-139">INPUTOBJECT: <ICostManagementIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f921-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f921-140">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="1f921-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="1f921-141">`[ExportName <String>]`: 이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="1f921-142">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}'이고 차원/쿼리 작업에 사용되는 통합 계정의 경우 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="1f921-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="1f921-144">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합된 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="1f921-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1f921-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f921-146">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1f921-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="1f921-147">여기에는 구독 범위의 'subscriptions/{subscriptionId}', resourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 청구 계정 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}'이 포함됩니다. Department 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccounts/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft 관리 그룹 범위에 대한 관리/managementGroups/{managementGroupId}', 외부 청구 계정 범위에 대한 'providers/Microsoft.CostManagement/externalBillingAccountName}', 외부 구독 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}'.</span><span class="sxs-lookup"><span data-stu-id="1f921-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="1f921-148">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="1f921-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="1f921-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f921-149">RELATED LINKS</span></span>

