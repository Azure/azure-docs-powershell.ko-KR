---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369237"
---
# <span data-ttu-id="4b85b-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4b85b-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="4b85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b85b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b85b-103">정책 할당에 대한 정책 수정을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="4b85b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b85b-104">SYNTAX</span></span>

### <span data-ttu-id="4b85b-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b85b-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b85b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b85b-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b85b-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b85b-107">DESCRIPTION</span></span>
<span data-ttu-id="4b85b-108">**Start-AzPolicyRemediation** cmdlet은 특정 정책 할당에 대한 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="4b85b-109">수정 범위의 모든 비준수 리소스가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="4b85b-110">수정은 'deployIfNotExists' 효과가 적용된 정책에만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="4b85b-111">예제</span><span class="sxs-lookup"><span data-stu-id="4b85b-111">EXAMPLES</span></span>

### <span data-ttu-id="4b85b-112">예제 1: 구독 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="4b85b-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="4b85b-113">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="4b85b-114">예제 2: 선택적 필터를 사용하여 관리 그룹 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="4b85b-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="4b85b-115">이 명령은 주어진 정책 할당에 대한 관리 그룹 'mg1'에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="4b85b-116">'westus' 또는 'eastus' 위치에 있는 리소스만 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="4b85b-117">예제 3: 정책 집합 정의 할당에 대한 리소스 그룹 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="4b85b-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="4b85b-118">이 명령은 주어진 정책 할당에 대한 리소스 그룹 'myRG'에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="4b85b-119">정책 할당은 이니셔티브라고도 하는 정책 집합 정의를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="4b85b-120">정책 정의 참조 ID는 이니셔티브 내에서 수정해야 하는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="4b85b-121">예제 4: 수정을 시작하고 백그라운드에서 완료될 때까지 기다림</span><span class="sxs-lookup"><span data-stu-id="4b85b-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="4b85b-122">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에서 새 정책 수정을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="4b85b-123">최종 수정 상태를 반환하기 전에 수정이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="4b85b-124">예제 5: 수정하기 전에 비준수 리소스를 검색하는 수정 시작</span><span class="sxs-lookup"><span data-stu-id="4b85b-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="4b85b-125">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="4b85b-126">구독의 리소스 규정 준수 상태는 정책 할당에 대해 다시 평가됩니다. 비준수 리소스는 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="4b85b-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b85b-127">PARAMETERS</span></span>

### <span data-ttu-id="4b85b-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b85b-128">-AsJob</span></span>
<span data-ttu-id="4b85b-129">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4b85b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b85b-130">-DefaultProfile</span></span>
<span data-ttu-id="4b85b-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="4b85b-132">-LocationFilter</span></span>
<span data-ttu-id="4b85b-133">수정에 포함해야 하는 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="4b85b-134">이러한 위치에 없는 리소스는 수정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4b85b-135">-ManagementGroupName</span></span>
<span data-ttu-id="4b85b-136">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-136">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4b85b-137">-Name</span></span>
<span data-ttu-id="4b85b-138">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-138">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="4b85b-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="4b85b-140">정책 할당 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-140">Policy assignment ID.</span></span>
<span data-ttu-id="4b85b-141">예:</span><span class="sxs-lookup"><span data-stu-id="4b85b-141">E.g.</span></span>
<span data-ttu-id="4b85b-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="4b85b-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="4b85b-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="4b85b-144">수정되는 개별 정의의 정책 정의 참조 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="4b85b-145">정책 할당이 정책 집합 정의를 할당할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="4b85b-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="4b85b-147">수정 작업에서 수정해야 하는 리소스를 검색하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="4b85b-148">관리 그룹 범위를 수정하는 경우 ReEvaluateCompliance가 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b85b-149">-ResourceGroupName</span></span>
<span data-ttu-id="4b85b-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b85b-151">-ResourceId</span></span>
<span data-ttu-id="4b85b-152">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-152">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="4b85b-153">-Scope</span></span>
<span data-ttu-id="4b85b-154">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-154">Scope of the resource.</span></span>
<span data-ttu-id="4b85b-155">예:</span><span class="sxs-lookup"><span data-stu-id="4b85b-155">E.g.</span></span>
<span data-ttu-id="4b85b-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="4b85b-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b85b-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b85b-157">-Confirm</span></span>
<span data-ttu-id="4b85b-158">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b85b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b85b-159">-WhatIf</span></span>
<span data-ttu-id="4b85b-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4b85b-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b85b-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b85b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b85b-162">CommonParameters</span></span>
<span data-ttu-id="4b85b-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b85b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b85b-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b85b-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b85b-165">입력</span><span class="sxs-lookup"><span data-stu-id="4b85b-165">INPUTS</span></span>

### <span data-ttu-id="4b85b-166">System.String</span><span class="sxs-lookup"><span data-stu-id="4b85b-166">System.String</span></span>

### <span data-ttu-id="4b85b-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4b85b-167">System.String[]</span></span>

## <span data-ttu-id="4b85b-168">출력</span><span class="sxs-lookup"><span data-stu-id="4b85b-168">OUTPUTS</span></span>

### <span data-ttu-id="4b85b-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="4b85b-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="4b85b-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b85b-170">NOTES</span></span>

## <span data-ttu-id="4b85b-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b85b-171">RELATED LINKS</span></span>
