---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711319"
---
# <span data-ttu-id="ae5d2-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="ae5d2-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="ae5d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5d2-103">Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae5d2-104">SYNTAX</span></span>

### <span data-ttu-id="ae5d2-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae5d2-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae5d2-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae5d2-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae5d2-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae5d2-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="ae5d2-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae5d2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="ae5d2-110">DESCRIPTION</span></span>
<span data-ttu-id="ae5d2-111">Connect-AzureRmAccount cmdlet은 Azure 리소스 관리자 cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="ae5d2-112">이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="ae5d2-113">서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzureAccount 또는 Import-AzurePublishSettingsFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="ae5d2-114">현재 사용자에 대 한 컨텍스트를 찾을 수 없는 경우이 명령은 사용자의 컨텍스트 목록을 해당 하는 각 (처음 25 개) 구독에 대 한 컨텍스트로 채워 집니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="ae5d2-115">사용자에 대해 생성 된 컨텍스트의 목록은 "AzureRmContext-ListAvailable"를 실행 하 여 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="ae5d2-116">이 컨텍스트 채우기를 건너뛰려면 "-SkipContextPopulation" 스위치 매개 변수를 사용 하 여이 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="ae5d2-117">이 cmdlet을 실행 한 후에는 AzureRmAccount을 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="ae5d2-118">예제의</span><span class="sxs-lookup"><span data-stu-id="ae5d2-118">EXAMPLES</span></span>

### <span data-ttu-id="ae5d2-119">예제 1: 대화형 로그인을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ae5d2-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ae5d2-120">이 명령은 Azure 계정에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="ae5d2-121">이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="ae5d2-122">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="ae5d2-123">예제 2: 조직 ID 자격 증명을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ae5d2-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ae5d2-124">첫 번째 명령은 사용자 자격 증명 (사용자 이름 및 암호)을 묻는 메시지를 표시 하 고이를 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="ae5d2-125">두 번째 명령은 $Credential에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="ae5d2-126">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="ae5d2-127">이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="ae5d2-128">예제 3: Azure service principal 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ae5d2-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ae5d2-129">첫 번째 명령은 서비스 사용자 자격 증명 (응용 프로그램 id 및 서비스 사용자 암호)을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="ae5d2-130">두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 된 서비스 사용자 자격 증명을 사용 하 여 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="ae5d2-131">ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="ae5d2-132">예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 대 한 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ae5d2-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ae5d2-133">이 명령은 Azure 계정에 연결 하 고, 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 기본적으로 실행 하도록 AzureRM PowerShell을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="ae5d2-134">예제 5: 관리 서비스 Id 로그인을 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="ae5d2-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ae5d2-135">이 명령은 호스트 환경의 관리 되는 서비스 id (예: 지정 된 관리 되는 서비스 Id를 사용 하 여 VirtualMachine에 실행 되는 경우)를 사용 하 여 연결 하 고,이를 통해 코드에서 지정 된 id로 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="ae5d2-136">예제 6: 인증서를 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="ae5d2-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="ae5d2-137">이 명령은 인증서 기반 서비스 사용자 인증을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="ae5d2-138">인증에 사용 되는 Theservice 주체를 지정 된 인증서로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="ae5d2-139">변수</span><span class="sxs-lookup"><span data-stu-id="ae5d2-139">PARAMETERS</span></span>

### <span data-ttu-id="ae5d2-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="ae5d2-140">-AccessToken</span></span>
<span data-ttu-id="ae5d2-141">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="ae5d2-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-142">-AccountId</span></span>
<span data-ttu-id="ae5d2-143">액세스 토큰의 계정 Id</span><span class="sxs-lookup"><span data-stu-id="ae5d2-143">Account Id for access token</span></span>

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

### <span data-ttu-id="ae5d2-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-144">-ApplicationId</span></span>
<span data-ttu-id="ae5d2-145">수단</span><span class="sxs-lookup"><span data-stu-id="ae5d2-145">SPN</span></span>

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

