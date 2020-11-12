---
title: Azure PowerShell로 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 서비스 주체를 만들고 사용하는 방법을 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a8ce4669d52e587bd171cbeab2496e5386029615
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407972"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="5e4c1-103">Azure PowerShell을 사용하여 Azure 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="5e4c1-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="5e4c1-104">Azure 서비스를 사용하도록 자동화된 도구에는 항상 제한된 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="5e4c1-105">Azure는 애플리케이션에서 모든 권한이 있는 사용자로 로그인하도록 하는 대신 서비스 주체를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="5e4c1-106">Azure 서비스 주체는 애플리케이션, 호스팅된 서비스 및 자동화된 도구에서 사용하여 Azure 리소스에 액세스하기 위해 만든 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="5e4c1-107">이 액세스는 서비스 주체에 할당된 역할로 제한되므로 액세스할 수 있는 리소스와 해당 수준을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="5e4c1-108">보안상의 이유로 사용자 ID를 통해 로그인할 수 있게 하는 대신, 항상 자동화된 도구에서 서비스 주체를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="5e4c1-109">이 문서에서는 Azure PowerShell을 사용하여 서비스 주체를 만들고, 정보를 가져오고, 다시 설정하는 단계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="5e4c1-110">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) 명령을 사용하여 서비스 주체를 만들면 보호해야 하는 자격 증명이 출력에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="5e4c1-111">이러한 자격 증명을 코드에 포함하지 않도록 하거나 소스 제어에 자격 증명을 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="5e4c1-112">또는 자격 증명을 사용할 필요가 없도록 [관리 ID](/azure/active-directory/managed-identities-azure-resources/overview)를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="5e4c1-113">기본적으로 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal)은 구독 범위에서 서비스 주체에 [Contributor](/azure/role-based-access-control/built-in-roles#contributor) 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="5e4c1-114">서비스 주체가 손상될 위험을 줄이려면 보다 구체적인 역할을 할당하고 범위를 리소스 또는 리소스 그룹으로 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="5e4c1-115">자세한 내용은 [역할 할당을 추가하는 단계](/azure/role-based-access-control/role-assignments-steps)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="5e4c1-116">서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="5e4c1-116">Create a service principal</span></span>

<span data-ttu-id="5e4c1-117">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet을 사용하여 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="5e4c1-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="5e4c1-118">서비스 주체를 만드는 경우 사용하는 로그인 인증 유형을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="5e4c1-119">계정에 서비스 주체를 만들 수 있는 권한이 없는 경우 `New-AzADServicePrincipal`에서 "권한이 부족하여 작업을 완료할 수 없습니다."라는 오류 메시지를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="5e4c1-120">서비스 주체를 만들려면 Azure Active Directory 관리자에게 문의하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="5e4c1-121">서비스 주체에 사용할 수 있는 인증 유형에는 암호 기반 인증 및 인증서 기반 인증의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="5e4c1-122">암호 기반 인증</span><span class="sxs-lookup"><span data-stu-id="5e4c1-122">Password-based authentication</span></span>

<span data-ttu-id="5e4c1-123">다른 인증 매개 변수가 없으면 임의로 만든 암호를 통한 암호 기반 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-123">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="5e4c1-124">암호 기반 인증을 원하는 경우 이 메서드를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-124">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="5e4c1-125">반환된 개체는 생성된 암호를 포함하는 `Secret` 멤버인 `SecureString`을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-125">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="5e4c1-126">서비스 주체로 인증하려면 이 값을 안전한 곳에서 저장하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-126">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="5e4c1-127">해당 값은 콘솔 출력에 표시되지 __않습니다__.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-127">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="5e4c1-128">암호를 잊어버린 경우 [서비스 주체 자격 증명을 다시 설정](#reset-credentials)하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-128">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="5e4c1-129">다음 코드를 사용하면 비밀을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-129">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="5e4c1-130">사용자 제공한 암호의 경우, `-PasswordCredential` 인수는 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 개체를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-130">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="5e4c1-131">이러한 개체는 유효한 `StartDate`, `EndDate`가 있어야 하며 일반 텍스트 `Password`를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-131">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="5e4c1-132">암호를 만드는 경우 [Azure Active Directory 암호 규칙 및 제한](/azure/active-directory/active-directory-passwords-policy)을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-132">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="5e4c1-133">취약한 암호를 사용하거나 암호를 다시 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-133">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="5e4c1-134">`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-134">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5e4c1-135">서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-135">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="5e4c1-136">서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 __직후에__ 다음 명령을 실행하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-136">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="5e4c1-137">인증서 기반 인증</span><span class="sxs-lookup"><span data-stu-id="5e4c1-137">Certificate-based authentication</span></span>

<span data-ttu-id="5e4c1-138">인증서 기반 인증을 사용하는 서비스 주체는 `-CertValue` 매개 변수를 사용하여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-138">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="5e4c1-139">이 매개 변수는 공용 인증서의 base64로 인코딩된 ASCII 문자열을 취합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-139">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="5e4c1-140">이는 PEM 파일 또는 텍스트 인코딩 CRT 또는 CER로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-140">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="5e4c1-141">공용 인증서의 이진 인코딩은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-141">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="5e4c1-142">이러한 명령은 사용할 수 있는 인증서가 이미 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-142">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="5e4c1-143">`PSADKeyCredential` 개체를 사용하는 `-KeyCredential` 매개 변수를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-143">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="5e4c1-144">이러한 객체는 유효한 `StartDate`, `EndDate`가 있어야 하며 `CertValue` 멤버가 공용 인증서의 base64 인코딩 ASCII 문자열로 설정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-144">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="5e4c1-145">`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-145">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="5e4c1-146">서비스 주체로 로그인하는 클라이언트는 인증서의 프라이빗 키에 액세스해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-146">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5e4c1-147">서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-147">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="5e4c1-148">서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 __직후에__ 다음 명령을 실행하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-148">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="5e4c1-149">기존 서비스 주체 가져오기</span><span class="sxs-lookup"><span data-stu-id="5e4c1-149">Get an existing service principal</span></span>

<span data-ttu-id="5e4c1-150">현재 활동 중인 테넌트의 서비스 주체 목록은 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal)을 사용하여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-150">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="5e4c1-151">기본적으로 이 명령은 테넌트의 __모든__ 서비스 주체를 반환하므로 대규모 조직의 경우 결과를 반환하는 데 오랜 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-151">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="5e4c1-152">대신 선택적 서버 측 필터링 인수 중 하나를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="5e4c1-153">`-DisplayNameBeginsWith`은 제공된 값과 일치하는 _접두사_ 가 있는 서비스 주체를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="5e4c1-154">서비스 주체의 표시 이름은 만드는 중에 `-DisplayName`으로 설정된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="5e4c1-155">`-DisplayName`은 서비스 주체 이름과 _정확히 일치하는_ 것을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="5e4c1-156">서비스 주체 역할 관리</span><span class="sxs-lookup"><span data-stu-id="5e4c1-156">Manage service principal roles</span></span>

