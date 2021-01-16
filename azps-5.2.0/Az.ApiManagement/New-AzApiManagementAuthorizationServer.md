---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: bfb074fe53afe2c3eb9d8a69580c817116cb9cd1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364589"
---
# <span data-ttu-id="94fae-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="94fae-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="94fae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94fae-102">SYNOPSIS</span></span>
<span data-ttu-id="94fae-103">권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-103">Creates an authorization server.</span></span>

## <span data-ttu-id="94fae-104">구문</span><span class="sxs-lookup"><span data-stu-id="94fae-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94fae-105">설명</span><span class="sxs-lookup"><span data-stu-id="94fae-105">DESCRIPTION</span></span>
<span data-ttu-id="94fae-106">**New-AzApiManagementAuthorizationServer** cmdlet은 Azure API Management 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="94fae-107">예제</span><span class="sxs-lookup"><span data-stu-id="94fae-107">EXAMPLES</span></span>

### <span data-ttu-id="94fae-108">예제 1: 권한 부여 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="94fae-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="94fae-109">이 명령은 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-109">This command creates an authorization server.</span></span>

### <span data-ttu-id="94fae-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="94fae-110">Example 2</span></span>

<span data-ttu-id="94fae-111">권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-111">Creates an authorization server.</span></span> <span data-ttu-id="94fae-112">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="94fae-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementAuthorizationServer -AccessTokenSendingMethods AuthorizationHeader -AuthorizationEndpointUrl 'https://contoso/auth' -AuthorizationRequestMethods Get -ClientAuthenticationMethods Basic -ClientId 'clientid' -ClientRegistrationPageUrl 'https://contoso/signup' -ClientSecret '0000000000000000000000000000000000000' -Context <PsApiManagementContext> -GrantTypes AuthorizationCode -Name 'Contoso OAuth2 server' -ServerId '0123456789' -TokenBodyParameters @{'par1'='val1'} -TokenEndpointUrl 'https://contoso/token'
```

## <span data-ttu-id="94fae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94fae-113">PARAMETERS</span></span>

### <span data-ttu-id="94fae-114">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="94fae-114">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="94fae-115">액세스 토큰을 보낼 메서드 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-115">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="94fae-116">psdx_paramvalues AuthorizationHeader 및 쿼리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-116">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-117">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="94fae-117">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="94fae-118">리소스 소유자를 인증하고 권한 부여를 얻기 위한 권한 부여 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-118">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="94fae-119">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="94fae-119">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="94fae-120">권한 부여 요청 메서드의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-120">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="94fae-121">유효한 값은 GET, POST입니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-121">Valid values are: GET, POST.</span></span>
<span data-ttu-id="94fae-122">기본값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-122">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-123">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="94fae-123">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="94fae-124">클라이언트 인증 방법의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-124">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="94fae-125">psdx_paramvalues 기본 및 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-125">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-126">-ClientId</span><span class="sxs-lookup"><span data-stu-id="94fae-126">-ClientId</span></span>
<span data-ttu-id="94fae-127">클라이언트 애플리케이션인 개발자 콘솔의 클라이언트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-127">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="94fae-128">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="94fae-128">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="94fae-129">인증 서버에 클라이언트를 등록하고 클라이언트 자격 증명을 얻기 위한 클라이언트 등록 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-129">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="94fae-130">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="94fae-130">-ClientSecret</span></span>
<span data-ttu-id="94fae-131">클라이언트 애플리케이션인 개발자 콘솔의 클라이언트 비밀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-131">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="94fae-132">-Context</span><span class="sxs-lookup"><span data-stu-id="94fae-132">-Context</span></span>
<span data-ttu-id="94fae-133">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="94fae-133">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="94fae-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fae-134">-DefaultProfile</span></span>
<span data-ttu-id="94fae-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94fae-136">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="94fae-136">-DefaultScope</span></span>
<span data-ttu-id="94fae-137">권한 부여 서버에 대한 기본 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-137">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="94fae-138">-Description</span><span class="sxs-lookup"><span data-stu-id="94fae-138">-Description</span></span>
<span data-ttu-id="94fae-139">권한 부여 서버에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-139">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="94fae-140">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="94fae-140">-GrantTypes</span></span>
<span data-ttu-id="94fae-141">권한 부여 유형의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-141">Specifies an array of grant types.</span></span>
<span data-ttu-id="94fae-142">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="94fae-142">psdx_paramvalues</span></span>
- <span data-ttu-id="94fae-143">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="94fae-143">AuthorizationCode</span></span>
- <span data-ttu-id="94fae-144">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="94fae-144">ClientCredentials</span></span> 
- <span data-ttu-id="94fae-145">암시적</span><span class="sxs-lookup"><span data-stu-id="94fae-145">Implicit</span></span> 
- <span data-ttu-id="94fae-146">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="94fae-146">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-147">-Name</span><span class="sxs-lookup"><span data-stu-id="94fae-147">-Name</span></span>
<span data-ttu-id="94fae-148">만들 권한 부여 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-148">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="94fae-149">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="94fae-149">-ResourceOwnerPassword</span></span>
<span data-ttu-id="94fae-150">리소스 소유자 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-150">Specifies the resource owner password.</span></span>
<span data-ttu-id="94fae-151">*GrantTypes* 매개 변수에서 ResourceOwnerPassword를 지정하는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-151">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="94fae-152">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="94fae-152">-ResourceOwnerUsername</span></span>
<span data-ttu-id="94fae-153">리소스 소유자 사용자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-153">Specifies the resource owner user name.</span></span>
<span data-ttu-id="94fae-154">*GrantTypes* 매개 변수로 ResourceOwnerPassword를 지정하는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-154">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="94fae-155">-ServerId</span><span class="sxs-lookup"><span data-stu-id="94fae-155">-ServerId</span></span>
<span data-ttu-id="94fae-156">만들 권한 부여 서버의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-156">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="94fae-157">-SupportState</span><span class="sxs-lookup"><span data-stu-id="94fae-157">-SupportState</span></span>
<span data-ttu-id="94fae-158">State 매개 변수를 *지원할지 여부를* 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-158">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-159">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="94fae-159">-TokenBodyParameters</span></span>
<span data-ttu-id="94fae-160">**application/x-www-form-urlencoded** 형식을 사용하여 추가 본문 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-160">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fae-161">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="94fae-161">-TokenEndpointUrl</span></span>
<span data-ttu-id="94fae-162">권한 부여 또는 새로 고침 토큰을 제시하는 대신 액세스 토큰을 얻기 위해 클라이언트에서 사용하는 토큰 엔드포인트 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-162">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="94fae-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fae-163">CommonParameters</span></span>
<span data-ttu-id="94fae-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94fae-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fae-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94fae-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fae-166">입력</span><span class="sxs-lookup"><span data-stu-id="94fae-166">INPUTS</span></span>

### <span data-ttu-id="94fae-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="94fae-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="94fae-168">System.String</span><span class="sxs-lookup"><span data-stu-id="94fae-168">System.String</span></span>

### <span data-ttu-id="94fae-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span><span class="sxs-lookup"><span data-stu-id="94fae-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="94fae-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span><span class="sxs-lookup"><span data-stu-id="94fae-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="94fae-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span><span class="sxs-lookup"><span data-stu-id="94fae-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="94fae-172">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="94fae-172">System.Collections.Hashtable</span></span>

### <span data-ttu-id="94fae-173">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94fae-173">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="94fae-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span><span class="sxs-lookup"><span data-stu-id="94fae-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="94fae-175">출력</span><span class="sxs-lookup"><span data-stu-id="94fae-175">OUTPUTS</span></span>

### <span data-ttu-id="94fae-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="94fae-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="94fae-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94fae-177">NOTES</span></span>

## <span data-ttu-id="94fae-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94fae-178">RELATED LINKS</span></span>