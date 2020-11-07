---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: ed7043746aa5ce59e733737acf8da61bdb44b0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710999"
---
# <span data-ttu-id="99399-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99399-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="99399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99399-102">SYNOPSIS</span></span>
<span data-ttu-id="99399-103">권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99399-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99399-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99399-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99399-105">DESCRIPTION</span></span>
<span data-ttu-id="99399-106">**AzureRmApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="99399-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99399-107">EXAMPLES</span></span>

### <span data-ttu-id="99399-108">예제 1: 권한 부여 서버 수정</span><span class="sxs-lookup"><span data-stu-id="99399-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="99399-109">이 명령은 지정 된 API 관리 권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="99399-110">변수</span><span class="sxs-lookup"><span data-stu-id="99399-110">PARAMETERS</span></span>

### <span data-ttu-id="99399-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="99399-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="99399-112">액세스 토큰을 보낼 메서드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="99399-113">psdx_paramvalues AuthorizationHeader 및 Query.</span><span class="sxs-lookup"><span data-stu-id="99399-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="99399-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="99399-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="99399-115">리소스 소유자를 인증 하 고 권한 부여 권한을 얻을 수 있는 권한 부여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="99399-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="99399-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="99399-117">인증 요청 메서드 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="99399-118">psdx_paramvalues 가져오고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="99399-119">기본 값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="99399-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99399-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="99399-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="99399-121">클라이언트 인증 방법의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="99399-122">기본 및 본문을 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="99399-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="99399-123">-ClientId</span></span>
<span data-ttu-id="99399-124">클라이언트 응용 프로그램에 해당 하는 개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="99399-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="99399-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="99399-126">인증 서버에 클라이언트를 등록 하 고 클라이언트 자격 증명을 가져오는 클라이언트 등록 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="99399-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="99399-127">-ClientSecret</span></span>
<span data-ttu-id="99399-128">클라이언트 응용 프로그램 개발자 콘솔의 클라이언트 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="99399-129">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="99399-129">-Context</span></span>
<span data-ttu-id="99399-130">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99399-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="99399-131">-DefaultScope</span></span>
<span data-ttu-id="99399-132">권한 부여 서버의 기본 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="99399-133">-설명</span><span class="sxs-lookup"><span data-stu-id="99399-133">-Description</span></span>
<span data-ttu-id="99399-134">권한 부여 서버에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="99399-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="99399-135">-GrantTypes</span></span>
<span data-ttu-id="99399-136">허용 형식 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="99399-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="99399-137">psdx_paramvalues</span></span>

- <span data-ttu-id="99399-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="99399-138">AuthorizationCode</span></span>
- <span data-ttu-id="99399-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="99399-139">ClientCredentials</span></span> 
- <span data-ttu-id="99399-140">명시적</span><span class="sxs-lookup"><span data-stu-id="99399-140">Implicit</span></span> 
- <span data-ttu-id="99399-141">Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="99399-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="99399-142">-이름</span><span class="sxs-lookup"><span data-stu-id="99399-142">-Name</span></span>
<span data-ttu-id="99399-143">수정할 인증 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-143">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="99399-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99399-144">-PassThru</span></span>
<span data-ttu-id="99399-145">passthru</span><span class="sxs-lookup"><span data-stu-id="99399-145">passthru</span></span>

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

### <span data-ttu-id="99399-146">-Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="99399-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="99399-147">리소스 소유자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="99399-148">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-148">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="99399-149">-Resource소유자 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="99399-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="99399-150">리소스 소유자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="99399-151">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="99399-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="99399-152">-ServerId</span></span>
<span data-ttu-id="99399-153">수정할 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-153">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="99399-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="99399-154">-SupportState</span></span>
<span data-ttu-id="99399-155">*State* 매개 변수를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99399-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="99399-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="99399-156">-TokenBodyParameters</span></span>
<span data-ttu-id="99399-157">Application/x-www-urlencoded 형식을 사용 하 여 추가 본문 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-157">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="99399-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="99399-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="99399-159">권한 부여를 제공 하거나 새로 고침 토큰을 제공 하기 위해 exchange에서 액세스 토큰을 가져오는 클라이언트의 토큰 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-159">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="99399-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99399-160">-DefaultProfile</span></span>
<span data-ttu-id="99399-161">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99399-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99399-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99399-162">CommonParameters</span></span>
<span data-ttu-id="99399-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99399-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99399-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99399-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99399-165">입력</span><span class="sxs-lookup"><span data-stu-id="99399-165">INPUTS</span></span>

## <span data-ttu-id="99399-166">출력</span><span class="sxs-lookup"><span data-stu-id="99399-166">OUTPUTS</span></span>

### <span data-ttu-id="99399-167">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="99399-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="99399-168">상속자</span><span class="sxs-lookup"><span data-stu-id="99399-168">NOTES</span></span>

## <span data-ttu-id="99399-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99399-169">RELATED LINKS</span></span>

[<span data-ttu-id="99399-170">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99399-170">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="99399-171">새로운 AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99399-171">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="99399-172">제거-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99399-172">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