<span data-ttu-id="5e4c1-157">Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="5e4c1-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5e4c1-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="5e4c1-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5e4c1-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="5e4c1-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5e4c1-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="5e4c1-161">서비스 주체의 기본 역할은 **참가자** 입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-161">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="5e4c1-162">이 역할에는 Azure 계정에서 읽고 쓸 수 있는 모든 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="5e4c1-163">**Reader** (읽기 권한자) 역할은 읽기 전용 액세스 권한으로 더 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-163">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="5e4c1-164">RBAC(역할 기반 액세스 제어)와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="5e4c1-165">다음 예제에서는 **Reader** 역할을 추가하고 **Contributor** (기여자) 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="5e4c1-166">역할 할당 cmdlet은 서비스 사용자 주체 ID를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="5e4c1-167">생성 시 생성되는 관련 애플리케이션 ID를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="5e4c1-168">서비스 주체에 대한 애플리케이션 ID를 가져오려면 `Get-AzADServicePrincipal`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="5e4c1-169">계정에 역할을 할당할 수 있는 권한이 없으면 계정에 "'Microsoft.Authorization/roleAssignments/write' 작업을 수행할 수 있는 권한이 없습니다."라는 오류 메시지가 표시됩니다. 역할을 관리하려면 Azure Active Directory 관리자에게 문의하십시오.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="5e4c1-170">역할을 추가해도 이전에 할당된 권한은 _제한되지 않습니다_.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-170">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="5e4c1-171">서비스 주체 권한을 제한할 때는 __Contributor__ 역할을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-171">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="5e4c1-172">변경 내용은 할당된 역할을 나열하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-172">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="5e4c1-173">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="5e4c1-173">Sign in using a service principal</span></span>

<span data-ttu-id="5e4c1-174">로그인하여 새 서비스 주체의 자격 증명과 권한을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-174">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="5e4c1-175">서비스 주체로 로그인하려면 해당 서비스와 연결된 `applicationId` 값과 이 서비스가 생성된 테넌트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-175">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="5e4c1-176">암호를 사용하는 서비스 주체로 로그인하려면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-176">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="5e4c1-177">인증서 기반 인증을 사용하려면 Azure PowerShell이 인증서 지문을 기반으로 로컬 인증서 저장소에서 정보를 검색할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-177">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="5e4c1-178">PowerShell에서 액세스할 수 있는 자격 증명 저장소로 인증서를 가져오는 방법은 [Azure PowerShell로 로그인](authenticate-azureps.md#sp-signin)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-178">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="5e4c1-179">자격 증명 다시 설정</span><span class="sxs-lookup"><span data-stu-id="5e4c1-179">Reset credentials</span></span>

<span data-ttu-id="5e4c1-180">서비스 주체에 대한 자격 증명을 잊어 버린 경우 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential)을 사용하여 새 자격 증명을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-180">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="5e4c1-181">이 cmdlet은 `New-AzADServicePrincipal`과 동일한 자격 증명 인수 및 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-181">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="5e4c1-182">자격 증명 인수가 없으면 무작위 암호가 있는 새로운 `PasswordCredential`이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-182">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e4c1-183">새 자격 증명을 할당하기 전에 해당 로그인을 방지하기 위해 기존 자격 증명을 제거하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="5e4c1-184">이를 위해서는 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4c1-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
