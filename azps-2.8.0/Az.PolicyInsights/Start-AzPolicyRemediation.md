---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: df7b0803952a7a972d2c68ef2d8e7ec61d42c5e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872310"
---
# <span data-ttu-id="d6f73-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d6f73-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="d6f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f73-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f73-103">정책 할당에 대 한 정책 수정을 만들고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="d6f73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6f73-104">SYNTAX</span></span>

### <span data-ttu-id="d6f73-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6f73-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6f73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f73-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d6f73-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f73-108">**AzPolicyRemediation** cmdlet은 특정 정책 할당에 대 한 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="d6f73-109">업데이트 관리 범위 또는 그 아래에 있는 모든 비규격 리소스는 재구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="d6f73-110">업데이트 관리는 ' deployIfNotExists ' 효과가 있는 정책에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="d6f73-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d6f73-111">EXAMPLES</span></span>

### <span data-ttu-id="d6f73-112">예제 1: 구독 범위에서 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="d6f73-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="d6f73-113">이 명령은 지정 된 정책 할당에 대 한 ' My 구독 ' 구독에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="d6f73-114">예제 2: 관리 그룹 범위에서 선택적 필터를 사용 하 여 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="d6f73-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="d6f73-115">이 명령은 지정 된 정책 할당에 대 한 관리 그룹 ' mg1 '에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="d6f73-116">' Westus ' 또는 ' e us ' 위치의 리소스만 재구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="d6f73-117">예제 3: 정책 집합 정의 할당에 대 한 리소스 그룹 범위에서 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="d6f73-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="d6f73-118">이 명령은 지정 된 정책 할당에 대 한 리소스 그룹 ' myRG '에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="d6f73-119">정책 할당은 정책 집합 정의 (이니셔티브 라고도 함)를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="d6f73-120">정책 정의 참조 ID는 이니셔티브에서 재구성 해야 하는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="d6f73-121">예제 4: 수정을 시작 하 고 백그라운드에서 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="d6f73-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="d6f73-122">이 명령은 지정 된 정책 할당에 대 한 ' My 구독 ' 구독에서 새 정책 수정을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d6f73-123">마지막 업데이트 관리 상태를 반환 하기 전에 업데이트 관리가 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="d6f73-124">변수</span><span class="sxs-lookup"><span data-stu-id="d6f73-124">PARAMETERS</span></span>

### <span data-ttu-id="d6f73-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f73-125">-AsJob</span></span>
<span data-ttu-id="d6f73-126">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d6f73-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f73-127">-DefaultProfile</span></span>
<span data-ttu-id="d6f73-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f73-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="d6f73-129">-LocationFilter</span></span>
<span data-ttu-id="d6f73-130">업데이트 관리에 포함 해야 하는 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="d6f73-131">이러한 위치에 존재 하지 않는 리소스는 재구성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="d6f73-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f73-132">-ManagementGroupName</span></span>
<span data-ttu-id="d6f73-133">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-133">Management group ID.</span></span>

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

### <span data-ttu-id="d6f73-134">-이름</span><span class="sxs-lookup"><span data-stu-id="d6f73-134">-Name</span></span>
<span data-ttu-id="d6f73-135">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-135">Resource name.</span></span>

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

### <span data-ttu-id="d6f73-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d6f73-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="d6f73-137">정책 할당 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-137">Policy assignment ID.</span></span>
<span data-ttu-id="d6f73-138">즉.</span><span class="sxs-lookup"><span data-stu-id="d6f73-138">E.g.</span></span>
<span data-ttu-id="d6f73-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="d6f73-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="d6f73-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d6f73-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="d6f73-141">재구성 되는 개별 정의의 정책 정의 참조 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="d6f73-142">정책 할당이 정책 집합 정의를 할당할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="d6f73-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f73-143">-ResourceGroupName</span></span>
<span data-ttu-id="d6f73-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-144">Resource group name.</span></span>

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

### <span data-ttu-id="d6f73-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f73-145">-ResourceId</span></span>
<span data-ttu-id="d6f73-146">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-146">Resource ID.</span></span>

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

### <span data-ttu-id="d6f73-147">-범위</span><span class="sxs-lookup"><span data-stu-id="d6f73-147">-Scope</span></span>
<span data-ttu-id="d6f73-148">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-148">Scope of the resource.</span></span>
<span data-ttu-id="d6f73-149">즉.</span><span class="sxs-lookup"><span data-stu-id="d6f73-149">E.g.</span></span>
<span data-ttu-id="d6f73-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d6f73-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d6f73-151">-확인</span><span class="sxs-lookup"><span data-stu-id="d6f73-151">-Confirm</span></span>
<span data-ttu-id="d6f73-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f73-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f73-153">-WhatIf</span></span>
<span data-ttu-id="d6f73-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f73-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f73-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f73-156">CommonParameters</span></span>
<span data-ttu-id="d6f73-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f73-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f73-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f73-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f73-159">입력</span><span class="sxs-lookup"><span data-stu-id="d6f73-159">INPUTS</span></span>

### <span data-ttu-id="d6f73-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6f73-160">System.String</span></span>

### <span data-ttu-id="d6f73-161">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="d6f73-161">System.String[]</span></span>

## <span data-ttu-id="d6f73-162">출력</span><span class="sxs-lookup"><span data-stu-id="d6f73-162">OUTPUTS</span></span>

### <span data-ttu-id="d6f73-163">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d6f73-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d6f73-164">상속자</span><span class="sxs-lookup"><span data-stu-id="d6f73-164">NOTES</span></span>

## <span data-ttu-id="d6f73-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6f73-165">RELATED LINKS</span></span>
