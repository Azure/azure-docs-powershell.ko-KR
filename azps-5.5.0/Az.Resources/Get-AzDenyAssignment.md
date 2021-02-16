---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178849"
---
# <span data-ttu-id="224b4-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="224b4-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="224b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224b4-102">SYNOPSIS</span></span>
<span data-ttu-id="224b4-103">지정된 범위에서 Azure RBAC 거부 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="224b4-104">기본적으로 선택한 Azure 구독의 모든 거부 할당이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="224b4-105">해당 매개 변수를 사용하여 특정 사용자에게 거부 할당을 나열하거나 특정 리소스 그룹 또는 리소스에 대한 거부 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="224b4-106">구문</span><span class="sxs-lookup"><span data-stu-id="224b4-106">SYNTAX</span></span>

### <span data-ttu-id="224b4-107">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="224b4-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224b4-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="224b4-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="224b4-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="224b4-125">설명</span><span class="sxs-lookup"><span data-stu-id="224b4-125">DESCRIPTION</span></span>
<span data-ttu-id="224b4-126">Get-AzDenyAssignment 명령을 사용하여 범위에 효과적인 모든 거부 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="224b4-127">매개 변수가 없는 경우 이 명령은 구독에서 수행된 모든 거부 할당을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="224b4-128">보안 주체, 거부 할당 이름 및 범위에 대한 필터링 매개 변수를 사용하여 이 목록을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="224b4-129">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="224b4-130">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="224b4-131">Azure AD 애플리케이션을 지정하기 위해 ServicePrincipalName 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="224b4-132">액세스가 거부되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="224b4-133">기본적으로 선택한 구독으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="224b4-134">거부 할당의 범위는 다음 매개 변수 조합 a 중 하나를 사용하여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="224b4-135">범위 - /subscriptions/로 시작하는 정식 \<subscriptionId\> 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="224b4-136">이렇게 하면 특정 범위에 적용된 거부 할당(즉, 해당 범위 이상에서 모든 거부 할당)이 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="224b4-137">b.</span><span class="sxs-lookup"><span data-stu-id="224b4-137">b.</span></span>
<span data-ttu-id="224b4-138">ResourceGroupName - 구독에 속한 모든 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="224b4-139">이렇게 하면 지정된 리소스 그룹에서 유효하게 할당을 필터링합니다. 즉, 해당 범위 이상에서 모든 거부 할당이 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="224b4-140">c.</span><span class="sxs-lookup"><span data-stu-id="224b4-140">c.</span></span>
<span data-ttu-id="224b4-141">ResourceName, ResourceType, ResourceGroupName 및 (선택 사항) ParentResource - 구독에서 특정 리소스를 식별하고 해당 리소스 범위에서 유효 거부 할당을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="224b4-142">구독의 특정 사용자에 대해 거부되는 액세스를 확인하려면 ExpandPrincipalGroups 스위치를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="224b4-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="224b4-143">그러면 사용자 및 사용자가 구성원인 그룹에 할당된 모든 거부 할당이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="224b4-144">예제</span><span class="sxs-lookup"><span data-stu-id="224b4-144">EXAMPLES</span></span>

### <span data-ttu-id="224b4-145">예제 1</span><span class="sxs-lookup"><span data-stu-id="224b4-145">Example 1</span></span>

<span data-ttu-id="224b4-146">구독의 모든 거부 할당 나열</span><span class="sxs-lookup"><span data-stu-id="224b4-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="224b4-147">예제 2</span><span class="sxs-lookup"><span data-stu-id="224b4-147">Example 2</span></span>

<span data-ttu-id="224b4-148">scope testRG 이상에서 사용자에게 수행된 모든 거부 john.doe@contoso.com 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="224b4-149">예제 3</span><span class="sxs-lookup"><span data-stu-id="224b4-149">Example 3</span></span>

<span data-ttu-id="224b4-150">지정된 서비스 주체의 모든 거부 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="224b4-151">예제 4</span><span class="sxs-lookup"><span data-stu-id="224b4-151">Example 4</span></span>

<span data-ttu-id="224b4-152">'site1' 웹 사이트 범위에서 거부 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="224b4-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="224b4-153">PARAMETERS</span></span>

