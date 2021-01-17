---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490375"
---
# <span data-ttu-id="f14ab-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f14ab-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="f14ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f14ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f14ab-103">지정된 범위에서 지정된 보안 주체에 지정된 RBAC 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="f14ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="f14ab-104">SYNTAX</span></span>

### <span data-ttu-id="f14ab-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f14ab-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14ab-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14ab-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f14ab-116">설명</span><span class="sxs-lookup"><span data-stu-id="f14ab-116">DESCRIPTION</span></span>
<span data-ttu-id="f14ab-117">New-AzRoleAssignment 명령을 사용하여 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="f14ab-118">액세스 권한은 적절한 범위에서 적절한 RBAC 역할을 할당하여 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="f14ab-119">전체 구독에 대한 액세스 권한을 부여하려면 구독 범위에서 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="f14ab-120">구독 내의 특정 리소스 그룹에 대한 액세스 권한을 부여하려면 리소스 그룹 범위에서 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="f14ab-121">과제의 제목을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="f14ab-122">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="f14ab-123">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="f14ab-124">Azure AD 애플리케이션을 지정하기 위해 ApplicationId 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="f14ab-125">할당되는 역할은 RoleDefinitionName 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="f14ab-126">액세스 권한이 부여되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="f14ab-127">기본적으로 선택한 구독으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="f14ab-128">할당의 범위는 다음 매개 변수 조합 a 중 하나를 사용하여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="f14ab-129">범위 - /subscriptions/b로 시작하는 정식 \<subscriptionId\> 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="f14ab-130">ResourceGroupName - 지정된 리소스 그룹에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="f14ab-131">c.</span><span class="sxs-lookup"><span data-stu-id="f14ab-131">c.</span></span>
<span data-ttu-id="f14ab-132">ResourceName, ResourceType, ResourceGroupName 및 (선택 사항) ParentResource - 액세스 권한을 부여할 리소스 그룹 내에서 특정 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="f14ab-133">예제</span><span class="sxs-lookup"><span data-stu-id="f14ab-133">EXAMPLES</span></span>

### <span data-ttu-id="f14ab-134">예제 1</span><span class="sxs-lookup"><span data-stu-id="f14ab-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="f14ab-135">위임에 사용할 수 있는 역할 할당을 통해 리소스 그룹 범위에서 사용자에게 읽기 권한자 역할 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="f14ab-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="f14ab-136">예제 2</span><span class="sxs-lookup"><span data-stu-id="f14ab-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="f14ab-137">보안 그룹에 대한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="f14ab-137">Grant access to a security group</span></span>

### <span data-ttu-id="f14ab-138">예제 3</span><span class="sxs-lookup"><span data-stu-id="f14ab-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="f14ab-139">리소스(웹 사이트)에서 사용자에게 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="f14ab-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="f14ab-140">예제 4</span><span class="sxs-lookup"><span data-stu-id="f14ab-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="f14ab-141">중첩된 리소스(서브넷)에서 그룹에 대한 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="f14ab-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="f14ab-142">예제 5</span><span class="sxs-lookup"><span data-stu-id="f14ab-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="f14ab-143">서비스 주체에 대한 읽기 권한자 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="f14ab-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="f14ab-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f14ab-144">PARAMETERS</span></span>

