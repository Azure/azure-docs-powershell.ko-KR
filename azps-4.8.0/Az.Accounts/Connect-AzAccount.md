---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 073a70077eabbdf20d72874b22c11b7f0dae2844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211937"
---
# <span data-ttu-id="c71b8-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c71b8-101">Connect-AzAccount</span></span>

## <span data-ttu-id="c71b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c71b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c71b8-103">Az PowerShell 모듈에서 cmdlet과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="c71b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c71b8-104">SYNTAX</span></span>

### <span data-ttu-id="c71b8-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="c71b8-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c71b8-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c71b8-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c71b8-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="c71b8-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c71b8-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c71b8-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c71b8-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c71b8-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c71b8-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="c71b8-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c71b8-111">설명은</span><span class="sxs-lookup"><span data-stu-id="c71b8-111">DESCRIPTION</span></span>

<span data-ttu-id="c71b8-112">이 `Connect-AzAccount` cmdlet은 Az PowerShell 모듈에서 cmdlet과 함께 사용할 수 있도록 인증 된 계정을 사용 하 여 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="c71b8-113">Azure Resource Manager 요청과 함께이 인증 된 계정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="c71b8-114">서비스 관리에 사용할 인증 된 계정을 추가 하려면 `Add-AzureAccount` Azure PowerShell 모듈에서 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="c71b8-115">현재 사용자에 대 한 컨텍스트를 찾을 수 없는 경우 사용자의 컨텍스트 목록은 처음 25 개의 각 구독에 대 한 컨텍스트로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="c71b8-116">사용자에 대해 생성 된 컨텍스트 목록은를 실행 하 여 찾을 수 있습니다 `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="c71b8-117">이 컨텍스트 채우기를 건너뛰려면 **Skipcontextpopulation** 스위치 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="c71b8-118">이 cmdlet을 실행 한 후를 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다 `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="c71b8-119">예제의</span><span class="sxs-lookup"><span data-stu-id="c71b8-119">EXAMPLES</span></span>

### <span data-ttu-id="c71b8-120">예제 1: Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="c71b8-121">이 예제에서는 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-121">This example connects to an Azure account.</span></span> <span data-ttu-id="c71b8-122">Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="c71b8-123">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-124">예제 2: (Windows PowerShell 5.1에만 해당) 조직 ID 자격 증명을 사용 하 여 Azure에 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="c71b8-125">이 시나리오는 Windows PowerShell 5.1 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="c71b8-126">첫 번째 명령은 사용자 자격 증명을 묻는 메시지를 표시 하 고 변수에 저장 합니다 `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c71b8-127">두 번째 명령은에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다 `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="c71b8-128">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-129">예제 3: 서비스 사용자 계정을 사용 하 여 Azure에 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="c71b8-130">첫 번째 명령은 사용자 자격 증명을 입력 하 라는 메시지를 표시 하 고 변수에 저장 합니다 `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c71b8-131">메시지가 표시 되 면 사용자 이름 및 서비스 사용자 암호에 대 한 응용 프로그램 ID를 암호로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="c71b8-132">두 번째 명령은 변수에 저장 된 서비스 사용자 자격 증명을 사용 하 여 지정 된 Azure 테 넌 트를 연결 합니다 `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="c71b8-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="c71b8-133">**Serviceprincipal** switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-134">예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="c71b8-135">이 예제에서는 지정 된 테 넌 트 및 구독을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-136">예제 5: 관리 서비스 Id를 사용 하 여 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="c71b8-137">이 예제에서는 호스트 환경의 MSI (관리 서비스 Id)를 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="c71b8-138">예를 들어 MSI를 할당 한 가상 컴퓨터에서 Azure에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-139">예제 6: 관리 서비스 Id 로그인 및 ClientId를 사용 하 여 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="c71b8-140">이 예제에서는 **myUserAssignedIdentity** 의 관리 되는 서비스 id를 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="c71b8-141">사용자가 할당 한 id를 가상 컴퓨터에 추가 하 고 사용자가 할당 한 id의 ClientId를 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="c71b8-142">자세한 내용은 [AZURE VM에서 azure 리소스의 관리 되는 Id 구성을](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c71b8-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c71b8-143">예제 7: 인증서를 사용 하 여 연결</span><span class="sxs-lookup"><span data-stu-id="c71b8-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="c71b8-144">이 예제에서는 인증서 기반 서비스 사용자 인증을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="c71b8-145">인증에 사용 되는 서비스 사용자를 지정 된 인증서를 사용 하 여 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="c71b8-146">자체 서명 된 인증서를 만들고 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [Azure PowerShell을 사용 하 여 인증서로 서비스 사용자 만들기를](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c71b8-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="c71b8-147">변수</span><span class="sxs-lookup"><span data-stu-id="c71b8-147">PARAMETERS</span></span>

### <span data-ttu-id="c71b8-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="c71b8-148">-AccessToken</span></span>

<span data-ttu-id="c71b8-149">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="c71b8-150">액세스 토큰은 자격 증명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="c71b8-151">적절 한 보안 예방 조치를 사용 하 여 기밀을 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="c71b8-152">또한 액세스 토큰은 시간 제한을 초과 하며 장기 실행 작업이 완료 되지 못하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="c71b8-153">-AccountId</span></span>

<span data-ttu-id="c71b8-154">**AccessToken** 매개 변수 집합의 액세스 토큰에 대 한 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="c71b8-155">**Managedservice** 매개 변수 집합의 관리 서비스에 대 한 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="c71b8-156">관리 서비스 리소스 ID 또는 연결 된 클라이언트 ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="c71b8-157">시스템에 할당 된 id를 사용 하려면이 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c71b8-158">-ApplicationId</span></span>