### <span data-ttu-id="ae5d2-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ae5d2-146">-CertificateThumbprint</span></span>
<span data-ttu-id="ae5d2-147">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="ae5d2-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="ae5d2-148">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="ae5d2-148">-ContextName</span></span>
<span data-ttu-id="ae5d2-149">이 로그인의 기본 컨텍스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-149">Name of the default context from this login.</span></span>  <span data-ttu-id="ae5d2-150">로그인 후이 이름을 기준으로이 컨텍스트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="ae5d2-151">-Credential</span><span class="sxs-lookup"><span data-stu-id="ae5d2-151">-Credential</span></span>
<span data-ttu-id="ae5d2-152">PSCredential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="ae5d2-153">PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="ae5d2-154">PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d2-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5d2-155">-DefaultProfile</span></span>
<span data-ttu-id="ae5d2-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae5d2-157">-환경</span><span class="sxs-lookup"><span data-stu-id="ae5d2-157">-Environment</span></span>
<span data-ttu-id="ae5d2-158">로그인 하는 계정이 포함 된 환경</span><span class="sxs-lookup"><span data-stu-id="ae5d2-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="ae5d2-159">-Force</span><span class="sxs-lookup"><span data-stu-id="ae5d2-159">-Force</span></span>
<span data-ttu-id="ae5d2-160">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="ae5d2-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ae5d2-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ae5d2-161">-GraphAccessToken</span></span>
<span data-ttu-id="ae5d2-162">Graph 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="ae5d2-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="ae5d2-163">-Id</span><span class="sxs-lookup"><span data-stu-id="ae5d2-163">-Identity</span></span>
<span data-ttu-id="ae5d2-164">현재 환경에서 관리 서비스 id를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="ae5d2-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="ae5d2-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="ae5d2-166">KeyVault 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="ae5d2-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="ae5d2-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="ae5d2-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="ae5d2-168">관리 서비스 로그인에 대 한 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ae5d2-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="ae5d2-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="ae5d2-169">-ManagedServicePort</span></span>
<span data-ttu-id="ae5d2-170">관리 서비스 로그인의 포트 번호</span><span class="sxs-lookup"><span data-stu-id="ae5d2-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="ae5d2-171">-Managed서비스 Ecret</span><span class="sxs-lookup"><span data-stu-id="ae5d2-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="ae5d2-172">특정 종류의 관리 서비스 로그인에 사용 되는 비밀.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="ae5d2-173">-범위</span><span class="sxs-lookup"><span data-stu-id="ae5d2-173">-Scope</span></span>
<span data-ttu-id="ae5d2-174">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ae5d2-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ae5d2-175">-ServicePrincipal</span></span>
<span data-ttu-id="ae5d2-176">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="ae5d2-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="ae5d2-177">-SkipContextPopulation</span></span>
<span data-ttu-id="ae5d2-178">컨텍스트를 찾을 수 없는 경우 컨텍스트 채우기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="ae5d2-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="ae5d2-179">-SkipValidation</span></span>
<span data-ttu-id="ae5d2-180">액세스 토큰에 대 한 유효성 검사 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="ae5d2-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="ae5d2-181">-구독</span><span class="sxs-lookup"><span data-stu-id="ae5d2-181">-Subscription</span></span>
<span data-ttu-id="ae5d2-182">구독 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="ae5d2-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="ae5d2-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ae5d2-183">-TenantId</span></span>
<span data-ttu-id="ae5d2-184">선택적 도메인 이름 또는 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="ae5d2-185">도메인 이름은 모든 로그인 상황에서 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="ae5d2-186">CSP (Cloud Solution Provider) 로그인의 경우 테 넌 트 ID가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5d2-187">-확인</span><span class="sxs-lookup"><span data-stu-id="ae5d2-187">-Confirm</span></span>
<span data-ttu-id="ae5d2-188">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae5d2-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5d2-189">-WhatIf</span></span>
<span data-ttu-id="ae5d2-190">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae5d2-191">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae5d2-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5d2-192">CommonParameters</span></span>
<span data-ttu-id="ae5d2-193">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae5d2-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5d2-194">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5d2-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5d2-195">입력</span><span class="sxs-lookup"><span data-stu-id="ae5d2-195">INPUTS</span></span>

### <span data-ttu-id="ae5d2-196">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae5d2-196">System.String</span></span>
<span data-ttu-id="ae5d2-197">매개 변수: 구독 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae5d2-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="ae5d2-198">출력</span><span class="sxs-lookup"><span data-stu-id="ae5d2-198">OUTPUTS</span></span>

### <span data-ttu-id="ae5d2-199">Microsoft. Azure. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ae5d2-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="ae5d2-200">상속자</span><span class="sxs-lookup"><span data-stu-id="ae5d2-200">NOTES</span></span>

## <span data-ttu-id="ae5d2-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae5d2-201">RELATED LINKS</span></span>
