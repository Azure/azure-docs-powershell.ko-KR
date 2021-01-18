---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492722"
---
# <span data-ttu-id="ceed4-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ceed4-101">Connect-AzAccount</span></span>

## <span data-ttu-id="ceed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceed4-102">SYNOPSIS</span></span>
<span data-ttu-id="ceed4-103">Az PowerShell 모듈의 cmdlet과 함께 사용하기 위해 인증된 계정으로 Azure에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="ceed4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ceed4-104">SYNTAX</span></span>

### <span data-ttu-id="ceed4-105">UserWithSubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="ceed4-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceed4-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ceed4-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceed4-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="ceed4-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceed4-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ceed4-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceed4-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ceed4-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceed4-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="ceed4-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ceed4-111">설명</span><span class="sxs-lookup"><span data-stu-id="ceed4-111">DESCRIPTION</span></span>

<span data-ttu-id="ceed4-112">이 cmdlet은 Az PowerShell 모듈의 cmdlet과 함께 사용하기 위해 인증된 계정으로 `Connect-AzAccount` Azure에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="ceed4-113">이 인증된 계정은 Azure Resource Manager 요청에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="ceed4-114">서비스 관리에 사용할 인증된 계정을 추가하려면 Azure PowerShell 모듈의 `Add-AzureAccount` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="ceed4-115">현재 사용자에 대한 컨텍스트가 없는 경우 사용자의 컨텍스트 목록은 처음 25개 구독 각각에 대한 컨텍스트로 채워진 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="ceed4-116">사용자에 대해 만든 컨텍스트 목록은 다음을 실행하여 찾을 수 `Get-AzContext -ListAvailable` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="ceed4-117">이 컨텍스트 인구를 건너뛰기 위해 **SkipContextPopulation** 스위치 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="ceed4-118">이 cmdlet을 실행한 후 다음을 사용하여 Azure 계정에서 연결을 끊을 수 `Disconnect-AzAccount` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="ceed4-119">예제</span><span class="sxs-lookup"><span data-stu-id="ceed4-119">EXAMPLES</span></span>

### <span data-ttu-id="ceed4-120">예제 1: Azure 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="ceed4-121">이 예제는 Azure 계정에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-121">This example connects to an Azure account.</span></span> <span data-ttu-id="ceed4-122">Microsoft 계정 또는 조직 ID 자격 증명을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="ceed4-123">자격 증명에 다단계 인증을 사용하도록 설정한 경우 대화형 옵션을 사용하여 로그인하거나 서비스 주체 인증을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ceed4-124">예제 2: (Windows PowerShell 5.1만 해당) 조직 ID 자격 증명을 사용하여 Azure에 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="ceed4-125">이 시나리오는 Windows PowerShell 5.1에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="ceed4-126">첫 번째 명령은 사용자 자격 증명을 묻는 메시지를 표시하고 변수에 `$Credential` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="ceed4-127">두 번째 명령은 에 저장된 자격 증명을 사용하여 Azure 계정에 `$Credential` 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="ceed4-128">이 계정은 조직 ID 자격 증명을 사용하여 Azure에서 인증합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ceed4-129">예제 3: 서비스 주체 계정을 사용하여 Azure에 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="ceed4-130">첫 번째 명령은 서비스 주체 자격 증명을 묻는 메시지를 표시하고 변수에 `$Credential` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="ceed4-131">메시지가 표시될 때 사용자 이름 및 서비스 주체 암호에 대한 애플리케이션 ID를 암호로 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="ceed4-132">두 번째 명령은 변수에 저장된 서비스 주체 자격 증명을 사용하여 지정된 Azure 테넌트에 `$Credential` 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="ceed4-133">**ServicePrincipal** 스위치 매개 변수는 계정이 서비스 주체로 인증하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ceed4-134">예제 4: 대화형 로그인을 사용하여 특정 테넌트 및 구독에 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="ceed4-135">이 예제에서는 지정된 테넌트 및 구독을 사용하여 Azure 계정에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ceed4-136">예제 5: 관리 서비스 ID를 사용하여 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="ceed4-137">이 예제에서는 호스트 환경의 MSI(관리 서비스 ID)를 사용하여 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="ceed4-138">예를 들어 MSI가 할당된 가상 머신에서 Azure에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ceed4-139">예제 6: 관리 서비스 ID 로그인 및 ClientId를 사용하여 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="ceed4-140">이 예제에서는 **myUserAssignedIdentity의** 관리 서비스 ID를 사용하여 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="ceed4-141">가상 머신에 사용자 할당 ID를 추가한 다음 사용자 할당 ID의 ClientId를 사용하여 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="ceed4-142">자세한 내용은 Azure VM에서 Azure 리소스에 대한 관리 ID [구성을 참조하세요.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="ceed4-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="ceed4-143">예제 7: 인증서를 사용하여 연결</span><span class="sxs-lookup"><span data-stu-id="ceed4-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="ceed4-144">이 예제에서는 인증서 기반 서비스 주체 인증을 사용하여 Azure 계정에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="ceed4-145">인증에 사용되는 서비스 주체는 지정된 인증서로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="ceed4-146">자체 서명된 인증서를 만들고 권한을 할당하는 자세한 내용은 Azure PowerShell을 사용하여 인증서로 서비스 주체 [만들기를 참조하세요.](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="ceed4-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="ceed4-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceed4-147">PARAMETERS</span></span>

