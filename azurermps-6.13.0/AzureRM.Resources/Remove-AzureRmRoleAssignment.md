---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 706ba111fb015c8865a33a9beec4fe3e722718ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528403"
---
# <span data-ttu-id="fdb2e-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fdb2e-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="fdb2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb2e-103">특정 범위에서 특정 역할에 할당 된 지정 된 주체에 대 한 역할 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdb2e-104">SYNTAX</span></span>

### <span data-ttu-id="fdb2e-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fdb2e-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb2e-117">설명은</span><span class="sxs-lookup"><span data-stu-id="fdb2e-117">DESCRIPTION</span></span>
<span data-ttu-id="fdb2e-118">Remove-AzureRmRoleAssignment를 사용 하 여 지정 된 범위에 있는 모든 주체에 대 한 액세스를 취소 하 고 역할을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="fdb2e-119">과제의 개체 즉, 주체를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="fdb2e-120">Principal은 사용자 (SignInName 또는 ObjectId 매개 변수를 사용 하 여 사용자 식별), 보안 그룹 (그룹을 식별 하는 데 ObjectId 매개 변수 사용) 또는 서비스 주체 (ServicePrincipalName 또는 ObjectId 매개 변수를 사용 하 여 ServicePrincipal을 식별 합니다.)가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="fdb2e-121">RoleDefinitionName 매개 변수를 사용 하 여 principal이 할당 된 역할을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="fdb2e-122">할당 범위를 지정 하 고 지정 하지 않으면 기본적으로 구독 범위 (즉, 구독 범위에서 지정 된 사용자 및 역할에 대 한 할당을 삭제 하려고 함)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="fdb2e-123">할당 범위는 다음 매개 변수 중 하나를 사용 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="fdb2e-124">에서.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-124">a.</span></span>
<span data-ttu-id="fdb2e-125">Scope-/subscriptions/b로 시작 하는 정규화 된 범위입니다 \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="fdb2e-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="fdb2e-126">ResourceGroupName-구독에 있는 모든 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="fdb2e-127">c.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-127">c.</span></span>
<span data-ttu-id="fdb2e-128">Context.resourcename, ResourceType, ResourceGroupName 및 (선택적) ParentResource-구독에서 특정 리소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="fdb2e-129">예제의</span><span class="sxs-lookup"><span data-stu-id="fdb2e-129">EXAMPLES</span></span>

### <span data-ttu-id="fdb2e-130">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdb2e-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="fdb2e-131">john.doe@contoso.comRg1 resourcegroup 범위에서 독자 역할에 할당 된 사용자에 대 한 역할 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="fdb2e-132">예제 2</span><span class="sxs-lookup"><span data-stu-id="fdb2e-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="fdb2e-133">ObjectId로 식별 되 고 독자 역할에 할당 된 그룹 주체에 대 한 역할 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="fdb2e-134">삭제할 과제를 찾을 범위로 현재 구독을 사용 하도록 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="fdb2e-135">예제 3</span><span class="sxs-lookup"><span data-stu-id="fdb2e-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="fdb2e-136">Get-AzureRmRoleAssignment 이상에서 가져온 첫 번째 역할 할당 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="fdb2e-137">변수</span><span class="sxs-lookup"><span data-stu-id="fdb2e-137">PARAMETERS</span></span>

