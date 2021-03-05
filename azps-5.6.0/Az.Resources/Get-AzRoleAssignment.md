---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: dd59b49ad4002d38cd9a49506cb1723b5ac1e426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997360"
---
# <span data-ttu-id="e6b08-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e6b08-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="e6b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b08-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b08-103">지정된 범위에서 Azure RBAC 역할 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="e6b08-104">기본적으로 선택한 Azure 구독의 모든 역할 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="e6b08-105">각 매개 변수를 사용하여 특정 사용자에게 할당을 나열하거나 특정 리소스 그룹 또는 리소스에 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="e6b08-106">구문</span><span class="sxs-lookup"><span data-stu-id="e6b08-106">SYNTAX</span></span>

### <span data-ttu-id="e6b08-107">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6b08-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b08-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b08-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b08-124">설명</span><span class="sxs-lookup"><span data-stu-id="e6b08-124">DESCRIPTION</span></span>
<span data-ttu-id="e6b08-125">명령 Get-AzRoleAssignment 범위에 효과적인 모든 역할 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="e6b08-126">매개 변수가 없는 경우 이 명령은 구독에서 수행한 모든 역할 할당을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="e6b08-127">이 목록은 주체, 역할 및 범위에 대한 필터링 매개 변수를 사용하여 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="e6b08-128">과제의 제목을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="e6b08-129">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e6b08-130">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e6b08-131">Azure AD 애플리케이션을 지정하기 위해 ServicePrincipalName 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="e6b08-132">할당되는 역할은 RoleDefinitionName 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="e6b08-133">액세스가 부여되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="e6b08-134">기본값은 선택한 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="e6b08-135">할당의 범위를 다음 매개 변수 조합 a 중 하나를 사용하여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="e6b08-136">범위 - /subscriptions/로 시작하는 완전히 자격이 있는 \<subscriptionId\> 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="e6b08-137">이렇게 하면 해당 특정 범위(예: 해당 범위 이상의 모든 할당)에서 효과적인 할당을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="e6b08-138">b.</span><span class="sxs-lookup"><span data-stu-id="e6b08-138">b.</span></span>
<span data-ttu-id="e6b08-139">ResourceGroupName - 구독 아래 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="e6b08-140">이렇게 하면 지정된 리소스 그룹 c에서 효과적으로 할당을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="e6b08-141">ResourceName, ResourceType, ResourceGroupName 및 (선택 사항) ParentResource - 구독에서 특정 리소스를 식별하고 해당 리소스 범위에서 효과적으로 할당을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="e6b08-142">구독에서 특정 사용자가 어떤 액세스 권한을 가르는지 확인하려면 ExpandPrincipalGroups 스위치를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="e6b08-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="e6b08-143">그러면 사용자 및 사용자가 구성원인 그룹에 할당된 모든 역할이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="e6b08-144">IncludeClassicAdministrators 스위치를 사용하여 구독 관리자 및 공동 관리자도 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="e6b08-145">예제</span><span class="sxs-lookup"><span data-stu-id="e6b08-145">EXAMPLES</span></span>

### <span data-ttu-id="e6b08-146">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6b08-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="e6b08-147">구독의 모든 역할 할당 나열</span><span class="sxs-lookup"><span data-stu-id="e6b08-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="e6b08-148">예제 2</span><span class="sxs-lookup"><span data-stu-id="e6b08-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="e6b08-149">테스트RG 범위 이상에서 사용자 및 해당 사용자가 구성원인 그룹에 대해 수행된 모든 john.doe@contoso.com 역할 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="e6b08-150">예제 3</span><span class="sxs-lookup"><span data-stu-id="e6b08-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="e6b08-151">지정된 서비스 주체의 모든 역할 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="e6b08-152">예제 4</span><span class="sxs-lookup"><span data-stu-id="e6b08-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="e6b08-153">'site1' 웹 사이트 범위에서 역할 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="e6b08-154">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6b08-154">PARAMETERS</span></span>

