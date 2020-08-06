---
title: Azure PowerShell로 로그인
description: Azure PowerShell 사용자나 서비스 주체로 로그인 또는 Azure 리소스에 대한 관리 ID로 로그인하는 방법.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.openlocfilehash: 7ac723202ca9e81c8ef4cba5e844d46b98ba4b67
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566441"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="f4317-103">Azure PowerShell로 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="f4317-104">Azure PowerShell에서는 여러 인증 방법을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="f4317-105">시작하는 가장 쉬운 방법은 [Azure Cloud Shell](/azure/cloud-shell/overview)을 사용하는 것으로서, 자동으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="f4317-106">로컬 설치에서는, 브라우저를 통해 대화형으로 로그인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="f4317-107">자동화 스크립트를 작성할 때 권장되는 방법은 필요한 권한이 있는 [서비스 주체](create-azure-service-principal-azureps.md)를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="f4317-108">사용 사례에 대해 로그인 권한을 가능한 한 많이 제한하면 Azure 리소스를 안전하게 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="f4317-109">처음에 두 개 이상의 구독에 액세스할 수 있는 경우 첫 번째 구독에 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="f4317-110">명령은 기본적으로 이 구독에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="f4317-111">세션에 대한 활성 구독을 변경하려면 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="f4317-112">활성 구독을 변경하고 동일한 시스템의 세션 간에 지속되도록 하려면 [AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4317-113">로그인한 상태를 유지하는 한, 여러 PowerShell 세션에서 자격 증명을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="f4317-114">자세한 내용은 [영구 자격 증명](context-persistence.md)에 대한 아티클을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="f4317-115">대화형으로 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-115">Sign in interactively</span></span>

<span data-ttu-id="f4317-116">대화형으로 로그인하려면 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="f4317-117">이 cmdlet은 PowerShell 버전 6 이상에서 실행할 경우 토큰 문자열을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="f4317-118">로그인하려면 이 문자열을 복사하여 웹 브라우저에서 [microsoft.com/devicelogin](https://microsoft.com/devicelogin)에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="f4317-119">그러면 PowerShell 세션이 인증되어 Azure에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="f4317-120">Windows PowerShell에서 토큰 문자열을 받도록 `UseDeviceAuthentication` 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4317-121">Active Directory Domain Services 인증 구현 및 보안 문제의 변경으로 인해 Azure PowerShell에서 사용자 이름/암호 자격 증명이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="f4317-122">자동화 목적으로 자격 증명 권한 부여를 사용하는 경우 대신 [서비스 주체](create-azure-service-principal-azureps.md)를 생성하세요.</span><span class="sxs-lookup"><span data-stu-id="f4317-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f4317-123">[Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet을 사용하여 테넌트 ID를 이 문서의 다음 두 섹션에서 사용할 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="f4317-124">서비스 주체 <a name="sp-signin"/>으로 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="f4317-125">서비스 주체는 비대화형 Azure 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="f4317-126">다른 사용자 계정과 마찬가지로 해당 권한은 Azure Active Directory를 사용하여 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="f4317-127">서비스 주체에 필요한 권한만 부여하여 자동화 스크립트 보안을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="f4317-128">Azure PowerShell에 사용할 서비스 주체를 생성하는 방법을 보려면 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](create-azure-service-principal-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4317-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f4317-129">서비스 주체로 로그인하려면 `Connect-AzAccount` cmdlet `-ServicePrincipal`인수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="f4317-130">또한 서비스 주체의 애플리케이션 ID, 로그인 자격 증명 및 서비스 주체와 연결된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="f4317-131">서비스 보안 주체로 로그인하는 방법은 암호 기반 또는 인증서 기반 인증 중 어떤 것으로 구성되어 있는지에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="f4317-132">암호 기반 인증</span><span class="sxs-lookup"><span data-stu-id="f4317-132">Password-based authentication</span></span>

<span data-ttu-id="f4317-133">이 섹션의 예제에서 사용할 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="f4317-134">서비스 주체 만들기에 대한 자세한 내용은 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](/powershell/azure/create-azure-service-principal-azureps)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4317-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f4317-135">서비스 주체의 자격 증명을 적절한 개체로 가져오려면 [Get-credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="f4317-136">이 cmdlet은 사용자 이름 및 암호를 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="f4317-137">서비스 주체의 `applicationID`를 사용자 이름으로 사용하고 해당 `secret`을 암호의 일반 텍스트로 변환하세요.</span><span class="sxs-lookup"><span data-stu-id="f4317-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f4317-138">자동화 시나리오의 경우 다음과 같이 서비스 주체의 `applicationId` 및 `secret`에서 자격 증명을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f4317-139">서비스 주체 연결을 자동화할 때 좋은 암호 스토리지 방법을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="f4317-140">인증서 기반 인증</span><span class="sxs-lookup"><span data-stu-id="f4317-140">Certificate-based authentication</span></span>

