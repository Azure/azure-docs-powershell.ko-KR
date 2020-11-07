---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1fc81657b5e5be03daf191a1787ad342512d266e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699412"
---
# <span data-ttu-id="7031d-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7031d-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="7031d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7031d-102">SYNOPSIS</span></span>
<span data-ttu-id="7031d-103">지정 된 범위에서 Azure RBAC 역할 할당이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="7031d-104">기본적으로 선택한 Azure 구독에 모든 역할 할당이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="7031d-105">해당 매개 변수를 사용 하 여 특정 사용자에 게 과제를 나열 하거나 특정 자원 그룹 또는 자원에 대 한 배정을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="7031d-106">구문과</span><span class="sxs-lookup"><span data-stu-id="7031d-106">SYNTAX</span></span>

### <span data-ttu-id="7031d-107">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7031d-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7031d-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="7031d-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7031d-124">설명은</span><span class="sxs-lookup"><span data-stu-id="7031d-124">DESCRIPTION</span></span>
<span data-ttu-id="7031d-125">Get-AzRoleAssignment 명령을 사용 하 여 범위에 적용 되는 모든 역할 과제를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="7031d-126">매개 변수 없이이 명령은 구독에서 생성 된 모든 역할 과제를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="7031d-127">이 목록은 주도자, 역할 및 범위에 대 한 필터링 매개 변수를 사용 하 여 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="7031d-128">과제의 주제를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7031d-129">사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7031d-130">보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7031d-131">Azure AD 응용 프로그램을 지정 하려면 ServicePrincipalName 또는 ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="7031d-132">RoleDefinitionName 매개 변수를 사용 하 여 할당 되는 역할을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="7031d-133">액세스가 허용 되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="7031d-134">선택한 구독이 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="7031d-135">다음 매개 변수 조합 a 중 하나를 사용 하 여 할당 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="7031d-136">Scope-/subscriptions/subscriptionId부터 시작 하는 정규화 된 범위 \< 입니다 \> .</span><span class="sxs-lookup"><span data-stu-id="7031d-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="7031d-137">이렇게 하면 특정 범위 (예: 해당 범위에 있는 모든 과제)에 적용 되는 배정을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="7031d-138">b.</span><span class="sxs-lookup"><span data-stu-id="7031d-138">b.</span></span>
<span data-ttu-id="7031d-139">ResourceGroupName-구독에 있는 모든 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="7031d-140">지정 된 리소스 그룹 c에서 유효 하 게 배정을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="7031d-141">Context.resourcename, ResourceType, ResourceGroupName 및 (선택적) ParentResource-구독에서 특정 리소스를 식별 하 고 해당 리소스 범위에서 효과적인 배정을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="7031d-142">특정 사용자의 구독에 대 한 액세스 권한을 확인 하려면 ExpandPrincipalGroups 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="7031d-143">이렇게 하면 사용자에 게 할당 된 모든 역할과 사용자가 구성원으로 속해 있는 그룹이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="7031d-144">IncludeClassicAdministrators 스위치를 사용 하 여 구독 관리자와 공동 관리자도 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="7031d-145">예제의</span><span class="sxs-lookup"><span data-stu-id="7031d-145">EXAMPLES</span></span>

### <span data-ttu-id="7031d-146">예제 1</span><span class="sxs-lookup"><span data-stu-id="7031d-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="7031d-147">구독에 모든 역할 할당 나열</span><span class="sxs-lookup"><span data-stu-id="7031d-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="7031d-148">예제 2</span><span class="sxs-lookup"><span data-stu-id="7031d-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="7031d-149">TestRG 범위 이상에서 사용자에 게 할당 된 모든 역할 할당과 john.doe@contoso.com 멤버가 속한 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="7031d-150">예제 3</span><span class="sxs-lookup"><span data-stu-id="7031d-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="7031d-151">지정 된 서비스 사용자의 모든 역할 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="7031d-152">예제 4</span><span class="sxs-lookup"><span data-stu-id="7031d-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="7031d-153">' Site1 ' 웹 사이트 범위에서 역할 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="7031d-154">변수</span><span class="sxs-lookup"><span data-stu-id="7031d-154">PARAMETERS</span></span>

