---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536248"
---
# <span data-ttu-id="e3579-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e3579-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="e3579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3579-102">SYNOPSIS</span></span>
<span data-ttu-id="e3579-103">Azure Resource Manager cmdlet 요청에 사용할 인증 된 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3579-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3579-104">SYNTAX</span></span>

### <span data-ttu-id="e3579-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3579-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3579-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3579-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3579-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3579-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3579-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3579-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3579-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e3579-109">DESCRIPTION</span></span>
<span data-ttu-id="e3579-110">Add-AzureRmAcccount cmdlet은 Azure Resource Manager cmdlet 요청에 사용할 인증 된 Azure 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="e3579-111">이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="e3579-112">서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzureAccount 또는 Import-AzurePublishSettingsFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="e3579-113">예제의</span><span class="sxs-lookup"><span data-stu-id="e3579-113">EXAMPLES</span></span>

### <span data-ttu-id="e3579-114">예제 1: 대화형 로그인이 필요한 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e3579-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e3579-115">이 명령은 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="e3579-116">이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="e3579-117">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="e3579-118">예제 2: 조직 ID 자격 증명으로 인증 하는 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e3579-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e3579-119">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e3579-120">두 번째 명령은 $Credential의 자격 증명을 사용 하 여 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="e3579-121">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="e3579-122">이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="e3579-123">예제 3: 서비스 사용자 자격 증명을 사용 하 여 인증 하는 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e3579-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e3579-124">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="e3579-125">두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 되어 있는 자격 증명을 사용 하 여 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="e3579-126">ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="e3579-127">예제 4: 특정 테 넌 트 및 구독에 대 한 계정 추가</span><span class="sxs-lookup"><span data-stu-id="e3579-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e3579-128">이 명령은 기본적으로 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 실행 하는 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="e3579-129">변수</span><span class="sxs-lookup"><span data-stu-id="e3579-129">PARAMETERS</span></span>

### <span data-ttu-id="e3579-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e3579-130">-AccessToken</span></span>
<span data-ttu-id="e3579-131">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="e3579-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e3579-132">-AccountId</span></span>
<span data-ttu-id="e3579-133">액세스 토큰의 계정 Id</span><span class="sxs-lookup"><span data-stu-id="e3579-133">Account Id for access token</span></span>

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

### <span data-ttu-id="e3579-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3579-134">-ApplicationId</span></span>
<span data-ttu-id="e3579-135">수단</span><span class="sxs-lookup"><span data-stu-id="e3579-135">SPN</span></span>

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

### <span data-ttu-id="e3579-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3579-136">-CertificateThumbprint</span></span>
<span data-ttu-id="e3579-137">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="e3579-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="e3579-138">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="e3579-138">-ContextName</span></span>
<span data-ttu-id="e3579-139">이 로그인의 기본 컨텍스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-139">Name of the default context from this login.</span></span>  <span data-ttu-id="e3579-140">로그인 후이 이름을 기준으로이 컨텍스트를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="e3579-141">-Credential</span><span class="sxs-lookup"><span data-stu-id="e3579-141">-Credential</span></span>
<span data-ttu-id="e3579-142">PSCredential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="e3579-143">PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="e3579-144">PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="e3579-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3579-145">-DefaultProfile</span></span>
<span data-ttu-id="e3579-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3579-147">-환경</span><span class="sxs-lookup"><span data-stu-id="e3579-147">-Environment</span></span>
<span data-ttu-id="e3579-148">로그인 하는 계정이 포함 된 환경</span><span class="sxs-lookup"><span data-stu-id="e3579-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="e3579-149">-Force</span><span class="sxs-lookup"><span data-stu-id="e3579-149">-Force</span></span>
<span data-ttu-id="e3579-150">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="e3579-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="e3579-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="e3579-151">-GraphAccessToken</span></span>
<span data-ttu-id="e3579-152">Graph 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="e3579-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="e3579-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="e3579-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="e3579-154">KeyVault 서비스에 대 한 AccessToken</span><span class="sxs-lookup"><span data-stu-id="e3579-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="e3579-155">-범위</span><span class="sxs-lookup"><span data-stu-id="e3579-155">-Scope</span></span>
<span data-ttu-id="e3579-156">Wheher 변경 내용이 cusrrent 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 되는 경우와 같이 컨텍스트 변경의 범위를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e3579-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3579-157">-ServicePrincipal</span></span>
<span data-ttu-id="e3579-158">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3579-159">-구독</span><span class="sxs-lookup"><span data-stu-id="e3579-159">-Subscription</span></span>
<span data-ttu-id="e3579-160">구독 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="e3579-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="e3579-161">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e3579-161">-TenantId</span></span>
<span data-ttu-id="e3579-162">선택적 테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="e3579-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="e3579-163">-확인</span><span class="sxs-lookup"><span data-stu-id="e3579-163">-Confirm</span></span>
<span data-ttu-id="e3579-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3579-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3579-165">-WhatIf</span></span>
<span data-ttu-id="e3579-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3579-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3579-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3579-168">CommonParameters</span></span>
<span data-ttu-id="e3579-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3579-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3579-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3579-171">입력</span><span class="sxs-lookup"><span data-stu-id="e3579-171">INPUTS</span></span>

### <span data-ttu-id="e3579-172">이름</span><span class="sxs-lookup"><span data-stu-id="e3579-172">String</span></span>
<span data-ttu-id="e3579-173">' SubscriptionId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e3579-174">이름</span><span class="sxs-lookup"><span data-stu-id="e3579-174">String</span></span>
<span data-ttu-id="e3579-175">' SubscriptionName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3579-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e3579-176">출력</span><span class="sxs-lookup"><span data-stu-id="e3579-176">OUTPUTS</span></span>

### <span data-ttu-id="e3579-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e3579-177">PSAzureProfile</span></span>
<span data-ttu-id="e3579-178">로그인 한 사용자에 대 한 자격 증명, 구독, 계정 및 테 넌 트 정보</span><span class="sxs-lookup"><span data-stu-id="e3579-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="e3579-179">상속자</span><span class="sxs-lookup"><span data-stu-id="e3579-179">NOTES</span></span>

## <span data-ttu-id="e3579-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3579-180">RELATED LINKS</span></span>