### <span data-ttu-id="e6b08-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b08-155">-DefaultProfile</span></span>
<span data-ttu-id="e6b08-156">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6b08-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6b08-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e6b08-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="e6b08-158">지정된 경우 사용자와 사용자가 멤버인 그룹에 직접 할당된 역할을 반환합니다(전이적으로).</span><span class="sxs-lookup"><span data-stu-id="e6b08-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="e6b08-159">사용자 주체에만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="e6b08-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="e6b08-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="e6b08-161">지정한 경우 구독 클래식 관리자(공동 관리자, 서비스 관리자 등) 역할 할당도 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="e6b08-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e6b08-162">-ObjectId</span></span>
<span data-ttu-id="e6b08-163">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="e6b08-164">지정된 주체에 대해 수행된 모든 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="e6b08-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e6b08-165">-ParentResource</span></span>
<span data-ttu-id="e6b08-166">ResourceName 매개 변수를 사용하여 지정된 리소스의 계층 구조의 상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="e6b08-167">ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="e6b08-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b08-168">-ResourceGroupName</span></span>
<span data-ttu-id="e6b08-169">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-169">The resource group name.</span></span>
<span data-ttu-id="e6b08-170">지정된 리소스 그룹에 효과적인 역할 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="e6b08-171">ResourceName, ResourceType 및 ParentResource 매개 변수와 함께 사용하는 경우 명령은 리소스 그룹 내의 리소스에서 효과적인 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="e6b08-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e6b08-172">-ResourceName</span></span>
<span data-ttu-id="e6b08-173">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-173">The resource name.</span></span>
<span data-ttu-id="e6b08-174">예: storageaccountprod의 경우.</span><span class="sxs-lookup"><span data-stu-id="e6b08-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="e6b08-175">ResourceGroupName, ResourceType 및 (선택 사항)ParentResource 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e6b08-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e6b08-176">-ResourceType</span></span>
<span data-ttu-id="e6b08-177">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-177">The resource type.</span></span>
<span data-ttu-id="e6b08-178">예: Microsoft.Network/virtualNetworks입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="e6b08-179">ResourceGroupName, ResourceName 및 (선택 사항)ParentResource 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e6b08-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e6b08-180">-RoleDefinitionId</span></span>
<span data-ttu-id="e6b08-181">주체에 할당된 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="e6b08-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e6b08-182">-RoleDefinitionName</span></span>
<span data-ttu-id="e6b08-183">주체(예: Reader, 참가자, 가상 네트워크 관리자 등)에 할당된 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="e6b08-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="e6b08-184">-Scope</span></span>
<span data-ttu-id="e6b08-185">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="e6b08-186">상대 URI 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-186">In the format of relative URI.</span></span>
<span data-ttu-id="e6b08-187">예: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="e6b08-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="e6b08-188">"/subscriptions/{id}"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="e6b08-189">이 명령은 해당 범위에서 효과적인 모든 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="e6b08-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e6b08-190">-ServicePrincipalName</span></span>
<span data-ttu-id="e6b08-191">서비스 주체의 ServicePrincipalName입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="e6b08-192">지정된 Azure AD 애플리케이션에 대해 수행된 모든 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="e6b08-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e6b08-193">-SignInName</span></span>
<span data-ttu-id="e6b08-194">사용자의 전자 메일 주소 또는 사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="e6b08-195">지정된 사용자에게 수행된 모든 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="e6b08-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b08-196">CommonParameters</span></span>
<span data-ttu-id="e6b08-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b08-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b08-198">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6b08-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b08-199">입력</span><span class="sxs-lookup"><span data-stu-id="e6b08-199">INPUTS</span></span>

### <span data-ttu-id="e6b08-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e6b08-200">System.String</span></span>

### <span data-ttu-id="e6b08-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e6b08-201">System.Guid</span></span>

## <span data-ttu-id="e6b08-202">출력</span><span class="sxs-lookup"><span data-stu-id="e6b08-202">OUTPUTS</span></span>

### <span data-ttu-id="e6b08-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e6b08-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="e6b08-204">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6b08-204">NOTES</span></span>
<span data-ttu-id="e6b08-205">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="e6b08-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e6b08-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6b08-206">RELATED LINKS</span></span>

[<span data-ttu-id="e6b08-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e6b08-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="e6b08-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e6b08-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="e6b08-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e6b08-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

