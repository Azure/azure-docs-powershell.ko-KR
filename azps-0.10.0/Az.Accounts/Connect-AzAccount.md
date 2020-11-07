---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875314"
---
# <span data-ttu-id="e557a-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e557a-101">Connect-AzAccount</span></span>

## <span data-ttu-id="e557a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e557a-102">SYNOPSIS</span></span>
<span data-ttu-id="e557a-103">Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="e557a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e557a-104">SYNTAX</span></span>

### <span data-ttu-id="e557a-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e557a-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e557a-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e557a-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e557a-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="e557a-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e557a-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e557a-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e557a-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e557a-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e557a-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="e557a-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e557a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="e557a-111">DESCRIPTION</span></span>
<span data-ttu-id="e557a-112">Connect-AzAccount cmdlet은 Azure 리소스 관리자 cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="e557a-113">이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="e557a-114">서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzAccount 또는 Import-AzPublishSettingsFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="e557a-115">현재 사용자에 대 한 컨텍스트를 찾을 수 없는 경우이 명령은 사용자의 컨텍스트 목록을 해당 하는 각 (처음 25 개) 구독에 대 한 컨텍스트로 채워 집니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="e557a-116">사용자에 대해 생성 된 컨텍스트의 목록은 "AzContext-ListAvailable"를 실행 하 여 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="e557a-117">이 컨텍스트 채우기를 건너뛰려면 "-SkipContextPopulation" 스위치 매개 변수를 사용 하 여이 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="e557a-118">이 cmdlet을 실행 한 후에는 AzAccount을 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="e557a-119">예제의</span><span class="sxs-lookup"><span data-stu-id="e557a-119">EXAMPLES</span></span>

### <span data-ttu-id="e557a-120">예제 1: 대화형 로그인을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="e557a-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-121">이 명령은 Azure 계정에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="e557a-122">이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="e557a-123">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="e557a-124">예제 2: (Windows PowerShell 5.1에만 해당) 조직 ID 자격 증명을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="e557a-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-125">이 시나리오는 Windows PowerShell 5.1 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="e557a-126">첫 번째 명령은 사용자 자격 증명 (사용자 이름 및 암호)을 묻는 메시지를 표시 하 고이를 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="e557a-127">두 번째 명령은 $Credential에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="e557a-128">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="e557a-129">이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="e557a-130">예제 3: Azure service principal 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="e557a-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-131">첫 번째 명령은 서비스 사용자 자격 증명 (응용 프로그램 id 및 서비스 사용자 암호)을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="e557a-132">두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 된 서비스 사용자 자격 증명을 사용 하 여 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="e557a-133">ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="e557a-134">예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 대 한 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="e557a-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-135">이 명령은 Azure 계정에 연결 하 고, 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 기본적으로 실행 하도록 AzureRM PowerShell을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="e557a-136">예제 5: 관리 서비스 Id 로그인을 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e557a-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-137">이 명령은 호스트 환경의 관리 되는 서비스 id (예: 지정 된 관리 되는 서비스 Id를 사용 하 여 VirtualMachine에 실행 되는 경우)를 사용 하 여 연결 하 고,이를 통해 코드에서 지정 된 id로 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="e557a-138">예제 6: 관리 서비스 Id 로그인 및 ClientId를 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e557a-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-139">이 명령은 사용자가 할당 한 Id를 가상 컴퓨터에 추가한 다음 사용자가 할당 한 Id의 ClientId를 사용 하 여 연결 하 여 "myUserAssignedIdentity"의 관리 되는 서비스 id를 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="e557a-140">관리 Id 구성에 대 한 자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm</span><span class="sxs-lookup"><span data-stu-id="e557a-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="e557a-141">예제 7: 관리 서비스 Id 로그인 및 ClientId를 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e557a-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-142">이 명령은 사용자가 할당 한 Id를 가상 컴퓨터에 추가한 다음 사용자가 할당 한 Id의 Id를 사용 하 여 연결 하 여 "myUserAssignedIdentity"의 관리 되는 서비스 id를 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="e557a-143">관리 Id 구성에 대 한 자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm</span><span class="sxs-lookup"><span data-stu-id="e557a-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="e557a-144">예제 8: 인증서를 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e557a-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="e557a-145">이 명령은 인증서 기반 서비스 사용자 인증을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="e557a-146">인증에 사용 되는 서비스 사용자를 지정 된 인증서로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="e557a-147">예제 9: AccessToken 인증을 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e557a-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="e557a-148">이 명령은 제공 된 AccessToken 및 KeyVaultAccessToken를 사용 하 여 "AccountId"에 지정 된 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="e557a-149">변수</span><span class="sxs-lookup"><span data-stu-id="e557a-149">PARAMETERS</span></span>

