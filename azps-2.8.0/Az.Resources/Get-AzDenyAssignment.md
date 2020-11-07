---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871878"
---
# <span data-ttu-id="8f090-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f090-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="8f090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f090-102">SYNOPSIS</span></span>
<span data-ttu-id="8f090-103">지정 된 범위에서 Azure RBAC 거부 배정을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="8f090-104">기본적으로 선택한 Azure 구독에 모든 거부 할당이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="8f090-105">해당 매개 변수를 사용 하 여 특정 사용자에 게 할당 거부를 나열 하거나 특정 리소스 그룹 또는 리소스에 대해 거부 배정을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="8f090-106">구문과</span><span class="sxs-lookup"><span data-stu-id="8f090-106">SYNTAX</span></span>

### <span data-ttu-id="8f090-107">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f090-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f090-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f090-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f090-125">설명은</span><span class="sxs-lookup"><span data-stu-id="8f090-125">DESCRIPTION</span></span>
<span data-ttu-id="8f090-126">Get-AzDenyAssignment 명령을 사용 하 여 범위에 적용 되는 모든 거부 할당을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="8f090-127">매개 변수 없이이 명령을 사용 하면 구독에서 생성 된 모든 거부 할당이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="8f090-128">이 목록은 주도자, 거부 할당 이름 및 범위에 대 한 필터링 매개 변수를 사용 하 여 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="8f090-129">사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="8f090-130">보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="8f090-131">Azure AD 응용 프로그램을 지정 하려면 ServicePrincipalName 또는 ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="8f090-132">액세스가 거부 되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="8f090-133">선택한 구독이 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="8f090-134">거부 할당의 범위는 다음 매개 변수 조합 a 중 하나를 사용 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="8f090-135">Scope-/subscriptions/subscriptionId부터 시작 하는 정규화 된 범위 \< 입니다 \> .</span><span class="sxs-lookup"><span data-stu-id="8f090-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="8f090-136">이렇게 하면 특정 범위 (예: 해당 범위에 있는 모든 거부 할당)에 적용 되는 거부 할당이 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8f090-137">b.</span><span class="sxs-lookup"><span data-stu-id="8f090-137">b.</span></span>
<span data-ttu-id="8f090-138">ResourceGroupName-구독에 있는 모든 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="8f090-139">이렇게 하면 지정 된 리소스 그룹 (예: 해당 범위에 있는 모든 거부 할당)에서 유효 하 게 배정을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="8f090-140">c.</span><span class="sxs-lookup"><span data-stu-id="8f090-140">c.</span></span>
<span data-ttu-id="8f090-141">Context.resourcename, ResourceType, ResourceGroupName 및 (선택적) ParentResource-구독에서 특정 리소스를 식별 하 고 해당 리소스 범위에서 유효 하 게 할당 거부를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="8f090-142">구독에서 특정 사용자에 대해 거부 되는 액세스 권한을 확인 하려면 ExpandPrincipalGroups 스위치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="8f090-143">이렇게 하면 사용자에 게 할당 된 모든 거부 할당과 사용자가 구성원으로 속한 그룹에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="8f090-144">예제의</span><span class="sxs-lookup"><span data-stu-id="8f090-144">EXAMPLES</span></span>

### <span data-ttu-id="8f090-145">예제 1</span><span class="sxs-lookup"><span data-stu-id="8f090-145">Example 1</span></span>

<span data-ttu-id="8f090-146">구독에 모든 거부 과제를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8f090-147">예제 2</span><span class="sxs-lookup"><span data-stu-id="8f090-147">Example 2</span></span>

<span data-ttu-id="8f090-148">범위 testRG 이상에서 사용자에 게 적용 된 모든 거부 배정을 가져옵니다 john.doe@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8f090-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8f090-149">예제 3</span><span class="sxs-lookup"><span data-stu-id="8f090-149">Example 3</span></span>

<span data-ttu-id="8f090-150">지정 된 서비스 사용자의 모든 거부 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="8f090-151">예제 4</span><span class="sxs-lookup"><span data-stu-id="8f090-151">Example 4</span></span>