### <span data-ttu-id="ceed4-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="ceed4-148">-AccessToken</span></span>

<span data-ttu-id="ceed4-149">액세스 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="ceed4-150">액세스 토큰은 자격 증명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="ceed4-151">기밀을 유지하기 위해 적절한 보안 예방 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="ceed4-152">또한 액세스 토큰은 시간 제한이 있으며 장기 실행 작업이 완료되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="ceed4-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ceed4-153">-AccountId</span></span>

<span data-ttu-id="ceed4-154">**AccessToken** 매개 변수 집합의 액세스 토큰에 대한 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="ceed4-155">**ManagedService** 매개 변수 집합의 관리되는 서비스에 대한 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="ceed4-156">관리되는 서비스 리소스 ID 또는 연결된 클라이언트 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="ceed4-157">시스템 할당 ID를 사용 중이면 이 필드를 비워 두십시오.</span><span class="sxs-lookup"><span data-stu-id="ceed4-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="ceed4-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ceed4-158">-ApplicationId</span></span>

<span data-ttu-id="ceed4-159">서비스 주체의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="ceed4-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ceed4-160">-CertificateThumbprint</span></span>

<span data-ttu-id="ceed4-161">인증서 해시 또는 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="ceed4-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="ceed4-162">-ContextName</span></span>