### <span data-ttu-id="e557a-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e557a-150">-AccessToken</span></span>
<span data-ttu-id="e557a-151">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="e557a-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e557a-152">-AccountId</span></span>
<span data-ttu-id="e557a-153">AccessToken 매개 변수 집합의 액세스 토큰에 대 한 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="e557a-154">ManagedService 매개 변수 집합의 관리 서비스에 대 한 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="e557a-155">관리 서비스 리소스 Id 또는 연결 된 클라이언트 id 일 수 있습니다. 지정 된 SystemAssigned를 사용 하려면이 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="e557a-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e557a-156">-ApplicationId</span></span>
<span data-ttu-id="e557a-157">수단</span><span class="sxs-lookup"><span data-stu-id="e557a-157">SPN</span></span>

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

### <span data-ttu-id="e557a-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e557a-158">-CertificateThumbprint</span></span>
<span data-ttu-id="e557a-159">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="e557a-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="e557a-160">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="e557a-160">-ContextName</span></span>
<span data-ttu-id="e557a-161">이 로그인의 기본 컨텍스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-161">Name of the default context from this login.</span></span>  <span data-ttu-id="e557a-162">로그인 후이 이름을 기준으로이 컨텍스트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="e557a-163">-Credential</span><span class="sxs-lookup"><span data-stu-id="e557a-163">-Credential</span></span>
<span data-ttu-id="e557a-164">PSCredential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="e557a-165">PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="e557a-166">PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="e557a-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e557a-167">-DefaultProfile</span></span>
<span data-ttu-id="e557a-168">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e557a-169">-환경</span><span class="sxs-lookup"><span data-stu-id="e557a-169">-Environment</span></span>
<span data-ttu-id="e557a-170">로그인 하는 계정이 포함 된 환경</span><span class="sxs-lookup"><span data-stu-id="e557a-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="e557a-171">-Force</span><span class="sxs-lookup"><span data-stu-id="e557a-171">-Force</span></span>
<span data-ttu-id="e557a-172">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="e557a-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="e557a-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="e557a-173">-GraphAccessToken</span></span>
<span data-ttu-id="e557a-174">Graph 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="e557a-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="e557a-175">-Id</span><span class="sxs-lookup"><span data-stu-id="e557a-175">-Identity</span></span>
<span data-ttu-id="e557a-176">현재 환경에서 관리 서비스 id를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="e557a-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="e557a-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="e557a-178">KeyVault 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="e557a-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="e557a-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="e557a-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="e557a-180">관리 서비스 로그인에 대 한 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="e557a-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="e557a-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="e557a-181">-ManagedServicePort</span></span>
<span data-ttu-id="e557a-182">관리 서비스 로그인의 포트 번호</span><span class="sxs-lookup"><span data-stu-id="e557a-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="e557a-183">-Managed서비스 Ecret</span><span class="sxs-lookup"><span data-stu-id="e557a-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="e557a-184">특정 종류의 관리 서비스 로그인에 사용 되는 비밀.</span><span class="sxs-lookup"><span data-stu-id="e557a-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="e557a-185">-범위</span><span class="sxs-lookup"><span data-stu-id="e557a-185">-Scope</span></span>
<span data-ttu-id="e557a-186">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e557a-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e557a-187">-ServicePrincipal</span></span>
<span data-ttu-id="e557a-188">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="e557a-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="e557a-189">-SkipContextPopulation</span></span>
<span data-ttu-id="e557a-190">컨텍스트를 찾을 수 없는 경우 컨텍스트 채우기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="e557a-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="e557a-191">-SkipValidation</span></span>
<span data-ttu-id="e557a-192">액세스 토큰에 대 한 유효성 검사 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="e557a-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="e557a-193">-구독</span><span class="sxs-lookup"><span data-stu-id="e557a-193">-Subscription</span></span>
<span data-ttu-id="e557a-194">구독 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="e557a-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="e557a-195">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="e557a-195">-Tenant</span></span>
<span data-ttu-id="e557a-196">선택적 테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="e557a-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="e557a-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="e557a-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="e557a-198">브라우저 컨트롤 대신 장치 코드 인증 사용</span><span class="sxs-lookup"><span data-stu-id="e557a-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="e557a-199">-확인</span><span class="sxs-lookup"><span data-stu-id="e557a-199">-Confirm</span></span>
<span data-ttu-id="e557a-200">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e557a-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e557a-201">-WhatIf</span></span>
<span data-ttu-id="e557a-202">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e557a-203">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e557a-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e557a-204">CommonParameters</span></span>
<span data-ttu-id="e557a-205">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e557a-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e557a-206">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e557a-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e557a-207">입력</span><span class="sxs-lookup"><span data-stu-id="e557a-207">INPUTS</span></span>

### <span data-ttu-id="e557a-208">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e557a-208">System.String</span></span>

## <span data-ttu-id="e557a-209">출력</span><span class="sxs-lookup"><span data-stu-id="e557a-209">OUTPUTS</span></span>

### <span data-ttu-id="e557a-210">Microsoft. Azure. a PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e557a-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="e557a-211">상속자</span><span class="sxs-lookup"><span data-stu-id="e557a-211">NOTES</span></span>

## <span data-ttu-id="e557a-212">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e557a-212">RELATED LINKS</span></span>
