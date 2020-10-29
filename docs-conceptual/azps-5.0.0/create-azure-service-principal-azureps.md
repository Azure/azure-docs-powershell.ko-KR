---
title: Azure PowerShell로 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 서비스 주체를 만들고 사용하는 방법을 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3c876454560e4ad421e6d32a8ca8b30a651fd8af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754034"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="78db7-103">Azure PowerShell을 사용하여 Azure 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="78db7-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="78db7-104">Azure 서비스를 사용하도록 자동화된 도구에는 항상 제한된 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="78db7-105">Azure는 애플리케이션에서 모든 권한이 있는 사용자로 로그인하도록 하는 대신 서비스 주체를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="78db7-106">Azure 서비스 주체는 애플리케이션, 호스팅된 서비스 및 자동화된 도구에서 사용하여 Azure 리소스에 액세스하기 위해 만든 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="78db7-107">이 액세스는 서비스 주체에 할당된 역할로 제한되므로 액세스할 수 있는 리소스와 해당 수준을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="78db7-108">보안상의 이유로 사용자 ID를 통해 로그인할 수 있게 하는 대신, 항상 자동화된 도구에서 서비스 주체를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="78db7-109">이 문서에서는 Azure PowerShell을 사용하여 서비스 주체를 만들고, 정보를 가져오고, 다시 설정하는 단계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="78db7-110">서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="78db7-110">Create a service principal</span></span>

<span data-ttu-id="78db7-111">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet을 사용하여 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="78db7-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="78db7-112">서비스 주체를 만드는 경우 사용하는 로그인 인증 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="78db7-113">계정에 서비스 주체를 만들 수 있는 권한이 없는 경우 `New-AzADServicePrincipal`에서 "권한이 부족하여 작업을 완료할 수 없습니다"라는 오류 메시지를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="78db7-114">서비스 주체를 만들려면 Azure Active Directory 관리자에게 문의하십시오.</span><span class="sxs-lookup"><span data-stu-id="78db7-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="78db7-115">서비스 주체에 사용할 수 있는 인증 유형에는 암호 기반 인증 및 인증서 기반 인증의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="78db7-116">암호 기반 인증</span><span class="sxs-lookup"><span data-stu-id="78db7-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78db7-117">암호 기반 인증 서비스 주체의 기본 역할은 **기여자** 입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-117">The default role for a password-based authentication service principal is **Contributor** .</span></span> <span data-ttu-id="78db7-118">이 역할에는 Azure 계정에서 읽고 쓸 수 있는 모든 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="78db7-119">역할 할당 관리에 대한 내용은 [서비스 주체 역할 관리](#manage-service-principal-roles)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="78db7-120">다른 인증 매개 변수가 없으면 임의로 만든 암호를 통한 암호 기반 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="78db7-121">암호 기반 인증을 원하는 경우 이 메서드를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="78db7-122">반환된 개체는 생성된 암호를 포함하는 `Secret` 멤버인 `SecureString`을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="78db7-123">서비스 주체로 인증하려면 이 값을 안전한 곳에서 저장하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="78db7-124">해당 값은 콘솔 출력에 표시되지 _않습니다_ .</span><span class="sxs-lookup"><span data-stu-id="78db7-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="78db7-125">암호를 잊어버린 경우 [서비스 주체 자격 증명을 다시 설정](#reset-credentials)하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="78db7-126">다음 코드를 사용하면 비밀을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="78db7-127">사용자 제공한 암호의 경우, `-PasswordCredential` 인수는 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 개체를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="78db7-128">이러한 개체는 유효한 `StartDate`, `EndDate`가 있어야 하며 일반 텍스트 `Password`를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="78db7-129">암호를 만드는 경우 [Azure Active Directory 암호 규칙 및 제한](/azure/active-directory/active-directory-passwords-policy)을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="78db7-130">취약한 암호를 사용하거나 암호를 다시 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="78db7-131">`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78db7-132">서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="78db7-133">서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 _직후에_ 다음 명령을 실행하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="78db7-134">인증서 기반 인증</span><span class="sxs-lookup"><span data-stu-id="78db7-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78db7-135">인증서 기반 인증 서비스 주체를 만들 때에는 기본 역할이 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="78db7-136">역할 할당 관리에 대한 내용은 [서비스 주체 역할 관리](#manage-service-principal-roles)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="78db7-137">인증서 기반 인증을 사용하는 서비스 주체는 `-CertValue` 매개 변수를 사용하여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="78db7-138">이 매개 변수는 공용 인증서의 base64로 인코딩된 ASCII 문자열을 취합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="78db7-139">이는 PEM 파일 또는 텍스트 인코딩 CRT 또는 CER로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="78db7-140">공용 인증서의 이진 인코딩은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="78db7-141">이러한 명령은 사용할 수 있는 인증서가 이미 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="78db7-142">`PSADKeyCredential` 개체를 사용하는 `-KeyCredential` 매개 변수를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="78db7-143">이러한 객체는 유효한 `StartDate`, `EndDate`가 있어야 하며 `CertValue` 멤버가 공용 인증서의 base64 인코딩 ASCII 문자열로 설정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="78db7-144">`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="78db7-145">서비스 주체로 로그인하는 클라이언트는 인증서의 프라이빗 키에 액세스해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78db7-146">서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="78db7-147">서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 _직후에_ 다음 명령을 실행하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="78db7-148">기존 서비스 주체 가져오기</span><span class="sxs-lookup"><span data-stu-id="78db7-148">Get an existing service principal</span></span>

<span data-ttu-id="78db7-149">활성 테넌트의 서비스 주체 목록은 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal)을 사용하여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="78db7-150">이 명령은 기본적으로 테넌트의 _모든_ 서비스 주체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="78db7-151">대규모 조직의 경우 결과를 반환하는 데 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="78db7-152">대신 선택적 서버 측 필터링 인수 중 하나를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="78db7-153">`-DisplayNameBeginsWith`은 제공된 값과 일치하는 _접두사_ 가 있는 서비스 주체를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="78db7-154">서비스 주체의 표시 이름은 만드는 중에 `-DisplayName`으로 설정된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="78db7-155">`-DisplayName`은 서비스 주체 이름과 _정확히 일치하는_ 것을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="78db7-156">서비스 주체 역할 관리</span><span class="sxs-lookup"><span data-stu-id="78db7-156">Manage service principal roles</span></span>

