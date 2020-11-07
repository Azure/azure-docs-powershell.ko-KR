---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 696db55822242e124f006be233a9c8a8605a360d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697946"
---
# <span data-ttu-id="1a687-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1a687-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1a687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a687-102">SYNOPSIS</span></span>
<span data-ttu-id="1a687-103">권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="1a687-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a687-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a687-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a687-105">DESCRIPTION</span></span>
<span data-ttu-id="1a687-106">**AzApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="1a687-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a687-107">EXAMPLES</span></span>

### <span data-ttu-id="1a687-108">예제 1: 권한 부여 서버 수정</span><span class="sxs-lookup"><span data-stu-id="1a687-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="1a687-109">이 명령은 지정 된 API 관리 권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="1a687-110">변수</span><span class="sxs-lookup"><span data-stu-id="1a687-110">PARAMETERS</span></span>

### <span data-ttu-id="1a687-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="1a687-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="1a687-112">액세스 토큰을 보낼 메서드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="1a687-113">psdx_paramvalues AuthorizationHeader 및 Query.</span><span class="sxs-lookup"><span data-stu-id="1a687-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="1a687-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1a687-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="1a687-115">리소스 소유자를 인증 하 고 권한 부여 권한을 얻을 수 있는 권한 부여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="1a687-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="1a687-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="1a687-117">인증 요청 메서드 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="1a687-118">psdx_paramvalues 가져오고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="1a687-119">기본 값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-119">The default value is GET.</span></span>

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

### <span data-ttu-id="1a687-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="1a687-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="1a687-121">클라이언트 인증 방법의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="1a687-122">기본 및 본문을 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="1a687-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1a687-123">-ClientId</span></span>
<span data-ttu-id="1a687-124">클라이언트 응용 프로그램에 해당 하는 개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="1a687-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="1a687-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="1a687-126">인증 서버에 클라이언트를 등록 하 고 클라이언트 자격 증명을 가져오는 클라이언트 등록 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="1a687-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1a687-127">-ClientSecret</span></span>
<span data-ttu-id="1a687-128">클라이언트 응용 프로그램 개발자 콘솔의 클라이언트 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="1a687-129">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1a687-129">-Context</span></span>
<span data-ttu-id="1a687-130">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1a687-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a687-131">-DefaultProfile</span></span>
<span data-ttu-id="1a687-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a687-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="1a687-133">-DefaultScope</span></span>
<span data-ttu-id="1a687-134">권한 부여 서버의 기본 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="1a687-135">-설명</span><span class="sxs-lookup"><span data-stu-id="1a687-135">-Description</span></span>
<span data-ttu-id="1a687-136">권한 부여 서버에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="1a687-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="1a687-137">-GrantTypes</span></span>
<span data-ttu-id="1a687-138">허용 형식 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="1a687-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1a687-139">psdx_paramvalues</span></span>
- <span data-ttu-id="1a687-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="1a687-140">AuthorizationCode</span></span>
- <span data-ttu-id="1a687-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="1a687-141">ClientCredentials</span></span> 
- <span data-ttu-id="1a687-142">명시적</span><span class="sxs-lookup"><span data-stu-id="1a687-142">Implicit</span></span> 
- <span data-ttu-id="1a687-143">Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="1a687-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="1a687-144">-이름</span><span class="sxs-lookup"><span data-stu-id="1a687-144">-Name</span></span>
<span data-ttu-id="1a687-145">수정할 인증 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="1a687-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a687-146">-PassThru</span></span>
<span data-ttu-id="1a687-147">passthru</span><span class="sxs-lookup"><span data-stu-id="1a687-147">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a687-148">-Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="1a687-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="1a687-149">리소스 소유자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="1a687-150">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1a687-151">-Resource소유자 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="1a687-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="1a687-152">리소스 소유자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="1a687-153">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1a687-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1a687-154">-ServerId</span></span>
<span data-ttu-id="1a687-155">수정할 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="1a687-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="1a687-156">-SupportState</span></span>
<span data-ttu-id="1a687-157">*State* 매개 변수를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="1a687-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="1a687-158">-TokenBodyParameters</span></span>
<span data-ttu-id="1a687-159">Application/x-www-urlencoded 형식을 사용 하 여 추가 본문 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="1a687-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1a687-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="1a687-161">권한 부여를 제공 하거나 새로 고침 토큰을 제공 하기 위해 exchange에서 액세스 토큰을 가져오는 클라이언트의 토큰 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="1a687-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a687-162">CommonParameters</span></span>
<span data-ttu-id="1a687-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a687-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a687-164">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a687-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a687-165">입력</span><span class="sxs-lookup"><span data-stu-id="1a687-165">INPUTS</span></span>

### <span data-ttu-id="1a687-166">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a687-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1a687-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a687-167">System.String</span></span>

### <span data-ttu-id="1a687-168">ApiManagement [] ServiceManagement. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="1a687-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="1a687-169">ApiManagement [] ServiceManagement. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="1a687-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="1a687-170">ApiManagement [] ServiceManagement. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="1a687-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="1a687-171">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1a687-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1a687-172">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1a687-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1a687-173">ApiManagement [] ServiceManagement. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="1a687-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="1a687-174">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a687-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a687-175">출력</span><span class="sxs-lookup"><span data-stu-id="1a687-175">OUTPUTS</span></span>

### <span data-ttu-id="1a687-176">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1a687-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="1a687-177">상속자</span><span class="sxs-lookup"><span data-stu-id="1a687-177">NOTES</span></span>

## <span data-ttu-id="1a687-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a687-178">RELATED LINKS</span></span>

[<span data-ttu-id="1a687-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1a687-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1a687-180">새로운 AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1a687-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1a687-181">제거-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1a687-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


