---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528458"
---
# <span data-ttu-id="63f76-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="63f76-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="63f76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f76-102">SYNOPSIS</span></span>
<span data-ttu-id="63f76-103">정책 할당에 대 한 정책 수정을 만들고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63f76-104">SYNTAX</span></span>

### <span data-ttu-id="63f76-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="63f76-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f76-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63f76-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f76-107">설명은</span><span class="sxs-lookup"><span data-stu-id="63f76-107">DESCRIPTION</span></span>
<span data-ttu-id="63f76-108">**AzureRmPolicyRemediation** cmdlet은 특정 정책 할당에 대 한 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="63f76-109">업데이트 관리 범위 또는 그 아래에 있는 모든 비규격 리소스는 재구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="63f76-110">업데이트 관리는 ' deployIfNotExists ' 효과가 있는 정책에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="63f76-111">예제의</span><span class="sxs-lookup"><span data-stu-id="63f76-111">EXAMPLES</span></span>

### <span data-ttu-id="63f76-112">예제 1: 구독 범위에서 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="63f76-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="63f76-113">이 명령은 지정 된 정책 할당에 대 한 ' My 구독 ' 구독에서 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="63f76-114">예제 2: 관리 그룹 범위에서 선택적 필터를 사용 하 여 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="63f76-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="63f76-115">이 명령은 지정 된 정책 할당에 대 한 관리 그룹 ' mg1 '에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="63f76-116">' Westus ' 또는 ' e us ' 위치의 리소스만 재구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="63f76-117">예제 3: 정책 집합 정의 할당에 대 한 리소스 그룹 범위에서 재구성 시작</span><span class="sxs-lookup"><span data-stu-id="63f76-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="63f76-118">이 명령은 지정 된 정책 할당에 대 한 리소스 그룹 ' myRG '에 새 정책 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="63f76-119">정책 할당은 정책 집합 정의 (이니셔티브 라고도 함)를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="63f76-120">정책 정의 참조 ID는 이니셔티브에서 재구성 해야 하는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="63f76-121">예제 4: 수정을 시작 하 고 백그라운드에서 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="63f76-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="63f76-122">이 명령은 지정 된 정책 할당에 대 한 ' My 구독 ' 구독에서 새 정책 수정을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="63f76-123">마지막 업데이트 관리 상태를 반환 하기 전에 업데이트 관리가 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="63f76-124">변수</span><span class="sxs-lookup"><span data-stu-id="63f76-124">PARAMETERS</span></span>

### <span data-ttu-id="63f76-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63f76-125">-AsJob</span></span>
<span data-ttu-id="63f76-126">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="63f76-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f76-127">-DefaultProfile</span></span>
<span data-ttu-id="63f76-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f76-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="63f76-129">-LocationFilter</span></span>
<span data-ttu-id="63f76-130">업데이트 관리에 포함 해야 하는 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="63f76-131">이러한 위치에 존재 하지 않는 리소스는 재구성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="63f76-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="63f76-132">-ManagementGroupName</span></span>
<span data-ttu-id="63f76-133">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-133">Management group ID.</span></span>

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

### <span data-ttu-id="63f76-134">-이름</span><span class="sxs-lookup"><span data-stu-id="63f76-134">-Name</span></span>
<span data-ttu-id="63f76-135">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-135">Resource name.</span></span>

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

### <span data-ttu-id="63f76-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="63f76-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="63f76-137">정책 할당 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-137">Policy assignment ID.</span></span>
<span data-ttu-id="63f76-138">즉.</span><span class="sxs-lookup"><span data-stu-id="63f76-138">E.g.</span></span>
<span data-ttu-id="63f76-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="63f76-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="63f76-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="63f76-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="63f76-141">재구성 되는 개별 정의의 정책 정의 참조 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="63f76-142">정책 할당이 정책 집합 정의를 할당할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="63f76-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f76-143">-ResourceGroupName</span></span>
<span data-ttu-id="63f76-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-144">Resource group name.</span></span>

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

### <span data-ttu-id="63f76-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f76-145">-ResourceId</span></span>
<span data-ttu-id="63f76-146">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-146">Resource ID.</span></span>

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

### <span data-ttu-id="63f76-147">-범위</span><span class="sxs-lookup"><span data-stu-id="63f76-147">-Scope</span></span>
<span data-ttu-id="63f76-148">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-148">Scope of the resource.</span></span>
<span data-ttu-id="63f76-149">즉.</span><span class="sxs-lookup"><span data-stu-id="63f76-149">E.g.</span></span>
<span data-ttu-id="63f76-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="63f76-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="63f76-151">-확인</span><span class="sxs-lookup"><span data-stu-id="63f76-151">-Confirm</span></span>
<span data-ttu-id="63f76-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f76-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f76-153">-WhatIf</span></span>
<span data-ttu-id="63f76-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f76-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f76-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f76-156">CommonParameters</span></span>
<span data-ttu-id="63f76-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f76-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f76-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f76-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f76-159">입력</span><span class="sxs-lookup"><span data-stu-id="63f76-159">INPUTS</span></span>

### <span data-ttu-id="63f76-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63f76-160">System.String</span></span>

### <span data-ttu-id="63f76-161">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="63f76-161">System.String[]</span></span>

## <span data-ttu-id="63f76-162">출력</span><span class="sxs-lookup"><span data-stu-id="63f76-162">OUTPUTS</span></span>

### <span data-ttu-id="63f76-163">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="63f76-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="63f76-164">상속자</span><span class="sxs-lookup"><span data-stu-id="63f76-164">NOTES</span></span>

## <span data-ttu-id="63f76-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63f76-165">RELATED LINKS</span></span>