### <span data-ttu-id="fdb2e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb2e-138">-DefaultProfile</span></span>
<span data-ttu-id="fdb2e-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fdb2e-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdb2e-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb2e-140">-InputObject</span></span>
<span data-ttu-id="fdb2e-141">역할 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fdb2e-142">-ObjectId</span></span>
<span data-ttu-id="fdb2e-143">사용자, 그룹 또는 서비스 사용자의 Azure AD ObjectId</span><span class="sxs-lookup"><span data-stu-id="fdb2e-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="fdb2e-144">-ParentResource</span></span>
<span data-ttu-id="fdb2e-145">계층 구조의 상위 리소스 (예를 들어, Context.resourcename 매개 변수를 사용 하 여 지정 된 리소스)입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="fdb2e-146">ResourceGroupName, ResourceType 및 Context.resourcename 매개 변수와 함께 사용 하 여 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdb2e-147">-PassThru</span></span>
<span data-ttu-id="fdb2e-148">지정 된 경우 삭제 된 역할 과제를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="fdb2e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-149">-ResourceGroupName</span></span>
<span data-ttu-id="fdb2e-150">역할이 할당 된 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="fdb2e-151">지정 된 리소스 그룹 범위에서 과제를 삭제 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="fdb2e-152">Context.resourcename, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 하는 경우이 명령은 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-153">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="fdb2e-153">-ResourceName</span></span>
<span data-ttu-id="fdb2e-154">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-154">The resource name.</span></span>
<span data-ttu-id="fdb2e-155">예를 들어 storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="fdb2e-156">ResourceGroupName, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 하 여 리소스를 식별 하 고 해당 범위에서 과제를 삭제 하는 상대 URI 형식으로 계층적 범위를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fdb2e-157">-ResourceType</span></span>
<span data-ttu-id="fdb2e-158">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-158">The resource type.</span></span>
<span data-ttu-id="fdb2e-159">예를 들어 Microsoft. p r o m/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="fdb2e-160">ResourceGroupName, Context.resourcename 및 (선택적) ParentResource 매개 변수와 함께 사용 하 여 리소스를 식별 하 고 해당 리소스 범위에서 과제를 삭제 하는 상대 URI 형식으로 계층적 범위를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fdb2e-161">-RoleDefinitionId</span></span>
<span data-ttu-id="fdb2e-162">과제를 삭제 해야 하는 RBAC 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-163">-RoleDefinitionName</span></span>
<span data-ttu-id="fdb2e-164">과제물을 삭제 해야 하는 RBAC 역할의 이름입니다 (예: 독자, 참가자, 가상 네트워크 관리자 등).</span><span class="sxs-lookup"><span data-stu-id="fdb2e-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-165">-범위</span><span class="sxs-lookup"><span data-stu-id="fdb2e-165">-Scope</span></span>
<span data-ttu-id="fdb2e-166">삭제할 역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="fdb2e-167">상대 URI 형식</span><span class="sxs-lookup"><span data-stu-id="fdb2e-167">In the format of relative URI.</span></span>
<span data-ttu-id="fdb2e-168">예를 들어 "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="fdb2e-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="fdb2e-169">지정 하지 않으면 구독 수준에서 역할을 삭제 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="fdb2e-170">지정 된 경우 "/subscriptions/{id}"으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-171">-ServicePrincipalName</span></span>
<span data-ttu-id="fdb2e-172">Azure AD 응용 프로그램의 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-173">-SignInName</span></span>
<span data-ttu-id="fdb2e-174">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb2e-175">-확인</span><span class="sxs-lookup"><span data-stu-id="fdb2e-175">-Confirm</span></span>
<span data-ttu-id="fdb2e-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb2e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb2e-177">-WhatIf</span></span>
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

### <span data-ttu-id="fdb2e-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb2e-178">CommonParameters</span></span>
<span data-ttu-id="fdb2e-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb2e-180">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb2e-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb2e-181">입력</span><span class="sxs-lookup"><span data-stu-id="fdb2e-181">INPUTS</span></span>

### <span data-ttu-id="fdb2e-182">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="fdb2e-182">System.Guid</span></span>

### <span data-ttu-id="fdb2e-183">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdb2e-183">System.String</span></span>

### <span data-ttu-id="fdb2e-184">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="fdb2e-185">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdb2e-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fdb2e-186">출력</span><span class="sxs-lookup"><span data-stu-id="fdb2e-186">OUTPUTS</span></span>

### <span data-ttu-id="fdb2e-187">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb2e-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="fdb2e-188">상속자</span><span class="sxs-lookup"><span data-stu-id="fdb2e-188">NOTES</span></span>
<span data-ttu-id="fdb2e-189">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="fdb2e-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="fdb2e-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdb2e-190">RELATED LINKS</span></span>

[<span data-ttu-id="fdb2e-191">새로운 AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fdb2e-191">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="fdb2e-192">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fdb2e-192">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="fdb2e-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fdb2e-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