### <span data-ttu-id="7031d-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7031d-155">-DefaultProfile</span></span>
<span data-ttu-id="7031d-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7031d-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7031d-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="7031d-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="7031d-158">지정 하는 경우 사용자에 게 직접 할당 된 역할을 반환 하 고 사용자가 구성원으로 속해 있는 그룹 (전이적)으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="7031d-159">사용자 보안 주체에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="7031d-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="7031d-161">지정 되는 경우, 구독 클래식 관리자 (공동 관리자, 서비스 관리자 등) 역할 지정도 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7031d-162">-ObjectId</span></span>
<span data-ttu-id="7031d-163">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="7031d-164">지정 된 계정에 대 한 모든 과제를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="7031d-165">-ParentResource</span></span>
<span data-ttu-id="7031d-166">Context.resourcename 매개 변수를 사용 하 여 지정 된 리소스의 계층 구조에 있는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="7031d-167">ResourceGroupName, ResourceType 및 Context.resourcename 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7031d-168">-ResourceGroupName</span></span>
<span data-ttu-id="7031d-169">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-169">The resource group name.</span></span>
<span data-ttu-id="7031d-170">지정 된 리소스 그룹에 적용 되는 역할 지정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="7031d-171">Context.resourcename, ResourceType, ParentResource 매개 변수와 함께 사용 하는 경우 명령에 리소스 그룹 내의 리소스에 대 한 실제 배정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-172">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="7031d-172">-ResourceName</span></span>
<span data-ttu-id="7031d-173">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-173">The resource name.</span></span>
<span data-ttu-id="7031d-174">예를 들어 storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="7031d-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="7031d-175">ResourceGroupName, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7031d-176">-ResourceType</span></span>
<span data-ttu-id="7031d-177">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-177">The resource type.</span></span>
<span data-ttu-id="7031d-178">예를 들어 Microsoft. p r o m/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="7031d-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="7031d-179">ResourceGroupName, Context.resourcename 및 (선택적) ParentResource 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7031d-180">-RoleDefinitionId</span></span>
<span data-ttu-id="7031d-181">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="7031d-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7031d-182">-RoleDefinitionName</span></span>
<span data-ttu-id="7031d-183">사용자에 게 할당 되는 역할입니다 (예: 독자, 참가자, 가상 네트워크 관리자 등).</span><span class="sxs-lookup"><span data-stu-id="7031d-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-184">-범위</span><span class="sxs-lookup"><span data-stu-id="7031d-184">-Scope</span></span>
<span data-ttu-id="7031d-185">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="7031d-186">상대 URI 형식</span><span class="sxs-lookup"><span data-stu-id="7031d-186">In the format of relative URI.</span></span>
<span data-ttu-id="7031d-187">예를 들어/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="7031d-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="7031d-188">"/Subscriptions/{id}"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="7031d-189">이 명령은 해당 범위에서 유효한 모든 과제를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7031d-190">-ServicePrincipalName</span></span>
<span data-ttu-id="7031d-191">서비스 사용자의 ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="7031d-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="7031d-192">지정 된 Azure AD 응용 프로그램에 대 한 모든 과제를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7031d-193">-SignInName</span></span>
<span data-ttu-id="7031d-194">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="7031d-195">지정 된 사용자에 대 한 모든 과제를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7031d-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7031d-196">CommonParameters</span></span>
<span data-ttu-id="7031d-197">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7031d-198">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7031d-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7031d-199">입력</span><span class="sxs-lookup"><span data-stu-id="7031d-199">INPUTS</span></span>

### <span data-ttu-id="7031d-200">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7031d-200">System.String</span></span>

### <span data-ttu-id="7031d-201">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="7031d-201">System.Guid</span></span>

## <span data-ttu-id="7031d-202">출력</span><span class="sxs-lookup"><span data-stu-id="7031d-202">OUTPUTS</span></span>

### <span data-ttu-id="7031d-203">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7031d-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="7031d-204">상속자</span><span class="sxs-lookup"><span data-stu-id="7031d-204">NOTES</span></span>
<span data-ttu-id="7031d-205">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="7031d-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7031d-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7031d-206">RELATED LINKS</span></span>

[<span data-ttu-id="7031d-207">새로운 AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7031d-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="7031d-208">제거-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7031d-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="7031d-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7031d-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