<span data-ttu-id="ceed4-163">이 로그인에 대한 기본 Azure 컨텍스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="ceed4-164">Azure 컨텍스트에 대한 자세한 내용은 [Azure PowerShell 컨텍스트 개체를 참조하세요.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="ceed4-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="ceed4-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="ceed4-165">-Credential</span></span>

<span data-ttu-id="ceed4-166">**PSCredential** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="ceed4-167">**PSCredential** 개체에 대한 자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="ceed4-168">**PSCredential** 개체는 조직 ID 자격 증명에 대한 사용자 ID 및 암호 또는 서비스 주체 자격 증명에 대한 애플리케이션 ID 및 비밀을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="ceed4-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceed4-169">-DefaultProfile</span></span>

<span data-ttu-id="ceed4-170">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceed4-171">-Environment</span><span class="sxs-lookup"><span data-stu-id="ceed4-171">-Environment</span></span>

<span data-ttu-id="ceed4-172">Azure 계정을 포함하는 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="ceed4-173">-Force</span><span class="sxs-lookup"><span data-stu-id="ceed4-173">-Force</span></span>

<span data-ttu-id="ceed4-174">메시지를 표시하지 않고 동일한 이름으로 기존 컨텍스트를 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="ceed4-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ceed4-175">-GraphAccessToken</span></span>

<span data-ttu-id="ceed4-176">Graph Service용 AccessToken입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="ceed4-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="ceed4-177">-Identity</span></span>

<span data-ttu-id="ceed4-178">관리 서비스 ID를 사용하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="ceed4-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="ceed4-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="ceed4-180">KeyVault Service에 대한 AccessToken입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="ceed4-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="ceed4-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="ceed4-182">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-182">Obsolete.</span></span> <span data-ttu-id="ceed4-183">사용자 지정된 MSI 엔드포인트를 사용 설정하기 위해 환경 변수를 MSI_ENDPOINT"를 http://localhost:50342/oauth2/token 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="ceed4-184">관리되는 서비스의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="ceed4-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="ceed4-185">-ManagedServicePort</span></span>

<span data-ttu-id="ceed4-186">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-186">Obsolete.</span></span> <span data-ttu-id="ceed4-187">사용자 지정된 MSI 엔드포인트를 사용 설정하기 위해 환경 변수를 MSI_ENDPOINT"를 http://localhost:50342/oauth2/token 지정합니다. 관리되는 서비스의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="ceed4-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="ceed4-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="ceed4-189">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-189">Obsolete.</span></span> <span data-ttu-id="ceed4-190">사용자 지정된 MSI 비밀을 사용 설정하기 위해 환경 변수를 MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="ceed4-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="ceed4-191">관리되는 서비스 로그인에 대한 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="ceed4-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="ceed4-192">-MaxContextPopulation</span></span>

<span data-ttu-id="ceed4-193">로그인 후 컨텍스트를 채우는 최대 구독 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="ceed4-194">기본값은 25입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-194">Default is 25.</span></span> <span data-ttu-id="ceed4-195">컨텍스트에 대한 모든 구독을 채우기 위해 -1로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="ceed4-195">To populate all subscriptions to contexts, set to -1.</span></span>

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

### <span data-ttu-id="ceed4-196">-Scope</span><span class="sxs-lookup"><span data-stu-id="ceed4-196">-Scope</span></span>

<span data-ttu-id="ceed4-197">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ceed4-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ceed4-198">-ServicePrincipal</span></span>

<span data-ttu-id="ceed4-199">서비스 주체 자격 증명을 제공하여 이 계정이 인증을 하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="ceed4-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="ceed4-200">-SkipContextPopulation</span></span>

<span data-ttu-id="ceed4-201">컨텍스트가 없는 경우 컨텍스트 인구를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="ceed4-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="ceed4-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="ceed4-202">-SkipValidation</span></span>

<span data-ttu-id="ceed4-203">액세스 토큰에 대한 유효성 검사 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="ceed4-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="ceed4-204">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ceed4-204">-Subscription</span></span>

<span data-ttu-id="ceed4-205">구독 이름 또는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="ceed4-206">-Tenant</span><span class="sxs-lookup"><span data-stu-id="ceed4-206">-Tenant</span></span>

<span data-ttu-id="ceed4-207">선택적 테넌트 이름 또는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="ceed4-208">현재 API의 제한 사항으로 인해 B2B(기업간) 계정으로 연결할 때 테넌트 이름 대신 테넌트 ID를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="ceed4-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ceed4-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="ceed4-210">브라우저 컨트롤 대신 디바이스 코드 인증을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="ceed4-211">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceed4-211">-Confirm</span></span>

<span data-ttu-id="ceed4-212">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceed4-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceed4-213">-WhatIf</span></span>

<span data-ttu-id="ceed4-214">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ceed4-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceed4-215">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceed4-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceed4-216">CommonParameters</span></span>
<span data-ttu-id="ceed4-217">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceed4-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceed4-218">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ceed4-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceed4-219">입력</span><span class="sxs-lookup"><span data-stu-id="ceed4-219">INPUTS</span></span>

### <span data-ttu-id="ceed4-220">System.String</span><span class="sxs-lookup"><span data-stu-id="ceed4-220">System.String</span></span>

## <span data-ttu-id="ceed4-221">출력</span><span class="sxs-lookup"><span data-stu-id="ceed4-221">OUTPUTS</span></span>

### <span data-ttu-id="ceed4-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ceed4-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ceed4-223">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceed4-223">NOTES</span></span>

## <span data-ttu-id="ceed4-224">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceed4-224">RELATED LINKS</span></span>