<span data-ttu-id="78db7-157">Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="78db7-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="78db7-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="78db7-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="78db7-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="78db7-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="78db7-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="78db7-161">암호 기반 인증 서비스 주체의 기본 역할은 **기여자** 입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-161">The default role for a password-based authentication service principal is **Contributor** .</span></span> <span data-ttu-id="78db7-162">이 역할에는 Azure 계정에서 읽고 쓸 수 있는 모든 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="78db7-163">**Reader** (읽기 권한자) 역할은 읽기 전용 액세스 권한으로 더 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="78db7-164">RBAC(역할 기반 액세스 제어)와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="78db7-165">다음 예제에서는 **Reader** 역할을 추가하고 **Contributor** (기여자) 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="78db7-166">역할 할당 cmdlet은 서비스 사용자 주체 ID를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="78db7-167">생성 시 생성되는 관련 애플리케이션 ID를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="78db7-168">서비스 주체에 대한 애플리케이션 ID를 가져오려면 `Get-AzADServicePrincipal`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="78db7-169">계정에 역할을 할당할 수 있는 권한이 없으면 계정에 "'Microsoft.Authorization/roleAssignments/write' 작업을 수행할 수 있는 권한이 없습니다"라는 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="78db7-170">역할을 관리하려면 Azure Active Directory 관리자에게 문의하십시오.</span><span class="sxs-lookup"><span data-stu-id="78db7-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="78db7-171">역할을 추가해도 이전에 할당된 권한은 _제한되지 않습니다_ .</span><span class="sxs-lookup"><span data-stu-id="78db7-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="78db7-172">서비스 주체 권한을 제한할 때는 **Contributor** 역할을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="78db7-173">변경 내용은 할당된 역할을 나열하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="78db7-174">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="78db7-174">Sign in using a service principal</span></span>

<span data-ttu-id="78db7-175">로그인하여 새 서비스 주체의 자격 증명과 권한을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="78db7-176">서비스 주체로 로그인하려면 해당 서비스와 연결된 `applicationId` 값과 이 서비스가 생성된 테넌트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="78db7-177">암호를 사용하는 서비스 주체로 로그인하려면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="78db7-178">인증서 기반 인증을 사용하려면 Azure PowerShell이 인증서 지문을 기반으로 로컬 인증서 저장소에서 정보를 검색할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="78db7-179">PowerShell에서 액세스할 수 있는 자격 증명 저장소로 인증서를 가져오는 방법은 [Azure PowerShell로 로그인](authenticate-azureps.md#sp-signin)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="78db7-180">자격 증명 다시 설정</span><span class="sxs-lookup"><span data-stu-id="78db7-180">Reset credentials</span></span>

<span data-ttu-id="78db7-181">서비스 주체의 자격 증명을 잊어버린 경우 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential)을 통해 임의의 암호를 사용하는 새 자격 증명을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="78db7-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="78db7-182">이 cmdlet은 암호를 다시 설정할 때 사용자 정의 자격 증명을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78db7-183">새 자격 증명을 할당하기 전에 해당 로그인을 방지하기 위해 기존 자격 증명을 제거하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="78db7-184">이를 위해서는 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="78db7-185">문제 해결</span><span class="sxs-lookup"><span data-stu-id="78db7-185">Troubleshooting</span></span>

<span data-ttu-id="78db7-186">만약 _"New-AzADServicePrincipal: identifierUris 속성 값이 동일한 다른 개체가 이미 있습니다."_ 이름이 같은 서비스 주체가 없는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_ , verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="78db7-187">기존 서비스 주체가 더 이상 필요 없으면 다음 예제를 사용하여 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="78db7-188">이전에 Azure Active Directory 애플리케이션에 대한 서비스 주체를 만든 경우에도 이 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="78db7-189">서비스 주체를 제거해도 애플리케이션을 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="78db7-190">이 애플리케이션은 이름이 같은 또 다른 서비스 주체를 만들지 못하게 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="78db7-191">다음 예제를 사용하여 이름이 같은 Azure Active Directory 애플리케이션이 없는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="78db7-192">이름이 같은 애플리케이션이 있는 경우 다음 예제를 사용하여 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="78db7-193">그렇지 않으면 만들려는 새 서비스 주체의 다른 이름을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="78db7-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
