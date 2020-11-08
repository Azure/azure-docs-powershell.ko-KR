---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 46530ce5fd72ea01abdd258feb9f7049bf9670a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042260"
---
# <span data-ttu-id="78a33-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="78a33-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="78a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a33-102">SYNOPSIS</span></span>
<span data-ttu-id="78a33-103">권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-103">Creates an authorization server.</span></span>

## <span data-ttu-id="78a33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78a33-104">SYNTAX</span></span>

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

## <span data-ttu-id="78a33-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78a33-105">DESCRIPTION</span></span>
<span data-ttu-id="78a33-106">**AzApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="78a33-107">예제의</span><span class="sxs-lookup"><span data-stu-id="78a33-107">EXAMPLES</span></span>

### <span data-ttu-id="78a33-108">예제 1: 권한 부여 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="78a33-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="78a33-109">이 명령은 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="78a33-110">변수</span><span class="sxs-lookup"><span data-stu-id="78a33-110">PARAMETERS</span></span>

### <span data-ttu-id="78a33-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="78a33-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="78a33-112">액세스 토큰을 보낼 메서드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="78a33-113">psdx_paramvalues AuthorizationHeader 및 Query.</span><span class="sxs-lookup"><span data-stu-id="78a33-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="78a33-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="78a33-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="78a33-115">리소스 소유자를 인증 하 고 권한 부여 권한을 얻을 수 있는 권한 부여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="78a33-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="78a33-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="78a33-117">인증 요청 메서드 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="78a33-118">유효한 값은 GET, POST입니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="78a33-119">기본 값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-119">The default value is GET.</span></span>

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

### <span data-ttu-id="78a33-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="78a33-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="78a33-121">클라이언트 인증 방법의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="78a33-122">기본 및 본문을 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="78a33-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="78a33-123">-ClientId</span></span>
<span data-ttu-id="78a33-124">클라이언트 응용 프로그램에 해당 하는 개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="78a33-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="78a33-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="78a33-126">인증 서버에 클라이언트를 등록 하 고 클라이언트 자격 증명을 가져오는 클라이언트 등록 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="78a33-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="78a33-127">-ClientSecret</span></span>
<span data-ttu-id="78a33-128">클라이언트 응용 프로그램 개발자 콘솔의 클라이언트 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="78a33-129">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="78a33-129">-Context</span></span>
<span data-ttu-id="78a33-130">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="78a33-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a33-131">-DefaultProfile</span></span>
<span data-ttu-id="78a33-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a33-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="78a33-133">-DefaultScope</span></span>
<span data-ttu-id="78a33-134">권한 부여 서버의 기본 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="78a33-135">-설명</span><span class="sxs-lookup"><span data-stu-id="78a33-135">-Description</span></span>
<span data-ttu-id="78a33-136">권한 부여 서버에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="78a33-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="78a33-137">-GrantTypes</span></span>
<span data-ttu-id="78a33-138">허용 형식 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="78a33-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="78a33-139">psdx_paramvalues</span></span>
- <span data-ttu-id="78a33-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="78a33-140">AuthorizationCode</span></span>
- <span data-ttu-id="78a33-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="78a33-141">ClientCredentials</span></span> 
- <span data-ttu-id="78a33-142">명시적</span><span class="sxs-lookup"><span data-stu-id="78a33-142">Implicit</span></span> 
- <span data-ttu-id="78a33-143">Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="78a33-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="78a33-144">-이름</span><span class="sxs-lookup"><span data-stu-id="78a33-144">-Name</span></span>
<span data-ttu-id="78a33-145">만들 인증 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="78a33-146">-Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="78a33-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="78a33-147">리소스 소유자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="78a33-148">*GrantTypes* 매개 변수로 Resource소유 암호를 지정한 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="78a33-149">-Resource소유자 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="78a33-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="78a33-150">리소스 소유자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="78a33-151">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="78a33-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="78a33-152">-ServerId</span></span>
<span data-ttu-id="78a33-153">만들 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="78a33-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="78a33-154">-SupportState</span></span>
<span data-ttu-id="78a33-155">*State* 매개 변수를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="78a33-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="78a33-156">-TokenBodyParameters</span></span>
<span data-ttu-id="78a33-157">**Application/x-www-urlencoded** 형식을 사용 하 여 추가 본문 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="78a33-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="78a33-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="78a33-159">권한 부여를 제공 하거나 새로 고침 토큰을 제공 하기 위해 exchange에서 액세스 토큰을 가져오기 위해 클라이언트에서 사용 하는 토큰 끝점 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="78a33-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a33-160">CommonParameters</span></span>
<span data-ttu-id="78a33-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78a33-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a33-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78a33-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a33-163">입력</span><span class="sxs-lookup"><span data-stu-id="78a33-163">INPUTS</span></span>

### <span data-ttu-id="78a33-164">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78a33-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78a33-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78a33-165">System.String</span></span>

### <span data-ttu-id="78a33-166">ApiManagement [] ServiceManagement. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="78a33-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="78a33-167">ApiManagement [] ServiceManagement. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="78a33-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="78a33-168">ApiManagement [] ServiceManagement. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="78a33-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="78a33-169">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="78a33-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="78a33-170">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78a33-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78a33-171">ApiManagement [] ServiceManagement. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="78a33-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="78a33-172">출력</span><span class="sxs-lookup"><span data-stu-id="78a33-172">OUTPUTS</span></span>

### <span data-ttu-id="78a33-173">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="78a33-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="78a33-174">상속자</span><span class="sxs-lookup"><span data-stu-id="78a33-174">NOTES</span></span>

## <span data-ttu-id="78a33-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78a33-175">RELATED LINKS</span></span>