### <span data-ttu-id="224b4-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224b4-154">-DefaultProfile</span></span>
<span data-ttu-id="224b4-155">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="224b4-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="224b4-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="224b4-156">-DenyAssignmentName</span></span>
<span data-ttu-id="224b4-157">거부 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224b4-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="224b4-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="224b4-159">지정된 경우 사용자 및 사용자가 멤버인 그룹에 직접 할당된 거부 할당을 반환합니다(전이적).</span><span class="sxs-lookup"><span data-stu-id="224b4-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="224b4-160">사용자 계정에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="224b4-161">-Id</span><span class="sxs-lookup"><span data-stu-id="224b4-161">-Id</span></span>
<span data-ttu-id="224b4-162">할당 ID를 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224b4-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="224b4-163">-ObjectId</span></span>
<span data-ttu-id="224b4-164">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="224b4-165">지정된 보안 주체에 대해 수행된 모든 거부 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224b4-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="224b4-166">-ParentResource</span></span>
<span data-ttu-id="224b4-167">ResourceName 매개 변수를 사용하여 지정된 리소스의 계층 구조에 있는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="224b4-168">ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="224b4-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224b4-169">-ResourceGroupName</span></span>
<span data-ttu-id="224b4-170">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-170">The resource group name.</span></span>
<span data-ttu-id="224b4-171">지정된 리소스 그룹에 효과적인 거부 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="224b4-172">ResourceName, ResourceType 및 ParentResource 매개 변수와 함께 사용하는 경우 명령은 리소스 그룹 내의 리소스에서 유효하지는 할당을 거부하는 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="224b4-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="224b4-173">-ResourceName</span></span>
<span data-ttu-id="224b4-174">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-174">The resource name.</span></span>
<span data-ttu-id="224b4-175">예: storageaccountprod</span><span class="sxs-lookup"><span data-stu-id="224b4-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="224b4-176">ResourceGroupName, ResourceType 및 (선택 사항) ParentResource 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="224b4-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="224b4-177">-ResourceType</span></span>
<span data-ttu-id="224b4-178">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-178">The resource type.</span></span>
<span data-ttu-id="224b4-179">예: Microsoft.Network/virtualNetworks</span><span class="sxs-lookup"><span data-stu-id="224b4-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="224b4-180">ResourceGroupName, ResourceName 및 (선택 사항) ParentResource 매개 변수와 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="224b4-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="224b4-181">-Scope</span></span>
<span data-ttu-id="224b4-182">역할 할당의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="224b4-183">상대 URI 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-183">In the format of relative URI.</span></span>
<span data-ttu-id="224b4-184">예: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="224b4-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="224b4-185">"/subscriptions/{id}"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="224b4-186">이 명령은 해당 범위에 적용된 모든 거부 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="224b4-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="224b4-187">-ServicePrincipalName</span></span>
<span data-ttu-id="224b4-188">서비스 주체의 ServicePrincipalName입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="224b4-189">지정된 Azure AD 애플리케이션에 대해 수행된 모든 거부 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="224b4-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="224b4-190">-SignInName</span></span>
<span data-ttu-id="224b4-191">사용자의 이메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="224b4-192">지정된 사용자에게 수행된 모든 거부 할당을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="224b4-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224b4-193">CommonParameters</span></span>
<span data-ttu-id="224b4-194">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="224b4-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224b4-195">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="224b4-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224b4-196">입력</span><span class="sxs-lookup"><span data-stu-id="224b4-196">INPUTS</span></span>

### <span data-ttu-id="224b4-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="224b4-197">System.Guid</span></span>

### <span data-ttu-id="224b4-198">System.String</span><span class="sxs-lookup"><span data-stu-id="224b4-198">System.String</span></span>

## <span data-ttu-id="224b4-199">출력</span><span class="sxs-lookup"><span data-stu-id="224b4-199">OUTPUTS</span></span>

### <span data-ttu-id="224b4-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="224b4-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="224b4-201">참고 사항</span><span class="sxs-lookup"><span data-stu-id="224b4-201">NOTES</span></span>
<span data-ttu-id="224b4-202">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="224b4-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="224b4-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="224b4-203">RELATED LINKS</span></span>