<span data-ttu-id="f4317-141">인증서 기반 인증을 사용하려면 Azure PowerShell이 인증서 지문을 기반으로 로컬 인증서 저장소에서 정보를 검색할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f4317-142">등록된 애플리케이션 대신 서비스 주체를 사용하는 경우 `-ServicePrincipal` 인수를 추가하고 서비스 주체의 애플리케이션 ID를 `-ApplicationId` 매개 변수 값으로 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f4317-143">PowerShell 5.1에서 인증서 저장소는 [PKI](/powershell/module/pkiclient) 모듈을 사용하여 관리하고 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="f4317-144">PowerShell Core 6.x 이상에서는 프로세스가 더 복잡합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="f4317-145">다음 스크립트는 기존 인증서를 PowerShell에서 액세스할 수 있는 인증서 저장소로 가져오는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="f4317-146">PowerShell 5.1에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4317-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="f4317-147">PowerShell Core 6.x 이상에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4317-147">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="f4317-148">관리 ID를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-148">Sign in using a managed identity</span></span>

<span data-ttu-id="f4317-149">관리 ID는 Azure Active Directory의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="f4317-150">관리 ID는 Azure에서 실행되는 리소스에 할당된 서비스 주체입니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="f4317-151">로그인에 관리 ID 서비스 주체를 사용할 수 있으며, 다른 리소스에 액세스하려면 앱 전용 액세스 토큰이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="f4317-152">관리 ID는 Azure 클라우드에서 실행되는 리소스에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="f4317-153">이 예제에서는 호스트 환경의 관리 ID를 사용하여 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="f4317-154">예를 들어, 관리 서비스 ID가 할당된 VirtualMachine에서 실행하는 경우 할당된 해당 ID를 사용하여 코드가 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="f4317-155">기본이 아닌 테넌트를 사용하여 로그인하거나 클라우드 솔루션 공급자(CSP)로 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="f4317-156">계정이 두 개 이상의 테넌트와 연결된 경우 로그인하려면 연결할 때 `-Tenant` 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="f4317-157">이 매개 변수는 모든 로그인 메서드에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="f4317-158">로그인할 때 이 매개 변수 값은 테넌트의 Azure 개체 ID(테넌트 ID) 또는 테넌트의 정규화된 도메인 이름이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="f4317-159">[클라우드 솔루션 공급자(CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)의 경우 `-Tenant` 값은 **반드시** 테넌트 ID여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="f4317-160">다른 클라우드로 로그인</span><span class="sxs-lookup"><span data-stu-id="f4317-160">Sign in to another Cloud</span></span>

<span data-ttu-id="f4317-161">Azure 클라우드 서비스는 지역 데이터 처리법을 준수하는 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="f4317-162">지역별 클라우드의 계정에 대해 로그인할 때 `-Environment` 인수를 사용해서 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="f4317-163">이 매개 변수는 모든 로그인 메서드에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="f4317-164">예를 들어 계정이 중국 클라우드에 있는 경우:</span><span class="sxs-lookup"><span data-stu-id="f4317-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="f4317-165">다음 명령은 사용 가능한 환경 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4317-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
