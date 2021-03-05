---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: ef26f52068794349b785c8c067ead33b1ee3284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983600"
---
# <span data-ttu-id="0046f-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="0046f-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="0046f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0046f-102">SYNOPSIS</span></span>
<span data-ttu-id="0046f-103">내보내기 실행 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-103">The operation to execute an export.</span></span>

## <span data-ttu-id="0046f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0046f-104">SYNTAX</span></span>

### <span data-ttu-id="0046f-105">실행(기본값)</span><span class="sxs-lookup"><span data-stu-id="0046f-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0046f-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0046f-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0046f-107">설명</span><span class="sxs-lookup"><span data-stu-id="0046f-107">DESCRIPTION</span></span>
<span data-ttu-id="0046f-108">내보내기 실행 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-108">The operation to execute an export.</span></span>

## <span data-ttu-id="0046f-109">예제</span><span class="sxs-lookup"><span data-stu-id="0046f-109">EXAMPLES</span></span>

### <span data-ttu-id="0046f-110">예제 1: ExportName 및 Scope로 내보내기 호출</span><span class="sxs-lookup"><span data-stu-id="0046f-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="0046f-111">ExportName 및 Scope로 내보내기 호출</span><span class="sxs-lookup"><span data-stu-id="0046f-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="0046f-112">예제 2: InputObject로 내보내기 호출</span><span class="sxs-lookup"><span data-stu-id="0046f-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="0046f-113">InputObject로 내보내기 호출</span><span class="sxs-lookup"><span data-stu-id="0046f-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="0046f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0046f-114">PARAMETERS</span></span>

### <span data-ttu-id="0046f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0046f-115">-DefaultProfile</span></span>
<span data-ttu-id="0046f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0046f-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="0046f-117">-ExportName</span></span>
<span data-ttu-id="0046f-118">이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="0046f-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0046f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0046f-119">-InputObject</span></span>
<span data-ttu-id="0046f-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0046f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0046f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0046f-121">-PassThru</span></span>
<span data-ttu-id="0046f-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0046f-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="0046f-123">-Scope</span></span>
<span data-ttu-id="0046f-124">이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0046f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0046f-125">-Confirm</span></span>
<span data-ttu-id="0046f-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0046f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0046f-127">-WhatIf</span></span>
<span data-ttu-id="0046f-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0046f-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0046f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0046f-130">CommonParameters</span></span>
<span data-ttu-id="0046f-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0046f-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0046f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0046f-133">입력</span><span class="sxs-lookup"><span data-stu-id="0046f-133">INPUTS</span></span>

### <span data-ttu-id="0046f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="0046f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="0046f-135">출력</span><span class="sxs-lookup"><span data-stu-id="0046f-135">OUTPUTS</span></span>

### <span data-ttu-id="0046f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0046f-136">System.Boolean</span></span>

## <span data-ttu-id="0046f-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0046f-137">NOTES</span></span>

<span data-ttu-id="0046f-138">별칭</span><span class="sxs-lookup"><span data-stu-id="0046f-138">ALIASES</span></span>

<span data-ttu-id="0046f-139">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0046f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0046f-140">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0046f-141">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0046f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0046f-142">INPUTOBJECT <ICostManagementIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0046f-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0046f-143">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="0046f-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="0046f-144">`[ExportName <String>]`: 이름 내보내기.</span><span class="sxs-lookup"><span data-stu-id="0046f-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="0046f-145">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대해 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="0046f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="0046f-147">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="0046f-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0046f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0046f-149">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="0046f-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="0046f-150">여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}', ResourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위의 'providers/Microsoft.Billing/billingAccountId}/billingProfiles/{billingProfileId}' BillingProfile scope, 'providers/Microsoft.BillingAccountId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}'.Management/managementGroups/{managementGroupId}' for Management Group 범위, 'providers/Microsoft.CostManagement/externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptionName}'</span><span class="sxs-lookup"><span data-stu-id="0046f-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="0046f-151">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="0046f-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="0046f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0046f-152">RELATED LINKS</span></span>

