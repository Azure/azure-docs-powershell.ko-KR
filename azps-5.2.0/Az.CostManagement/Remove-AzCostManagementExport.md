---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336609"
---
# <span data-ttu-id="a9ffb-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="a9ffb-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="a9ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ffb-103">내보내기 삭제 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-103">The operation to delete a export.</span></span>

## <span data-ttu-id="a9ffb-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9ffb-104">SYNTAX</span></span>

### <span data-ttu-id="a9ffb-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="a9ffb-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9ffb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9ffb-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9ffb-107">설명</span><span class="sxs-lookup"><span data-stu-id="a9ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="a9ffb-108">내보내기 삭제 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-108">The operation to delete a export.</span></span>

## <span data-ttu-id="a9ffb-109">예제</span><span class="sxs-lookup"><span data-stu-id="a9ffb-109">EXAMPLES</span></span>

### <span data-ttu-id="a9ffb-110">예제 1: 범위 및 이름으로 AzCostManagementExport 삭제</span><span class="sxs-lookup"><span data-stu-id="a9ffb-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="a9ffb-111">범위 및 ExportName에 의해 AzCostManagementExport 삭제</span><span class="sxs-lookup"><span data-stu-id="a9ffb-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="a9ffb-112">예제 2: 내보내기 개체로 AzCostManagementExport 삭제</span><span class="sxs-lookup"><span data-stu-id="a9ffb-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="a9ffb-113">InputObject로 AzCostManagementExport 삭제</span><span class="sxs-lookup"><span data-stu-id="a9ffb-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="a9ffb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9ffb-114">PARAMETERS</span></span>

### <span data-ttu-id="a9ffb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ffb-115">-DefaultProfile</span></span>
<span data-ttu-id="a9ffb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ffb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9ffb-117">-InputObject</span></span>
<span data-ttu-id="a9ffb-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ffb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9ffb-119">-Name</span></span>
<span data-ttu-id="a9ffb-120">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ffb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9ffb-121">-PassThru</span></span>
<span data-ttu-id="a9ffb-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a9ffb-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="a9ffb-123">-Scope</span></span>
<span data-ttu-id="a9ffb-124">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ffb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9ffb-125">-Confirm</span></span>
<span data-ttu-id="a9ffb-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ffb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ffb-127">-WhatIf</span></span>
<span data-ttu-id="a9ffb-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a9ffb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ffb-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ffb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ffb-130">CommonParameters</span></span>
<span data-ttu-id="a9ffb-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ffb-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ffb-133">입력</span><span class="sxs-lookup"><span data-stu-id="a9ffb-133">INPUTS</span></span>

### <span data-ttu-id="a9ffb-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="a9ffb-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="a9ffb-135">출력</span><span class="sxs-lookup"><span data-stu-id="a9ffb-135">OUTPUTS</span></span>

### <span data-ttu-id="a9ffb-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9ffb-136">System.Boolean</span></span>

## <span data-ttu-id="a9ffb-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9ffb-137">NOTES</span></span>

<span data-ttu-id="a9ffb-138">별칭</span><span class="sxs-lookup"><span data-stu-id="a9ffb-138">ALIASES</span></span>

<span data-ttu-id="a9ffb-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a9ffb-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9ffb-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9ffb-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9ffb-142">INPUTOBJECT: <ICostManagementIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9ffb-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9ffb-143">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="a9ffb-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="a9ffb-144">`[ExportName <String>]`: 이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="a9ffb-145">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}'이고 차원/쿼리 작업에 사용되는 통합 계정의 경우 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="a9ffb-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="a9ffb-147">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합된 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="a9ffb-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a9ffb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9ffb-149">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="a9ffb-150">여기에는 구독 범위의 'subscriptions/{subscriptionId}', resourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 청구 계정 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}'이 포함됩니다. Department 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccounts/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft 관리 그룹 범위에 대한 관리/managementGroups/{managementGroupId}', 외부 청구 계정 범위에 대한 'providers/Microsoft.CostManagement/externalBillingAccountName}', 외부 구독 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}'.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="a9ffb-151">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="a9ffb-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="a9ffb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9ffb-152">RELATED LINKS</span></span>