<span data-ttu-id="c71b8-159">서비스 사용자의 응용 프로그램 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c71b8-160">-CertificateThumbprint</span></span>

<span data-ttu-id="c71b8-161">인증서 해시 또는 지문.</span><span class="sxs-lookup"><span data-stu-id="c71b8-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-162">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="c71b8-162">-ContextName</span></span>

<span data-ttu-id="c71b8-163">이 로그인에 대 한 기본 Azure 컨텍스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="c71b8-164">Azure 컨텍스트에 대 한 자세한 내용은 [Azure PowerShell 컨텍스트 개체](/powershell/azure/context-persistence)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c71b8-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="c71b8-165">-Credential</span></span>

<span data-ttu-id="c71b8-166">**PSCredential** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="c71b8-167">**PSCredential** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Credential` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="c71b8-168">**PSCredential** 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 id 및 비밀에 대 한 사용자 id 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71b8-169">-DefaultProfile</span></span>

<span data-ttu-id="c71b8-170">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c71b8-171">-환경</span><span class="sxs-lookup"><span data-stu-id="c71b8-171">-Environment</span></span>

<span data-ttu-id="c71b8-172">Azure 계정을 포함 하는 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-173">-Force</span><span class="sxs-lookup"><span data-stu-id="c71b8-173">-Force</span></span>

<span data-ttu-id="c71b8-174">메시지를 표시 하지 않고 같은 이름으로 기존 컨텍스트를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-174">Overwrite the existing context with the same name without prompting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c71b8-175">-GraphAccessToken</span></span>

<span data-ttu-id="c71b8-176">Graph 서비스에 대 한 AccessToken.</span><span class="sxs-lookup"><span data-stu-id="c71b8-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-177">-Id</span><span class="sxs-lookup"><span data-stu-id="c71b8-177">-Identity</span></span>

<span data-ttu-id="c71b8-178">관리 서비스 Id를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="c71b8-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="c71b8-180">KeyVault 서비스에 대 한 AccessToken.</span><span class="sxs-lookup"><span data-stu-id="c71b8-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="c71b8-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="c71b8-182">관리 서비스의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-182">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="c71b8-183">-ManagedServicePort</span></span>

<span data-ttu-id="c71b8-184">관리 서비스의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-184">Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-185">-Managed서비스 Ecret</span><span class="sxs-lookup"><span data-stu-id="c71b8-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="c71b8-186">관리 서비스 로그인에 대 한 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-186">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-187">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c71b8-187">-MaxContextPopulation</span></span>

<span data-ttu-id="c71b8-188">로그인 후 컨텍스트를 채우는 최대 구독 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-188">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="c71b8-189">기본값은 25입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-189">Default is 25.</span></span> <span data-ttu-id="c71b8-190">모든 구독을 컨텍스트에 채우려면-1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-190">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-191">-범위</span><span class="sxs-lookup"><span data-stu-id="c71b8-191">-Scope</span></span>

<span data-ttu-id="c71b8-192">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-192">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-193">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c71b8-193">-ServicePrincipal</span></span>

<span data-ttu-id="c71b8-194">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-194">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-195">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c71b8-195">-SkipContextPopulation</span></span>

<span data-ttu-id="c71b8-196">컨텍스트를 찾을 수 없는 경우 컨텍스트 채우기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-196">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-197">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="c71b8-197">-SkipValidation</span></span>

<span data-ttu-id="c71b8-198">액세스 토큰에 대 한 유효성 검사를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-198">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-199">-구독</span><span class="sxs-lookup"><span data-stu-id="c71b8-199">-Subscription</span></span>

<span data-ttu-id="c71b8-200">구독 이름 또는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-200">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-201">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="c71b8-201">-Tenant</span></span>

<span data-ttu-id="c71b8-202">선택적 테 넌 트 이름 또는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-202">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="c71b8-203">현재 API의 제한 사항으로 인해 B2B (비즈니스 간) 계정으로 연결할 때 테 넌 트 이름 대신 테 넌 트 ID를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-203">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-204">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="c71b8-204">-UseDeviceAuthentication</span></span>

<span data-ttu-id="c71b8-205">브라우저 컨트롤 대신 디바이스 코드 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-205">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="c71b8-206">PowerShell 버전 6 이상에 대 한 기본 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-206">This is the default authentication type for PowerShell version 6 and higher.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-207">-확인</span><span class="sxs-lookup"><span data-stu-id="c71b8-207">-Confirm</span></span>

<span data-ttu-id="c71b8-208">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-208">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71b8-209">-WhatIf</span></span>

<span data-ttu-id="c71b8-210">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c71b8-211">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-211">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b8-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71b8-212">CommonParameters</span></span>
<span data-ttu-id="c71b8-213">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c71b8-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71b8-214">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c71b8-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71b8-215">입력</span><span class="sxs-lookup"><span data-stu-id="c71b8-215">INPUTS</span></span>

### <span data-ttu-id="c71b8-216">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c71b8-216">System.String</span></span>

## <span data-ttu-id="c71b8-217">출력</span><span class="sxs-lookup"><span data-stu-id="c71b8-217">OUTPUTS</span></span>

### <span data-ttu-id="c71b8-218">Microsoft. Azure. a PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c71b8-218">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="c71b8-219">상속자</span><span class="sxs-lookup"><span data-stu-id="c71b8-219">NOTES</span></span>

## <span data-ttu-id="c71b8-220">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c71b8-220">RELATED LINKS</span></span>
