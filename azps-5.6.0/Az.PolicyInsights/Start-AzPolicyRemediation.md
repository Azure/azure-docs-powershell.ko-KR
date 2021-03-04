---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989067"
---
# <span data-ttu-id="e2df5-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e2df5-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="e2df5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2df5-102">SYNOPSIS</span></span>
<span data-ttu-id="e2df5-103">정책 할당에 대한 정책 수정을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="e2df5-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2df5-104">SYNTAX</span></span>

### <span data-ttu-id="e2df5-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2df5-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2df5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2df5-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2df5-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2df5-107">DESCRIPTION</span></span>
<span data-ttu-id="e2df5-108">**Start-AzPolicyRemediation** cmdlet은 특정 정책 할당에 대한 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="e2df5-109">수정 범위 또는 아래에 있는 모든 비준수 리소스가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="e2df5-110">수정은 'deployIfNotExists' 효과가 있는 정책에만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="e2df5-111">예제</span><span class="sxs-lookup"><span data-stu-id="e2df5-111">EXAMPLES</span></span>

### <span data-ttu-id="e2df5-112">예제 1: 구독 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="e2df5-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="e2df5-113">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="e2df5-114">예제 2: 선택적 필터를 사용하여 관리 그룹 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="e2df5-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="e2df5-115">이 명령은 주어진 정책 할당에 대한 관리 그룹 'mg1'에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="e2df5-116">'westus' 또는 'eastus' 위치에 있는 리소스만 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="e2df5-117">예제 3: 정책 집합 정의 할당에 대한 리소스 그룹 범위에서 수정 시작</span><span class="sxs-lookup"><span data-stu-id="e2df5-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="e2df5-118">이 명령은 주어진 정책 할당에 대한 리소스 그룹 'myRG'에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="e2df5-119">정책 할당은 정책 집합 정의(이니셔티브라고도 합니다)를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="e2df5-120">정책 정의 참조 ID는 이니셔티브 내에서 수정해야 하는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="e2df5-121">예제 4: 수정을 시작하고 백그라운드에서 완료될 때까지 기다림</span><span class="sxs-lookup"><span data-stu-id="e2df5-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="e2df5-122">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에서 새 정책 수정을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="e2df5-123">최종 수정 상태를 반환하기 전에 수정이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="e2df5-124">예제 5: 수정하기 전에 비준수 리소스를 검색하는 수정 시작</span><span class="sxs-lookup"><span data-stu-id="e2df5-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="e2df5-125">이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="e2df5-126">구독의 리소스의 규정 준수 상태를 정책 할당에 대해 다시 평가하고 비준수 리소스가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="e2df5-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2df5-127">PARAMETERS</span></span>

### <span data-ttu-id="e2df5-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2df5-128">-AsJob</span></span>
<span data-ttu-id="e2df5-129">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e2df5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2df5-130">-DefaultProfile</span></span>
<span data-ttu-id="e2df5-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2df5-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="e2df5-132">-LocationFilter</span></span>
<span data-ttu-id="e2df5-133">수정에 포함해야 하는 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="e2df5-134">이러한 위치에 있지 않은 리소스는 수정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="e2df5-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e2df5-135">-ManagementGroupName</span></span>
<span data-ttu-id="e2df5-136">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-136">Management group ID.</span></span>

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

### <span data-ttu-id="e2df5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e2df5-137">-Name</span></span>
<span data-ttu-id="e2df5-138">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-138">Resource name.</span></span>

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

### <span data-ttu-id="e2df5-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="e2df5-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="e2df5-140">정책 할당 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-140">Policy assignment ID.</span></span>
<span data-ttu-id="e2df5-141">예:</span><span class="sxs-lookup"><span data-stu-id="e2df5-141">E.g.</span></span>
<span data-ttu-id="e2df5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="e2df5-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="e2df5-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="e2df5-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="e2df5-144">수정되는 개별 정의의 정책 정의 참조 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="e2df5-145">정책 할당이 정책 집합 정의를 할당할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="e2df5-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="e2df5-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="e2df5-147">수정 작업이 수정해야 하는 리소스를 검색하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="e2df5-148">관리 그룹 범위를 수정하는 경우 ReEvaluateCompliance는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="e2df5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2df5-149">-ResourceGroupName</span></span>
<span data-ttu-id="e2df5-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-150">Resource group name.</span></span>

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

### <span data-ttu-id="e2df5-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2df5-151">-ResourceId</span></span>
<span data-ttu-id="e2df5-152">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-152">Resource ID.</span></span>

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

### <span data-ttu-id="e2df5-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="e2df5-153">-Scope</span></span>
<span data-ttu-id="e2df5-154">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-154">Scope of the resource.</span></span>
<span data-ttu-id="e2df5-155">예:</span><span class="sxs-lookup"><span data-stu-id="e2df5-155">E.g.</span></span>
<span data-ttu-id="e2df5-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="e2df5-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="e2df5-157">-확인</span><span class="sxs-lookup"><span data-stu-id="e2df5-157">-Confirm</span></span>
<span data-ttu-id="e2df5-158">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2df5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2df5-159">-WhatIf</span></span>
<span data-ttu-id="e2df5-160">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2df5-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2df5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2df5-162">CommonParameters</span></span>
<span data-ttu-id="e2df5-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2df5-164">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2df5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2df5-165">입력</span><span class="sxs-lookup"><span data-stu-id="e2df5-165">INPUTS</span></span>

### <span data-ttu-id="e2df5-166">System.String</span><span class="sxs-lookup"><span data-stu-id="e2df5-166">System.String</span></span>

### <span data-ttu-id="e2df5-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e2df5-167">System.String[]</span></span>

## <span data-ttu-id="e2df5-168">출력</span><span class="sxs-lookup"><span data-stu-id="e2df5-168">OUTPUTS</span></span>

### <span data-ttu-id="e2df5-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="e2df5-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="e2df5-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2df5-170">NOTES</span></span>

## <span data-ttu-id="e2df5-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2df5-171">RELATED LINKS</span></span>
