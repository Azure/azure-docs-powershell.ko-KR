---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 6424ad453d7e2ee3c4933127cc58e6d3e1193e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535356"
---
# <span data-ttu-id="14d95-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14d95-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="14d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d95-102">SYNOPSIS</span></span>
<span data-ttu-id="14d95-103">권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14d95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14d95-104">SYNTAX</span></span>

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

## <span data-ttu-id="14d95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14d95-105">DESCRIPTION</span></span>
<span data-ttu-id="14d95-106">**AzureRmApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="14d95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14d95-107">EXAMPLES</span></span>

### <span data-ttu-id="14d95-108">예제 1: 권한 부여 서버 수정</span><span class="sxs-lookup"><span data-stu-id="14d95-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="14d95-109">이 명령은 지정 된 API 관리 권한 부여 서버를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="14d95-110">변수</span><span class="sxs-lookup"><span data-stu-id="14d95-110">PARAMETERS</span></span>

### <span data-ttu-id="14d95-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="14d95-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="14d95-112">액세스 토큰을 보낼 메서드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="14d95-113">psdx_paramvalues AuthorizationHeader 및 Query.</span><span class="sxs-lookup"><span data-stu-id="14d95-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="14d95-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="14d95-115">리소스 소유자를 인증 하 고 권한 부여 권한을 얻을 수 있는 권한 부여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="14d95-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="14d95-117">인증 요청 메서드 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="14d95-118">psdx_paramvalues 가져오고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="14d95-119">기본 값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="14d95-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="14d95-121">클라이언트 인증 방법의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="14d95-122">기본 및 본문을 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="14d95-123">-ClientId</span></span>
<span data-ttu-id="14d95-124">클라이언트 응용 프로그램에 해당 하는 개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="14d95-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="14d95-126">인증 서버에 클라이언트를 등록 하 고 클라이언트 자격 증명을 가져오는 클라이언트 등록 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="14d95-127">-ClientSecret</span></span>
<span data-ttu-id="14d95-128">클라이언트 응용 프로그램 개발자 콘솔의 클라이언트 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-128">Specifies the client secret of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-129">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="14d95-129">-Context</span></span>
<span data-ttu-id="14d95-130">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d95-131">-DefaultProfile</span></span>
<span data-ttu-id="14d95-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="14d95-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="14d95-133">-DefaultScope</span></span>
<span data-ttu-id="14d95-134">권한 부여 서버의 기본 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-135">-설명</span><span class="sxs-lookup"><span data-stu-id="14d95-135">-Description</span></span>
<span data-ttu-id="14d95-136">권한 부여 서버에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="14d95-137">-GrantTypes</span></span>
<span data-ttu-id="14d95-138">허용 형식 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="14d95-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="14d95-139">psdx_paramvalues</span></span>

- <span data-ttu-id="14d95-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="14d95-140">AuthorizationCode</span></span>
- <span data-ttu-id="14d95-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="14d95-141">ClientCredentials</span></span> 
- <span data-ttu-id="14d95-142">명시적</span><span class="sxs-lookup"><span data-stu-id="14d95-142">Implicit</span></span> 
- <span data-ttu-id="14d95-143">Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="14d95-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-144">-이름</span><span class="sxs-lookup"><span data-stu-id="14d95-144">-Name</span></span>
<span data-ttu-id="14d95-145">수정할 인증 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-145">Specifies the name of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14d95-146">-PassThru</span></span>
<span data-ttu-id="14d95-147">passthru</span><span class="sxs-lookup"><span data-stu-id="14d95-147">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-148">-Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="14d95-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="14d95-149">리소스 소유자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="14d95-150">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-151">-Resource소유자 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="14d95-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="14d95-152">리소스 소유자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="14d95-153">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="14d95-154">-ServerId</span></span>
<span data-ttu-id="14d95-155">수정할 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-155">Specifies the ID of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="14d95-156">-SupportState</span></span>
<span data-ttu-id="14d95-157">*State* 매개 변수를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="14d95-158">-TokenBodyParameters</span></span>
<span data-ttu-id="14d95-159">Application/x-www-urlencoded 형식을 사용 하 여 추가 본문 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="14d95-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="14d95-161">권한 부여를 제공 하거나 새로 고침 토큰을 제공 하기 위해 exchange에서 액세스 토큰을 가져오는 클라이언트의 토큰 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d95-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d95-162">CommonParameters</span></span>
<span data-ttu-id="14d95-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d95-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d95-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d95-165">입력</span><span class="sxs-lookup"><span data-stu-id="14d95-165">INPUTS</span></span>

### <span data-ttu-id="14d95-166">않아야</span><span class="sxs-lookup"><span data-stu-id="14d95-166">None</span></span>
<span data-ttu-id="14d95-167">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14d95-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14d95-168">출력</span><span class="sxs-lookup"><span data-stu-id="14d95-168">OUTPUTS</span></span>

### <span data-ttu-id="14d95-169">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="14d95-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="14d95-170">상속자</span><span class="sxs-lookup"><span data-stu-id="14d95-170">NOTES</span></span>

## <span data-ttu-id="14d95-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14d95-171">RELATED LINKS</span></span>

[<span data-ttu-id="14d95-172">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14d95-172">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="14d95-173">새로운 AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14d95-173">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="14d95-174">제거-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14d95-174">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


