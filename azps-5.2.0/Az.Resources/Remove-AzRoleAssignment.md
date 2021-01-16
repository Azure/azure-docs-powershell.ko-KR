---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351806"
---
# <span data-ttu-id="37083-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37083-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="37083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37083-102">SYNOPSIS</span></span>
<span data-ttu-id="37083-103">특정 범위에서 특정 역할에 할당된 지정된 보안 주체에 대한 역할 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="37083-104">구문</span><span class="sxs-lookup"><span data-stu-id="37083-104">SYNTAX</span></span>

### <span data-ttu-id="37083-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="37083-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37083-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="37083-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37083-117">설명</span><span class="sxs-lookup"><span data-stu-id="37083-117">DESCRIPTION</span></span>
<span data-ttu-id="37083-118">이 Remove-AzRoleAssignment 명령줄을 사용하여 주어진 범위 및 주어진 역할의 모든 보안 주체에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="37083-119">할당의 개체입니다. 예: 보안 주체는 반드시 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="37083-120">보안 주체는 사용자(SignInName 또는 ObjectId 매개 변수를 사용하여 사용자 식별), 보안 그룹(ObjectId 매개 변수를 사용하여 그룹 식별) 또는 서비스 주체(ServicePrincipalName 또는 ObjectId 매개 변수를 사용하여 ServicePrincipal 식별)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37083-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="37083-121">RoleDefinitionName 매개 변수를 사용하여 보안 주체에 할당된 역할을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="37083-122">할당의 범위를 지정할 수 있으며, 지정하지 않으면 기본적으로 구독 범위로 설정됩니다. 구독 범위에서 지정된 보안 주체 및 역할에 대한 할당을 삭제하려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="37083-123">다음 매개 변수 중 하나를 사용하여 할당 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37083-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="37083-124">a.</span><span class="sxs-lookup"><span data-stu-id="37083-124">a.</span></span>
<span data-ttu-id="37083-125">범위 - /subscriptions/b로 시작하는 정식 \<subscriptionId\> 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="37083-126">ResourceGroupName - 구독에 속한 모든 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="37083-127">c.</span><span class="sxs-lookup"><span data-stu-id="37083-127">c.</span></span>
<span data-ttu-id="37083-128">ResourceName, ResourceType, ResourceGroupName 및 (선택 사항) ParentResource - 구독에서 특정 리소스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="37083-129">예제</span><span class="sxs-lookup"><span data-stu-id="37083-129">EXAMPLES</span></span>

### <span data-ttu-id="37083-130">예제 1</span><span class="sxs-lookup"><span data-stu-id="37083-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="37083-131">rg1 리소스 그룹 범위에서 읽기 역할에 할당된 사용자에 대한 역할 john.doe@contoso.com 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="37083-132">예제 2</span><span class="sxs-lookup"><span data-stu-id="37083-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="37083-133">ObjectId로 식별되어 읽기 역할에 할당된 그룹 주체에 대한 역할 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="37083-134">기본적으로 현재 구독을 범위로 사용하여 삭제할 할당을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37083-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="37083-135">예제 3</span><span class="sxs-lookup"><span data-stu-id="37083-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="37083-136">명령줄에서 페치되는 첫 번째 역할 할당 개체를 Get-AzRoleAssignment 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="37083-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37083-137">PARAMETERS</span></span>