<span data-ttu-id="8f090-152">' Site1 ' 웹 사이트 범위에서 거부 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

```

## <span data-ttu-id="8f090-153">변수</span><span class="sxs-lookup"><span data-stu-id="8f090-153">PARAMETERS</span></span>

### <span data-ttu-id="8f090-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f090-154">-DefaultProfile</span></span>
<span data-ttu-id="8f090-155">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f090-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f090-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8f090-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="8f090-157">지정 하는 경우 사용자에 게 직접 할당 된 거부 할당과 사용자가 구성원으로 속해 있는 그룹 (전이적)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="8f090-158">사용자 보안 주체에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-158">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="8f090-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8f090-159">-ObjectId</span></span>
<span data-ttu-id="8f090-160">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="8f090-161">지정 된 계정에 대 한 모든 거부 할당을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-161">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f090-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="8f090-162">-ParentResource</span></span>
<span data-ttu-id="8f090-163">Context.resourcename 매개 변수를 사용 하 여 지정 된 리소스의 계층 구조에 있는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="8f090-164">ResourceGroupName, ResourceType 및 Context.resourcename 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="8f090-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f090-165">-ResourceGroupName</span></span>
<span data-ttu-id="8f090-166">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-166">The resource group name.</span></span>
<span data-ttu-id="8f090-167">지정 된 리소스 그룹에 적용 되는 거부 할당을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="8f090-168">이 명령은 Context.resourcename, ResourceType, ParentResource 매개 변수와 함께 사용 되는 경우 리소스 그룹 내의 리소스에 대 한 효율적인 할당 거부를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="8f090-169">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="8f090-169">-ResourceName</span></span>
<span data-ttu-id="8f090-170">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-170">The resource name.</span></span>
<span data-ttu-id="8f090-171">예를 들어 storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="8f090-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="8f090-172">ResourceGroupName, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="8f090-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8f090-173">-ResourceType</span></span>
<span data-ttu-id="8f090-174">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-174">The resource type.</span></span>
<span data-ttu-id="8f090-175">예를 들어 Microsoft. p r o m/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="8f090-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="8f090-176">ResourceGroupName, Context.resourcename 및 (선택적) ParentResource 매개 변수와 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="8f090-177">-범위</span><span class="sxs-lookup"><span data-stu-id="8f090-177">-Scope</span></span>
<span data-ttu-id="8f090-178">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="8f090-179">상대 URI 형식</span><span class="sxs-lookup"><span data-stu-id="8f090-179">In the format of relative URI.</span></span>
<span data-ttu-id="8f090-180">예를 들어/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="8f090-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="8f090-181">"/Subscriptions/{id}"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="8f090-182">이 명령은 해당 범위에서 효력을 갖는 모든 거부 할당을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-182">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="8f090-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8f090-183">-ServicePrincipalName</span></span>
<span data-ttu-id="8f090-184">서비스 사용자의 ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="8f090-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="8f090-185">지정 된 Azure AD 응용 프로그램에 대 한 모든 거부 할당을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="8f090-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8f090-186">-SignInName</span></span>
<span data-ttu-id="8f090-187">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="8f090-188">지정 된 사용자에 대 한 모든 거부 배정을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-188">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="8f090-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f090-189">CommonParameters</span></span>
<span data-ttu-id="8f090-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f090-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f090-191">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f090-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f090-192">입력</span><span class="sxs-lookup"><span data-stu-id="8f090-192">INPUTS</span></span>

### <span data-ttu-id="8f090-193">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="8f090-193">System.Guid</span></span>

### <span data-ttu-id="8f090-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f090-194">System.String</span></span>

## <span data-ttu-id="8f090-195">출력</span><span class="sxs-lookup"><span data-stu-id="8f090-195">OUTPUTS</span></span>

### <span data-ttu-id="8f090-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f090-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="8f090-197">상속자</span><span class="sxs-lookup"><span data-stu-id="8f090-197">NOTES</span></span>
<span data-ttu-id="8f090-198">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="8f090-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>