### <span data-ttu-id="f14ab-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="f14ab-145">-AllowDelegation</span></span>
<span data-ttu-id="f14ab-146">역할 할당을 만드는 동안 위임 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="f14ab-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f14ab-147">-ApplicationId</span></span>
<span data-ttu-id="f14ab-148">ServicePrincipal의 애플리케이션 ID</span><span class="sxs-lookup"><span data-stu-id="f14ab-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="f14ab-149">-Condition</span><span class="sxs-lookup"><span data-stu-id="f14ab-149">-Condition</span></span>
<span data-ttu-id="f14ab-150">RoleAssignment에 적용할 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14ab-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="f14ab-151">-ConditionVersion</span></span>
<span data-ttu-id="f14ab-152">조건의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14ab-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14ab-153">-DefaultProfile</span></span>
<span data-ttu-id="f14ab-154">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f14ab-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f14ab-155">-Description</span><span class="sxs-lookup"><span data-stu-id="f14ab-155">-Description</span></span>
<span data-ttu-id="f14ab-156">역할 할당에 대한 간략한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14ab-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f14ab-157">-InputFile</span></span>
<span data-ttu-id="f14ab-158">역할 할당 json에 대한 경로</span><span class="sxs-lookup"><span data-stu-id="f14ab-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14ab-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f14ab-159">-ObjectId</span></span>
<span data-ttu-id="f14ab-160">사용자, 그룹 또는 서비스 주체의 Azure AD Objectid입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-160">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="f14ab-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="f14ab-161">-ParentResource</span></span>
<span data-ttu-id="f14ab-162">계층 구조의 부모 리소스(ResourceName 매개 변수를 사용하여 지정된 리소스)</span><span class="sxs-lookup"><span data-stu-id="f14ab-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="f14ab-163">ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용하여 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f14ab-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14ab-164">-ResourceGroupName</span></span>
<span data-ttu-id="f14ab-165">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-165">The resource group name.</span></span>
<span data-ttu-id="f14ab-166">지정된 리소스 그룹에 효과적인 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="f14ab-167">ResourceName, ResourceType 및 (선택 사항)ParentResource 매개 변수와 함께 사용되는 경우 이 명령은 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f14ab-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f14ab-168">-ResourceName</span></span>
<span data-ttu-id="f14ab-169">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-169">The resource name.</span></span>
<span data-ttu-id="f14ab-170">예: storageaccountprod</span><span class="sxs-lookup"><span data-stu-id="f14ab-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="f14ab-171">ResourceGroupName, ResourceType 및 (선택 사항) ParentResource 매개 변수와 함께 사용하여 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f14ab-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f14ab-172">-ResourceType</span></span>
<span data-ttu-id="f14ab-173">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-173">The resource type.</span></span>
<span data-ttu-id="f14ab-174">예: Microsoft.Network/virtualNetworks</span><span class="sxs-lookup"><span data-stu-id="f14ab-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="f14ab-175">ResourceGroupName, ResourceName 및 (선택 사항) ParentResource 매개 변수와 함께 사용하여 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f14ab-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f14ab-176">-RoleDefinitionId</span></span>
<span data-ttu-id="f14ab-177">보안 주체에 할당해야 하는 RBAC 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="f14ab-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f14ab-178">-RoleDefinitionName</span></span>
<span data-ttu-id="f14ab-179">보안 주체에 할당해야 하는 RBAC 역할의 이름(예: 읽기 권한자, 참가자, Virtual Network 관리자 등)</span><span class="sxs-lookup"><span data-stu-id="f14ab-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="f14ab-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="f14ab-180">-Scope</span></span>
<span data-ttu-id="f14ab-181">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="f14ab-182">상대 URI 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-182">In the format of relative URI.</span></span>
<span data-ttu-id="f14ab-183">예: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="f14ab-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="f14ab-184">지정하지 않으면 구독 수준에서 역할 할당을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="f14ab-185">지정된 경우 "/subscriptions/{id}"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-185">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="f14ab-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f14ab-186">-SignInName</span></span>
<span data-ttu-id="f14ab-187">사용자의 이메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-187">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="f14ab-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14ab-188">CommonParameters</span></span>
<span data-ttu-id="f14ab-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ab-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14ab-190">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f14ab-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14ab-191">입력</span><span class="sxs-lookup"><span data-stu-id="f14ab-191">INPUTS</span></span>

### <span data-ttu-id="f14ab-192">System.String</span><span class="sxs-lookup"><span data-stu-id="f14ab-192">System.String</span></span>

### <span data-ttu-id="f14ab-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f14ab-193">System.Guid</span></span>

## <span data-ttu-id="f14ab-194">출력</span><span class="sxs-lookup"><span data-stu-id="f14ab-194">OUTPUTS</span></span>

### <span data-ttu-id="f14ab-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f14ab-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f14ab-196">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f14ab-196">NOTES</span></span>
<span data-ttu-id="f14ab-197">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="f14ab-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f14ab-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f14ab-198">RELATED LINKS</span></span>

[<span data-ttu-id="f14ab-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f14ab-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="f14ab-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f14ab-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="f14ab-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f14ab-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
