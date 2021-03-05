---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 31a635c5965d40cf12e77d556e987c08dfb7175a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993085"
---
# <span data-ttu-id="41199-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="41199-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="41199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41199-102">SYNOPSIS</span></span>
<span data-ttu-id="41199-103">새 ID 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41199-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="41199-104">구문</span><span class="sxs-lookup"><span data-stu-id="41199-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41199-105">설명</span><span class="sxs-lookup"><span data-stu-id="41199-105">DESCRIPTION</span></span>
<span data-ttu-id="41199-106">새 ID 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41199-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="41199-107">예제</span><span class="sxs-lookup"><span data-stu-id="41199-107">EXAMPLES</span></span>

### <span data-ttu-id="41199-108">예제 1: 개발자 포털 로그인에 대한 ID 공급자로 Facebook 구성</span><span class="sxs-lookup"><span data-stu-id="41199-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="41199-109">이 명령은 ApiManagement 서비스의 개발자 포털에서 허용되는 ID 공급자로 Facebook ID를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="41199-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="41199-110">이는 Facebook 앱의 ClientId 및 ClientSecret을 입력하는 것으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="41199-111">예제 2: 개발자 포털 로그인을 위한 ID 공급자로 adB2C 구성</span><span class="sxs-lookup"><span data-stu-id="41199-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="41199-112">이 명령은 ApiManagement 서비스의 개발자 포털에서 허용되는 ID 공급자로 Facebook ID를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="41199-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="41199-113">이는 Facebook 앱의 ClientId 및 ClientSecret을 입력하는 것으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="41199-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="41199-114">PARAMETERS</span></span>

### <span data-ttu-id="41199-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="41199-115">-AllowedTenants</span></span>
<span data-ttu-id="41199-116">허용된 Azure Active Directory 테넌트 목록</span><span class="sxs-lookup"><span data-stu-id="41199-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="41199-117">-Authority</span></span>
<span data-ttu-id="41199-118">AAD 또는 AAD B2C에 대한 OpenID Connect 검색 엔드포인트 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="41199-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="41199-120">-ClientId</span></span>
<span data-ttu-id="41199-121">외부 ID 공급자의 애플리케이션의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="41199-122">Facebook 로그인용 앱 ID, Google 로그인용 클라이언트 ID, Microsoft용 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="41199-123">-ClientSecret</span></span>
<span data-ttu-id="41199-124">로그인 요청을 인증하는 데 사용되는 외부 ID 공급자의 애플리케이션의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="41199-125">예를 들어 Facebook 로그인용 App Secret, Google 로그인용 API 키, Microsoft용 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-126">-Context</span><span class="sxs-lookup"><span data-stu-id="41199-126">-Context</span></span>
<span data-ttu-id="41199-127">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="41199-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41199-129">-DefaultProfile</span></span>
<span data-ttu-id="41199-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41199-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="41199-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="41199-132">암호 재설정 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-132">Password Reset Policy Name.</span></span> <span data-ttu-id="41199-133">AAD B2C ID 공급자에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="41199-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="41199-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="41199-136">프로필 편집 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="41199-137">AAD B2C ID 공급자에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="41199-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="41199-139">-SigninPolicyName</span></span>
<span data-ttu-id="41199-140">로그인 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-140">Signin Policy Name.</span></span> <span data-ttu-id="41199-141">AAD B2C ID 공급자에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="41199-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="41199-143">-SigninTenant</span></span>
<span data-ttu-id="41199-144">테넌트 대신 AAD B2C에서 오버라이드하는 Signin `common` 테넌트</span><span class="sxs-lookup"><span data-stu-id="41199-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="41199-145">-SignupPolicyName</span></span>
<span data-ttu-id="41199-146">등록 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-146">Signup Policy Name.</span></span> <span data-ttu-id="41199-147">AAD B2C ID 공급자에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="41199-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-149">-Type</span><span class="sxs-lookup"><span data-stu-id="41199-149">-Type</span></span>
<span data-ttu-id="41199-150">ID 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="41199-151">지정한 경우 식별자에 의해 ID 공급자 구성을 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="41199-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="41199-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41199-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41199-153">-확인</span><span class="sxs-lookup"><span data-stu-id="41199-153">-Confirm</span></span>
<span data-ttu-id="41199-154">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="41199-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41199-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41199-155">-WhatIf</span></span>
<span data-ttu-id="41199-156">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="41199-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41199-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41199-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41199-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41199-158">CommonParameters</span></span>
<span data-ttu-id="41199-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41199-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41199-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41199-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41199-161">입력</span><span class="sxs-lookup"><span data-stu-id="41199-161">INPUTS</span></span>

### <span data-ttu-id="41199-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41199-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41199-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="41199-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="41199-164">System.String</span><span class="sxs-lookup"><span data-stu-id="41199-164">System.String</span></span>

### <span data-ttu-id="41199-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="41199-165">System.String[]</span></span>

## <span data-ttu-id="41199-166">출력</span><span class="sxs-lookup"><span data-stu-id="41199-166">OUTPUTS</span></span>

### <span data-ttu-id="41199-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="41199-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="41199-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41199-168">NOTES</span></span>

## <span data-ttu-id="41199-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41199-169">RELATED LINKS</span></span>

[<span data-ttu-id="41199-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="41199-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="41199-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="41199-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="41199-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="41199-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
