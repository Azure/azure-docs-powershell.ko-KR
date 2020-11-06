---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525036"
---
# <span data-ttu-id="1f288-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="1f288-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="1f288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f288-102">SYNOPSIS</span></span>
<span data-ttu-id="1f288-103">Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f288-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f288-104">SYNTAX</span></span>

### <span data-ttu-id="1f288-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f288-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f288-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f288-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f288-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f288-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f288-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f288-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f288-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="1f288-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f288-110">설명은</span><span class="sxs-lookup"><span data-stu-id="1f288-110">DESCRIPTION</span></span>
<span data-ttu-id="1f288-111">Connect-AzureRmAccount cmdlet은 Azure 리소스 관리자 cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="1f288-112">이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="1f288-113">서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzureAccount 또는 Import-AzurePublishSettingsFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="1f288-114">이 cmdlet을 실행 한 후에는 AzureRmAccount을 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="1f288-115">예제의</span><span class="sxs-lookup"><span data-stu-id="1f288-115">EXAMPLES</span></span>

### <span data-ttu-id="1f288-116">예제 1: 대화형 로그인을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="1f288-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f288-117">이 명령은 Azure 계정에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="1f288-118">이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="1f288-119">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="1f288-120">예제 2: 조직 ID 자격 증명을 사용 하 여 Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="1f288-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f288-121">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="1f288-122">두 번째 명령은 $Credential에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="1f288-123">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="1f288-124">이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="1f288-125">예제 3: Azure service principal 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="1f288-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f288-126">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="1f288-127">두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 된 서비스 사용자 자격 증명을 사용 하 여 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="1f288-128">ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="1f288-129">예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 대 한 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="1f288-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f288-130">이 명령은 Azure 계정에 연결 하 고, 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 기본적으로 실행 하도록 AzureRM PowerShell을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="1f288-131">예제 5: 관리 서비스 Id 로그인을 사용 하 여 계정 추가</span><span class="sxs-lookup"><span data-stu-id="1f288-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f288-132">이 명령은 호스트 환경의 관리 되는 서비스 id를 사용 하 여 기록 합니다 (예: 지정 된 관리 되는 서비스 Id를 사용 하 여 VirtualMachine에서 실행 되는 경우 해당 id를 사용 하 여 코드에 로그인 할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="1f288-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="1f288-133">변수</span><span class="sxs-lookup"><span data-stu-id="1f288-133">PARAMETERS</span></span>

### <span data-ttu-id="1f288-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="1f288-134">-AccessToken</span></span>
<span data-ttu-id="1f288-135">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1f288-136">-AccountId</span></span>
<span data-ttu-id="1f288-137">액세스 토큰의 계정 Id</span><span class="sxs-lookup"><span data-stu-id="1f288-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1f288-138">-ApplicationId</span></span>
<span data-ttu-id="1f288-139">수단</span><span class="sxs-lookup"><span data-stu-id="1f288-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1f288-140">-CertificateThumbprint</span></span>
<span data-ttu-id="1f288-141">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="1f288-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-142">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="1f288-142">-ContextName</span></span>
<span data-ttu-id="1f288-143">이 로그인의 기본 컨텍스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-143">Name of the default context from this login.</span></span>  <span data-ttu-id="1f288-144">로그인 후이 이름을 기준으로이 컨텍스트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-145">-Credential</span><span class="sxs-lookup"><span data-stu-id="1f288-145">-Credential</span></span>
<span data-ttu-id="1f288-146">PSCredential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="1f288-147">PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="1f288-148">PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f288-149">-DefaultProfile</span></span>
<span data-ttu-id="1f288-150">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-151">-환경</span><span class="sxs-lookup"><span data-stu-id="1f288-151">-Environment</span></span>
<span data-ttu-id="1f288-152">로그인 하는 계정이 포함 된 환경</span><span class="sxs-lookup"><span data-stu-id="1f288-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-153">-Force</span><span class="sxs-lookup"><span data-stu-id="1f288-153">-Force</span></span>
<span data-ttu-id="1f288-154">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="1f288-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="1f288-155">-GraphAccessToken</span></span>
<span data-ttu-id="1f288-156">Graph 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="1f288-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-157">-Id</span><span class="sxs-lookup"><span data-stu-id="1f288-157">-Identity</span></span>
<span data-ttu-id="1f288-158">현재 환경에서 관리 서비스 id를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="1f288-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="1f288-160">KeyVault 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="1f288-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="1f288-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="1f288-162">관리 서비스 로그인에 대 한 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="1f288-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="1f288-163">-ManagedServicePort</span></span>
<span data-ttu-id="1f288-164">관리 서비스 로그인의 포트 번호</span><span class="sxs-lookup"><span data-stu-id="1f288-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-165">-범위</span><span class="sxs-lookup"><span data-stu-id="1f288-165">-Scope</span></span>
<span data-ttu-id="1f288-166">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f288-167">-ServicePrincipal</span></span>
<span data-ttu-id="1f288-168">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="1f288-169">-SkipValidation</span></span>
<span data-ttu-id="1f288-170">액세스 토큰에 대 한 유효성 검사 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="1f288-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-171">-구독</span><span class="sxs-lookup"><span data-stu-id="1f288-171">-Subscription</span></span>
<span data-ttu-id="1f288-172">구독 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="1f288-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-173">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1f288-173">-TenantId</span></span>
<span data-ttu-id="1f288-174">선택적 테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="1f288-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-175">-확인</span><span class="sxs-lookup"><span data-stu-id="1f288-175">-Confirm</span></span>
<span data-ttu-id="1f288-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f288-177">-WhatIf</span></span>
<span data-ttu-id="1f288-178">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f288-179">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f288-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f288-180">CommonParameters</span></span>
<span data-ttu-id="1f288-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f288-182">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f288-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f288-183">입력</span><span class="sxs-lookup"><span data-stu-id="1f288-183">INPUTS</span></span>

### <span data-ttu-id="1f288-184">이름</span><span class="sxs-lookup"><span data-stu-id="1f288-184">String</span></span>
<span data-ttu-id="1f288-185">' SubscriptionId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1f288-186">이름</span><span class="sxs-lookup"><span data-stu-id="1f288-186">String</span></span>
<span data-ttu-id="1f288-187">' SubscriptionName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f288-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1f288-188">출력</span><span class="sxs-lookup"><span data-stu-id="1f288-188">OUTPUTS</span></span>

### <span data-ttu-id="1f288-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="1f288-189">PSAzureProfile</span></span>
<span data-ttu-id="1f288-190">로그인 한 사용자에 대 한 자격 증명, 구독, 계정 및 테 넌 트 정보</span><span class="sxs-lookup"><span data-stu-id="1f288-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="1f288-191">상속자</span><span class="sxs-lookup"><span data-stu-id="1f288-191">NOTES</span></span>

## <span data-ttu-id="1f288-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f288-192">RELATED LINKS</span></span>

