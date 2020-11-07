---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: d1fe464078c41d07f0d40024c06c4d5f88358470
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871793"
---
# <span data-ttu-id="6d299-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6d299-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="6d299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d299-102">SYNOPSIS</span></span>
<span data-ttu-id="6d299-103">지정 된 범위에서 지정한 RBAC 역할을 지정 된 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="6d299-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d299-104">SYNTAX</span></span>

### <span data-ttu-id="6d299-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d299-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d299-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d299-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d299-115">설명은</span><span class="sxs-lookup"><span data-stu-id="6d299-115">DESCRIPTION</span></span>
<span data-ttu-id="6d299-116">New-AzRoleAssignment 명령을 사용 하 여 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-116">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="6d299-117">올바른 범위에서 적절 한 RBAC 역할을 할당 하 여 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-117">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="6d299-118">전체 구독에 대 한 액세스 권한을 부여 하려면 구독 범위에서 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-118">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="6d299-119">구독 내의 특정 리소스 그룹에 대 한 액세스 권한을 부여 하려면 리소스 그룹 범위에서 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-119">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="6d299-120">과제의 주제를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-120">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="6d299-121">사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-121">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="6d299-122">보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-122">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="6d299-123">Azure AD 응용 프로그램을 지정 하려면 ApplicationId 또는 ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-123">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="6d299-124">RoleDefinitionName 매개 변수를 사용 하 여 할당 되는 역할을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-124">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="6d299-125">액세스가 허용 되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-125">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="6d299-126">선택한 구독이 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-126">It defaults to the selected subscription.</span></span> <span data-ttu-id="6d299-127">다음 매개 변수 조합 a 중 하나를 사용 하 여 할당 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-127">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="6d299-128">Scope-/subscriptions/subscriptionId b로 시작 하는 정규화 된 범위입니다 \< \> .</span><span class="sxs-lookup"><span data-stu-id="6d299-128">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="6d299-129">ResourceGroupName-지정 된 리소스 그룹에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-129">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="6d299-130">c.</span><span class="sxs-lookup"><span data-stu-id="6d299-130">c.</span></span>
<span data-ttu-id="6d299-131">Context.resourcename, ResourceType, ResourceGroupName 및 (선택적) ParentResource-리소스 그룹 내에서 액세스 권한을 부여할 특정 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-131">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="6d299-132">예제의</span><span class="sxs-lookup"><span data-stu-id="6d299-132">EXAMPLES</span></span>

### <span data-ttu-id="6d299-133">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d299-133">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="6d299-134">위임에 사용할 수 있는 역할 할당이 있는 리소스 그룹 범위에서 사용자에 게 읽기 프로그램 역할 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="6d299-134">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="6d299-135">예제 2</span><span class="sxs-lookup"><span data-stu-id="6d299-135">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="6d299-136">보안 그룹에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="6d299-136">Grant access to a security group</span></span>

### <span data-ttu-id="6d299-137">예제 3</span><span class="sxs-lookup"><span data-stu-id="6d299-137">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="6d299-138">리소스 (웹 사이트)에서 사용자에 게 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="6d299-138">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="6d299-139">예제 4</span><span class="sxs-lookup"><span data-stu-id="6d299-139">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="6d299-140">중첩 된 리소스 (서브넷)에 있는 그룹에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="6d299-140">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="6d299-141">예제 5</span><span class="sxs-lookup"><span data-stu-id="6d299-141">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="6d299-142">서비스 사용자에 게 읽기 프로그램에 대 한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="6d299-142">Grant reader access to a service principal</span></span>

## <span data-ttu-id="6d299-143">변수</span><span class="sxs-lookup"><span data-stu-id="6d299-143">PARAMETERS</span></span>

