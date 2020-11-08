---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047996"
---
# <span data-ttu-id="737ac-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="737ac-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="737ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737ac-102">SYNOPSIS</span></span>
<span data-ttu-id="737ac-103">새 Id 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="737ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="737ac-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="737ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="737ac-105">DESCRIPTION</span></span>
<span data-ttu-id="737ac-106">새 Id 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="737ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="737ac-107">EXAMPLES</span></span>

### <span data-ttu-id="737ac-108">예제 1: Facebook을 개발자 포털 로그인의 id 공급자로 구성</span><span class="sxs-lookup"><span data-stu-id="737ac-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="737ac-109">이 명령은 ApiManagement 서비스의 개발자 포털에서 Facebook Id를 허용 된 Id 공급자로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="737ac-110">이는 Facebook 앱의 ClientId 및 ClientSecret을 입력 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="737ac-111">예제 2: adB2C를 개발자 포털 로그인의 id 공급자로 구성</span><span class="sxs-lookup"><span data-stu-id="737ac-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="737ac-112">이 명령은 ApiManagement 서비스의 개발자 포털에서 Facebook Id를 허용 된 Id 공급자로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="737ac-113">이는 Facebook 앱의 ClientId 및 ClientSecret을 입력 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="737ac-114">변수</span><span class="sxs-lookup"><span data-stu-id="737ac-114">PARAMETERS</span></span>

### <span data-ttu-id="737ac-115">-AllowedTenants 넌 트</span><span class="sxs-lookup"><span data-stu-id="737ac-115">-AllowedTenants</span></span>
<span data-ttu-id="737ac-116">허용 되는 Azure Active Directory 테 넌 트 목록</span><span class="sxs-lookup"><span data-stu-id="737ac-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="737ac-117">-기관</span><span class="sxs-lookup"><span data-stu-id="737ac-117">-Authority</span></span>
<span data-ttu-id="737ac-118">AAD 또는 AAD B2C에 대 한 OpenID Connect 검색 끝점 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="737ac-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="737ac-120">-ClientId</span></span>
<span data-ttu-id="737ac-121">외부 Id 공급자의 응용 프로그램에 대 한 클라이언트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="737ac-122">Facebook 로그인의 앱 ID, Google 로그인의 클라이언트 ID, Microsoft의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="737ac-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="737ac-123">-ClientSecret</span></span>
<span data-ttu-id="737ac-124">로그인 요청을 인증 하는 데 사용 되는 외부 Id 공급자에 해당 하는 응용 프로그램의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="737ac-125">예를 들어 Facebook 로그인에 대 한 앱 비밀, Google 로그인의 API 키, Microsoft의 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="737ac-126">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="737ac-126">-Context</span></span>
<span data-ttu-id="737ac-127">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="737ac-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-128">This parameter is required.</span></span>

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

### <span data-ttu-id="737ac-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737ac-129">-DefaultProfile</span></span>
<span data-ttu-id="737ac-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="737ac-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="737ac-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="737ac-132">암호 재설정 정책 이름.</span><span class="sxs-lookup"><span data-stu-id="737ac-132">Password Reset Policy Name.</span></span> <span data-ttu-id="737ac-133">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="737ac-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="737ac-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="737ac-136">프로필 편집 정책 이름</span><span class="sxs-lookup"><span data-stu-id="737ac-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="737ac-137">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="737ac-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="737ac-139">-SigninPolicyName</span></span>
<span data-ttu-id="737ac-140">로그인 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-140">Signin Policy Name.</span></span> <span data-ttu-id="737ac-141">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="737ac-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="737ac-143">-SigninTenant</span></span>
<span data-ttu-id="737ac-144">테 넌 트가 아닌 AAD B2C에서 재정의 하도록 로그인 테 넌 트 `common`</span><span class="sxs-lookup"><span data-stu-id="737ac-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="737ac-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="737ac-145">-SignupPolicyName</span></span>
<span data-ttu-id="737ac-146">등록 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-146">Signup Policy Name.</span></span> <span data-ttu-id="737ac-147">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="737ac-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-149">-Type</span><span class="sxs-lookup"><span data-stu-id="737ac-149">-Type</span></span>
<span data-ttu-id="737ac-150">Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="737ac-151">지정 된 경우 식별자를 사용 하 여 id 공급자 구성을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="737ac-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="737ac-153">-확인</span><span class="sxs-lookup"><span data-stu-id="737ac-153">-Confirm</span></span>
<span data-ttu-id="737ac-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737ac-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737ac-155">-WhatIf</span></span>
<span data-ttu-id="737ac-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="737ac-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737ac-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737ac-158">CommonParameters</span></span>
<span data-ttu-id="737ac-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="737ac-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737ac-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="737ac-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737ac-161">입력</span><span class="sxs-lookup"><span data-stu-id="737ac-161">INPUTS</span></span>

### <span data-ttu-id="737ac-162">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="737ac-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="737ac-163">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="737ac-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="737ac-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="737ac-164">System.String</span></span>

### <span data-ttu-id="737ac-165">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="737ac-165">System.String[]</span></span>

## <span data-ttu-id="737ac-166">출력</span><span class="sxs-lookup"><span data-stu-id="737ac-166">OUTPUTS</span></span>

### <span data-ttu-id="737ac-167">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="737ac-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="737ac-168">상속자</span><span class="sxs-lookup"><span data-stu-id="737ac-168">NOTES</span></span>

## <span data-ttu-id="737ac-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="737ac-169">RELATED LINKS</span></span>

[<span data-ttu-id="737ac-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="737ac-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="737ac-171">제거-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="737ac-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="737ac-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="737ac-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
