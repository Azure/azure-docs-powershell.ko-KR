---
title: Azure PowerShell을 사용하여 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 앱 또는 서비스의 서비스 주체를 만드는 방법을 알아봅니다.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 38bb4345a9e4d2d9e450e74f99fb2c320c3ca4d8
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534908"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="a58ff-104">Azure PowerShell을 사용하여 Azure 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a58ff-104">Create an Azure service principal with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="a58ff-105">Azure PowerShell을 사용하여 앱 또는 서비스를 관리하려는 경우 소유한 자격 증명 대신 AAD(Azure Active Directory) 서비스 주체에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="a58ff-106">이 문서에서는 Azure PowerShell을 사용하여 보안 주체를 만드는 과정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="a58ff-107">Azure Portal을 통해 서비스 주체를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="a58ff-108">자세한 내용은 [포털을 사용하여 리소스에 액세스할 수 있는 Active Directory 애플리케이션 및 서비스 주체 만들기](/azure/azure-resource-manager/resource-group-create-service-principal-portal)를 참고하세요.</span><span class="sxs-lookup"><span data-stu-id="a58ff-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="a58ff-109">'서비스 주체'란?</span><span class="sxs-lookup"><span data-stu-id="a58ff-109">What is a 'service principal'?</span></span>

<span data-ttu-id="a58ff-110">Azure 서비스 주체는 특정 Azure 리소스에 액세스하기 위해 사용자가 만든 앱과 서비스, 자동화 도구에서 사용하는 보안 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="a58ff-111">특정한 역할이 있는 '사용자 ID'(사용자 이름과 암호 또는 인증서)이며 엄격하게 통제된 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="a58ff-112">일반 사용자 ID와 달리 서비스 주체는 특정 작업만 수행하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="a58ff-113">해당 관리 작업을 수행하는 데 필요한 최소 사용 권한 수준을 부여하면 보안이 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="a58ff-114">고유한 사용 권한 수준 확인</span><span class="sxs-lookup"><span data-stu-id="a58ff-114">Verify your own permission level</span></span>

<span data-ttu-id="a58ff-115">먼저 Azure Active Directory와 Azure 구독에 대한 충분한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="a58ff-116">Active Directory에서 앱을 만들고 서비스 주체에 역할을 할당할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="a58ff-117">계정에 올바른 사용 권한이 있는지를 확인하는 가장 쉬운 방법은 포털을 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="a58ff-118">[필요한 사용 권한 확인](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a58ff-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="a58ff-119">앱의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a58ff-119">Create a service principal for your app</span></span>

<span data-ttu-id="a58ff-120">Azure 계정에 로그인하면 서비스 주체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="a58ff-121">다음 방법 중 하나로 배포된 앱을 식별해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="a58ff-122">다음 예제처럼 "MyDemoWebApp"와 같은 배포된 앱의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="a58ff-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="a58ff-123">애플리케이션 ID, 배포된 앱, 서비스 또는 개체와 관련된 고유 GUID</span><span class="sxs-lookup"><span data-stu-id="a58ff-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="a58ff-124">애플리케이션에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a58ff-124">Get information about your application</span></span>

<span data-ttu-id="a58ff-125">`Get-AzureRmADApplication` cmdlet을 사용하여 애플리케이션에 대한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="a58ff-126">애플리케이션의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a58ff-126">Create a service principal for your application</span></span>

<span data-ttu-id="a58ff-127">`New-AzureRmADServicePrincipal` cmdlet을 사용하여 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="a58ff-128">여기에서 Connect-AzureRmAccount에서 $servicePrincipal.Secret 속성을 직접 사용하거나(아래 "서비스 사용자를 사용하여 로그인"을 참조), 이 SecureString을 일반 텍스트 문자열로 변환하여 나중에 사용하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-128">From here, you can either directly use the $servicePrincipal.Secret property in Connect-AzureRmAccount (see "Sign in using the service principal" below), or you can convert this SecureString to a plain text string for later usage:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="a58ff-129">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="a58ff-129">Sign in using the service principal</span></span>

<span data-ttu-id="a58ff-130">이제 제공한 *appId* 및 자동으로 생성된 *암호*를 사용하여 앱에 새로운 서비스 주체로 로그인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-130">You can now sign in as the new service principal for your app using the *appId* you provided and *password* that was automatically generated.</span></span> <span data-ttu-id="a58ff-131">서비스 주체에 대한 테넌트 ID도 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="a58ff-132">개인 자격 증명을 사용하여 Azure에 로그인하는 경우 테넌트 ID가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="a58ff-133">서비스 주체로 로그인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="a58ff-134">로그인이 성공한 후 다음과 같은 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="a58ff-135">축하합니다!</span><span class="sxs-lookup"><span data-stu-id="a58ff-135">Congratulations!</span></span> <span data-ttu-id="a58ff-136">이러한 자격 증명을 사용하여 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="a58ff-137">다음으로 서비스 주체의 사용 권한을 조정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="a58ff-138">역할 관리</span><span class="sxs-lookup"><span data-stu-id="a58ff-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="a58ff-139">Azure 역할 기반 Access Control(RBAC)은 사용자 및 서비스 주체에 대한 역할을 정의하고 관리하기 위한 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="a58ff-140">역할에는 그와 관련된 일련의 사용 권한이 있으며 여기서 주체가 읽고 액세스하고 쓰고 관리할 수 있는 리소스를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="a58ff-141">RBAC와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a58ff-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="a58ff-142">Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="a58ff-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a58ff-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="a58ff-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a58ff-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="a58ff-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a58ff-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="a58ff-146">서비스 주체의 기본 역할은 **참가자**입니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="a58ff-147">광범위한 사용 권한을 고려하면 Azure 서비스와 앱의 상호 작용의 범위에 따라 최상의 선택이 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="a58ff-148">**읽기 권한자** 역할은 더 제한적이며 읽기 전용 앱의 경우에 좋은 선택이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="a58ff-149">역할 관련 사용 권한에 대한 세부 정보를 보거나 Azure Portal을 통해 사용자 지정 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="a58ff-150">이 예제에서는 **읽기 권한자** 역할을 이전 예제에 추가하고 **참가자** 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="a58ff-151">현재 할당된 역할을 보려면:</span><span class="sxs-lookup"><span data-stu-id="a58ff-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="a58ff-152">역할 관리를 위한 기타 Azure PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a58ff-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="a58ff-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a58ff-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="a58ff-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a58ff-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="a58ff-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a58ff-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="a58ff-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a58ff-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="a58ff-157">보안 주체의 자격 증명 변경</span><span class="sxs-lookup"><span data-stu-id="a58ff-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="a58ff-158">보안을 향상시키려면 사용 권한을 검토하고 암호를 정기적으로 업데이트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="a58ff-159">앱이 변경될 때 보안 자격 증명을 관리하고 수정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="a58ff-160">예를 들어, 새 암호를 만들고 이전 암호를 제거하여 서비스 주체의 암호를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58ff-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="a58ff-161">서비스 주체의 새 암호 추가</span><span class="sxs-lookup"><span data-stu-id="a58ff-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="a58ff-162">서비스 주체의 자격 증명 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="a58ff-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="a58ff-163">서비스 주체에게서 이전 암호 제거</span><span class="sxs-lookup"><span data-stu-id="a58ff-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="a58ff-164">서비스 주체의 자격 증명 목록 확인</span><span class="sxs-lookup"><span data-stu-id="a58ff-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="a58ff-165">서비스 주체에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a58ff-165">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
