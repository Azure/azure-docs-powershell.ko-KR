---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: f1853c8f9e1e8449d0b607cadede215ec42b8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702552"
---
# <span data-ttu-id="1c425-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1c425-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1c425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c425-102">SYNOPSIS</span></span>
<span data-ttu-id="1c425-103">권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c425-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c425-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c425-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c425-105">DESCRIPTION</span></span>
<span data-ttu-id="1c425-106">**AzureRmApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1c425-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c425-107">EXAMPLES</span></span>

### <span data-ttu-id="1c425-108">예제 1: 권한 부여 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="1c425-108">Example 1: Create an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="1c425-109">이 명령은 권한 부여 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="1c425-110">변수</span><span class="sxs-lookup"><span data-stu-id="1c425-110">PARAMETERS</span></span>

### <span data-ttu-id="1c425-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="1c425-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="1c425-112">액세스 토큰을 보낼 메서드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="1c425-113">psdx_paramvalues AuthorizationHeader 및 Query.</span><span class="sxs-lookup"><span data-stu-id="1c425-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="1c425-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1c425-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="1c425-115">리소스 소유자를 인증 하 고 권한 부여 권한을 얻을 수 있는 권한 부여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="1c425-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="1c425-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="1c425-117">인증 요청 메서드 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="1c425-118">유효한 값은 GET, POST입니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="1c425-119">기본 값은 GET입니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-119">The default value is GET.</span></span>

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

### <span data-ttu-id="1c425-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="1c425-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="1c425-121">클라이언트 인증 방법의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="1c425-122">기본 및 본문을 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="1c425-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1c425-123">-ClientId</span></span>
<span data-ttu-id="1c425-124">클라이언트 응용 프로그램에 해당 하는 개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="1c425-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="1c425-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="1c425-126">인증 서버에 클라이언트를 등록 하 고 클라이언트 자격 증명을 가져오는 클라이언트 등록 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="1c425-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1c425-127">-ClientSecret</span></span>
<span data-ttu-id="1c425-128">클라이언트 응용 프로그램 개발자 콘솔의 클라이언트 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="1c425-129">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1c425-129">-Context</span></span>
<span data-ttu-id="1c425-130">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1c425-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c425-131">-DefaultProfile</span></span>
<span data-ttu-id="1c425-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1c425-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="1c425-133">-DefaultScope</span></span>
<span data-ttu-id="1c425-134">권한 부여 서버의 기본 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="1c425-135">-설명</span><span class="sxs-lookup"><span data-stu-id="1c425-135">-Description</span></span>
<span data-ttu-id="1c425-136">권한 부여 서버에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="1c425-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="1c425-137">-GrantTypes</span></span>
<span data-ttu-id="1c425-138">허용 형식 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="1c425-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1c425-139">psdx_paramvalues</span></span>

- <span data-ttu-id="1c425-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="1c425-140">AuthorizationCode</span></span>
- <span data-ttu-id="1c425-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="1c425-141">ClientCredentials</span></span> 
- <span data-ttu-id="1c425-142">명시적</span><span class="sxs-lookup"><span data-stu-id="1c425-142">Implicit</span></span> 
- <span data-ttu-id="1c425-143">Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="1c425-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="1c425-144">-이름</span><span class="sxs-lookup"><span data-stu-id="1c425-144">-Name</span></span>
<span data-ttu-id="1c425-145">만들 인증 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="1c425-146">-Resource소유자 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="1c425-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="1c425-147">리소스 소유자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="1c425-148">*GrantTypes* 매개 변수로 Resource소유 암호를 지정한 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1c425-149">-Resource소유자 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="1c425-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="1c425-150">리소스 소유자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="1c425-151">Resource소유 암호가 *GrantTypes* 매개 변수로 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1c425-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1c425-152">-ServerId</span></span>
<span data-ttu-id="1c425-153">만들 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="1c425-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="1c425-154">-SupportState</span></span>
<span data-ttu-id="1c425-155">*State* 매개 변수를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="1c425-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="1c425-156">-TokenBodyParameters</span></span>
<span data-ttu-id="1c425-157">**Application/x-www-urlencoded** 형식을 사용 하 여 추가 본문 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="1c425-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1c425-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="1c425-159">권한 부여를 제공 하거나 새로 고침 토큰을 제공 하기 위해 exchange에서 액세스 토큰을 가져오기 위해 클라이언트에서 사용 하는 토큰 끝점 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="1c425-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c425-160">CommonParameters</span></span>
<span data-ttu-id="1c425-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c425-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c425-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c425-163">입력</span><span class="sxs-lookup"><span data-stu-id="1c425-163">INPUTS</span></span>

### <span data-ttu-id="1c425-164">않아야</span><span class="sxs-lookup"><span data-stu-id="1c425-164">None</span></span>
<span data-ttu-id="1c425-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c425-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c425-166">출력</span><span class="sxs-lookup"><span data-stu-id="1c425-166">OUTPUTS</span></span>

### <span data-ttu-id="1c425-167">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="1c425-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="1c425-168">상속자</span><span class="sxs-lookup"><span data-stu-id="1c425-168">NOTES</span></span>

## <span data-ttu-id="1c425-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c425-169">RELATED LINKS</span></span>