### <span data-ttu-id="37083-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37083-138">-DefaultProfile</span></span>
<span data-ttu-id="37083-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37083-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37083-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37083-140">-InputObject</span></span>
<span data-ttu-id="37083-141">역할 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="37083-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="37083-142">-ObjectId</span></span>
<span data-ttu-id="37083-143">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37083-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="37083-144">-ParentResource</span></span>
<span data-ttu-id="37083-145">계층 구조(ResourceName 매개 변수를 사용하여 지정된 리소스)의 부모 리소스(있는 경우).</span><span class="sxs-lookup"><span data-stu-id="37083-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="37083-146">ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용하여 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="37083-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37083-147">-PassThru</span></span>
<span data-ttu-id="37083-148">지정된 경우 삭제된 역할 할당을 표시</span><span class="sxs-lookup"><span data-stu-id="37083-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="37083-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37083-149">-ResourceGroupName</span></span>
<span data-ttu-id="37083-150">역할이 할당된 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="37083-151">지정된 리소스 그룹 범위에서 할당을 삭제하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="37083-152">ResourceName, ResourceType 및 (선택 사항)ParentResource 매개 변수와 함께 사용되는 경우 이 명령은 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="37083-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37083-153">-ResourceName</span></span>
<span data-ttu-id="37083-154">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-154">The resource name.</span></span>
<span data-ttu-id="37083-155">예: storageaccountprod</span><span class="sxs-lookup"><span data-stu-id="37083-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="37083-156">리소스를 식별하고 해당 범위에서 할당을 삭제하는 상대 URI의 형태로 계층적 범위를 생성하려면 ResourceGroupName, ResourceType 및 (선택 사항) ParentResource 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="37083-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="37083-157">-ResourceType</span></span>
<span data-ttu-id="37083-158">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-158">The resource type.</span></span>
<span data-ttu-id="37083-159">예: Microsoft.Network/virtualNetworks</span><span class="sxs-lookup"><span data-stu-id="37083-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="37083-160">ResourceGroupName, ResourceName 및 (선택 사항) ParentResource 매개 변수와 함께 사용하여 리소스를 식별하고 해당 리소스 범위에서 할당을 삭제하는 상대 URI의 형태로 계층적 범위를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="37083-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="37083-161">-RoleDefinitionId</span></span>
<span data-ttu-id="37083-162">할당을 삭제해야 하는 RBAC 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="37083-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="37083-163">-RoleDefinitionName</span></span>
<span data-ttu-id="37083-164">할당을 삭제해야 하는 RBAC 역할의 이름(예: 읽기 권한자, 참가자, Virtual Network 관리자 등)</span><span class="sxs-lookup"><span data-stu-id="37083-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="37083-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="37083-165">-Scope</span></span>
<span data-ttu-id="37083-166">삭제할 역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="37083-167">상대 URI 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-167">In the format of relative URI.</span></span>
<span data-ttu-id="37083-168">예: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="37083-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="37083-169">지정하지 않으면 구독 수준에서 역할을 삭제하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="37083-170">지정된 경우 "/subscriptions/{id}"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="37083-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="37083-171">-ServicePrincipalName</span></span>
<span data-ttu-id="37083-172">Azure AD 애플리케이션의 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="37083-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="37083-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="37083-173">-SignInName</span></span>
<span data-ttu-id="37083-174">사용자의 이메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37083-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="37083-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37083-175">-Confirm</span></span>
<span data-ttu-id="37083-176">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37083-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37083-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37083-177">-WhatIf</span></span>
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

### <span data-ttu-id="37083-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37083-178">CommonParameters</span></span>
<span data-ttu-id="37083-179">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37083-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37083-180">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37083-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37083-181">입력</span><span class="sxs-lookup"><span data-stu-id="37083-181">INPUTS</span></span>

### <span data-ttu-id="37083-182">System.String</span><span class="sxs-lookup"><span data-stu-id="37083-182">System.String</span></span>

### <span data-ttu-id="37083-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="37083-183">System.Guid</span></span>

### <span data-ttu-id="37083-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37083-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="37083-185">출력</span><span class="sxs-lookup"><span data-stu-id="37083-185">OUTPUTS</span></span>

### <span data-ttu-id="37083-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37083-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="37083-187">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37083-187">NOTES</span></span>
<span data-ttu-id="37083-188">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="37083-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="37083-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37083-189">RELATED LINKS</span></span>

[<span data-ttu-id="37083-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37083-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="37083-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37083-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="37083-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="37083-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

