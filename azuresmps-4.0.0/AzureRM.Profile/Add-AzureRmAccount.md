---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523272"
---
# <span data-ttu-id="90737-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="90737-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="90737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90737-102">SYNOPSIS</span></span>
<span data-ttu-id="90737-103">Azure Resource Manager cmdlet 요청에 사용할 인증 된 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="90737-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90737-104">SYNTAX</span></span>

### <span data-ttu-id="90737-105">UserWithSubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="90737-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="90737-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90737-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="90737-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90737-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="90737-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90737-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90737-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="90737-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90737-113">설명은</span><span class="sxs-lookup"><span data-stu-id="90737-113">DESCRIPTION</span></span>
<span data-ttu-id="90737-114">Add-AzureRmAcccount cmdlet은 Azure Resource Manager cmdlet 요청에 사용할 인증 된 Azure 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="90737-115">이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90737-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="90737-116">서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzureAccount 또는 Import-AzurePublishSettingsFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="90737-117">예제의</span><span class="sxs-lookup"><span data-stu-id="90737-117">EXAMPLES</span></span>

### <span data-ttu-id="90737-118">예제 1: 대화형 로그인이 필요한 계정 추가</span><span class="sxs-lookup"><span data-stu-id="90737-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="90737-119">이 명령은 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="90737-120">이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="90737-121">자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="90737-122">예제 2: 조직 ID 자격 증명으로 인증 하는 계정 추가</span><span class="sxs-lookup"><span data-stu-id="90737-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="90737-123">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="90737-124">두 번째 명령은 $Credential의 자격 증명을 사용 하 여 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="90737-125">이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="90737-126">이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90737-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="90737-127">예제 3: 서비스 사용자 자격 증명을 사용 하 여 인증 하는 계정 추가</span><span class="sxs-lookup"><span data-stu-id="90737-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="90737-128">첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="90737-129">두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 되어 있는 자격 증명을 사용 하 여 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="90737-130">ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90737-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="90737-131">예제 4: 특정 테 넌 트 및 구독에 대 한 계정 추가</span><span class="sxs-lookup"><span data-stu-id="90737-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="90737-132">이 명령은 기본적으로 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 실행 하는 Azure Resource Manager 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="90737-133">변수</span><span class="sxs-lookup"><span data-stu-id="90737-133">PARAMETERS</span></span>

### <span data-ttu-id="90737-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="90737-134">-AccessToken</span></span>
<span data-ttu-id="90737-135">액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="90737-136">-AccountId</span></span>
<span data-ttu-id="90737-137">액세스 토큰의 계정 Id</span><span class="sxs-lookup"><span data-stu-id="90737-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="90737-138">-ApplicationId</span></span>
<span data-ttu-id="90737-139">수단</span><span class="sxs-lookup"><span data-stu-id="90737-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="90737-140">-CertificateThumbprint</span></span>
<span data-ttu-id="90737-141">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="90737-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-142">-Credential</span><span class="sxs-lookup"><span data-stu-id="90737-142">-Credential</span></span>
<span data-ttu-id="90737-143">PSCredential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="90737-144">PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="90737-145">PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-146">-환경</span><span class="sxs-lookup"><span data-stu-id="90737-146">-Environment</span></span>
<span data-ttu-id="90737-147">로그인 하는 계정이 포함 된 환경</span><span class="sxs-lookup"><span data-stu-id="90737-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="90737-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="90737-148">-ServicePrincipal</span></span>
<span data-ttu-id="90737-149">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90737-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90737-150">-SubscriptionId</span></span>
<span data-ttu-id="90737-151">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="90737-152">이 매개 변수를 지정 하지 않으면 구독 목록의 첫 번째 구독이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90737-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90737-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="90737-153">-SubscriptionName</span></span>
<span data-ttu-id="90737-154">구독 이름</span><span class="sxs-lookup"><span data-stu-id="90737-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90737-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="90737-155">-TenantId</span></span>
<span data-ttu-id="90737-156">선택적 테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="90737-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90737-157">-확인</span><span class="sxs-lookup"><span data-stu-id="90737-157">-Confirm</span></span>
<span data-ttu-id="90737-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90737-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90737-159">-WhatIf</span></span>
<span data-ttu-id="90737-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90737-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90737-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90737-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90737-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90737-162">CommonParameters</span></span>
<span data-ttu-id="90737-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90737-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90737-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90737-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90737-165">입력</span><span class="sxs-lookup"><span data-stu-id="90737-165">INPUTS</span></span>

## <span data-ttu-id="90737-166">출력</span><span class="sxs-lookup"><span data-stu-id="90737-166">OUTPUTS</span></span>

### <span data-ttu-id="90737-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="90737-167">PSAzureProfile</span></span>

## <span data-ttu-id="90737-168">상속자</span><span class="sxs-lookup"><span data-stu-id="90737-168">NOTES</span></span>

## <span data-ttu-id="90737-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90737-169">RELATED LINKS</span></span>