### <span data-ttu-id="6d299-144">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="6d299-144">-AllowDelegation</span></span>
<span data-ttu-id="6d299-145">역할 할당을 만드는 동안 위임 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-145">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-146">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6d299-146">-ApplicationId</span></span>
<span data-ttu-id="6d299-147">ServicePrincipal의 응용 프로그램 ID</span><span class="sxs-lookup"><span data-stu-id="6d299-147">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d299-148">-DefaultProfile</span></span>
<span data-ttu-id="6d299-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6d299-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d299-150">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6d299-150">-ObjectId</span></span>
<span data-ttu-id="6d299-151">사용자, 그룹 또는 서비스 사용자의 Azure AD Objectid</span><span class="sxs-lookup"><span data-stu-id="6d299-151">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-152">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="6d299-152">-ParentResource</span></span>
<span data-ttu-id="6d299-153">계층 구조의 부모 리소스 (Context.resourcename 매개 변수를 사용 하 여 지정 된 리소스)</span><span class="sxs-lookup"><span data-stu-id="6d299-153">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="6d299-154">ResourceGroupName, ResourceType 및 Context.resourcename 매개 변수와 함께 사용 해야만 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-154">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6d299-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d299-155">-ResourceGroupName</span></span>
<span data-ttu-id="6d299-156">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-156">The resource group name.</span></span>
<span data-ttu-id="6d299-157">지정 된 리소스 그룹에 적용 되는 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-157">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="6d299-158">Context.resourcename, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 하는 경우이 명령은 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-158">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-159">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="6d299-159">-ResourceName</span></span>
<span data-ttu-id="6d299-160">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-160">The resource name.</span></span>
<span data-ttu-id="6d299-161">예를 들어 storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="6d299-161">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="6d299-162">ResourceGroupName, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 해야만 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-162">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6d299-163">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6d299-163">-ResourceType</span></span>
<span data-ttu-id="6d299-164">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-164">The resource type.</span></span>
<span data-ttu-id="6d299-165">예를 들어 Microsoft. p r o m/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="6d299-165">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="6d299-166">ResourceGroupName, Context.resourcename 및 (선택적) ParentResource 매개 변수와 함께 사용 해야만 리소스를 식별 하는 상대 URI 형식으로 계층적 범위를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-166">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6d299-167">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6d299-167">-RoleDefinitionId</span></span>
<span data-ttu-id="6d299-168">주도자에 게 할당 해야 하는 RBAC 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-168">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="6d299-169">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6d299-169">-RoleDefinitionName</span></span>
<span data-ttu-id="6d299-170">사용자에 게 할당 해야 하는 RBAC 역할의 이름입니다 (예: 독자, 참가자, 가상 네트워크 관리자 등).</span><span class="sxs-lookup"><span data-stu-id="6d299-170">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-171">-범위</span><span class="sxs-lookup"><span data-stu-id="6d299-171">-Scope</span></span>
<span data-ttu-id="6d299-172">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-172">The Scope of the role assignment.</span></span>
<span data-ttu-id="6d299-173">상대 URI 형식</span><span class="sxs-lookup"><span data-stu-id="6d299-173">In the format of relative URI.</span></span>
<span data-ttu-id="6d299-174">예를 들어 "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="6d299-174">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="6d299-175">지정 하지 않으면 구독 수준에서 역할 할당이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-175">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="6d299-176">지정 된 경우 "/subscriptions/{id}"으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-176">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-177">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6d299-177">-SignInName</span></span>
<span data-ttu-id="6d299-178">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-178">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d299-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d299-179">CommonParameters</span></span>
<span data-ttu-id="6d299-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d299-181">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d299-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d299-182">입력</span><span class="sxs-lookup"><span data-stu-id="6d299-182">INPUTS</span></span>

### <span data-ttu-id="6d299-183">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d299-183">System.String</span></span>

### <span data-ttu-id="6d299-184">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="6d299-184">System.Guid</span></span>

## <span data-ttu-id="6d299-185">출력</span><span class="sxs-lookup"><span data-stu-id="6d299-185">OUTPUTS</span></span>

### <span data-ttu-id="6d299-186">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d299-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="6d299-187">상속자</span><span class="sxs-lookup"><span data-stu-id="6d299-187">NOTES</span></span>
<span data-ttu-id="6d299-188">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="6d299-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6d299-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d299-189">RELATED LINKS</span></span>

[<span data-ttu-id="6d299-190">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6d299-190">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="6d299-191">제거-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6d299-191">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="6d299-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6d299-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
