---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 482a558e469e3f8094e4b619ef61ec37f076f739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043865"
---
# <span data-ttu-id="41766-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="41766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41766-102">SYNOPSIS</span></span>
<span data-ttu-id="41766-103">API를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-103">Modifies an API.</span></span>

## <span data-ttu-id="41766-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41766-104">SYNTAX</span></span>

### <span data-ttu-id="41766-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="41766-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41766-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41766-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41766-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41766-107">DESCRIPTION</span></span>
<span data-ttu-id="41766-108">**AzApiManagementApi** Cmdlet은 Azure API Management api를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="41766-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41766-109">EXAMPLES</span></span>

### <span data-ttu-id="41766-110">예제 1 API 수정</span><span class="sxs-lookup"><span data-stu-id="41766-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="41766-111">예제 2 기존 ApiVersionSet에 API 추가</span><span class="sxs-lookup"><span data-stu-id="41766-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="41766-112">이 예제에서는 기존 API 버전 집합에 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="41766-113">예제 3 API가 가리키는 백 엔드 ServiceUrl 변경</span><span class="sxs-lookup"><span data-stu-id="41766-113">Example 3 Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="41766-114">이 예제에서는가 가리키는 ServiceUrl을 업데이트 `echo-api` 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="41766-115">변수</span><span class="sxs-lookup"><span data-stu-id="41766-115">PARAMETERS</span></span>

### <span data-ttu-id="41766-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="41766-116">-ApiId</span></span>
<span data-ttu-id="41766-117">수정할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-117">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41766-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="41766-118">-AuthorizationScope</span></span>
<span data-ttu-id="41766-119">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="41766-120">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="41766-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="41766-121">-AuthorizationServerId</span></span>
<span data-ttu-id="41766-122">OAuth 권한 부여 서버 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="41766-123">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-123">The default value is $Null.</span></span>
<span data-ttu-id="41766-124">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="41766-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="41766-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="41766-126">API에 액세스 토큰을 전달 하는 데 사용 되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="41766-127">를 참조 http://tools.ietf.org/html/rfc6749#section-4 하세요.</span><span class="sxs-lookup"><span data-stu-id="41766-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="41766-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-128">This parameter is optional.</span></span> <span data-ttu-id="41766-129">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-129">Default value is $null.</span></span>

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

### <span data-ttu-id="41766-130">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="41766-130">-Context</span></span>
<span data-ttu-id="41766-131">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-131">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41766-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41766-132">-DefaultProfile</span></span>
<span data-ttu-id="41766-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41766-134">-설명</span><span class="sxs-lookup"><span data-stu-id="41766-134">-Description</span></span>
<span data-ttu-id="41766-135">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="41766-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41766-136">-InputObject</span></span>
<span data-ttu-id="41766-137">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="41766-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41766-139">-이름</span><span class="sxs-lookup"><span data-stu-id="41766-139">-Name</span></span>
<span data-ttu-id="41766-140">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="41766-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="41766-141">-OpenIdProviderId</span></span>
<span data-ttu-id="41766-142">OpenId 인증 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="41766-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-143">This parameter is optional.</span></span> <span data-ttu-id="41766-144">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-144">Default value is $null.</span></span> <span data-ttu-id="41766-145">BearerTokenSendingMethods가 지정 된 경우를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="41766-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41766-146">-PassThru</span></span>
<span data-ttu-id="41766-147">passthru</span><span class="sxs-lookup"><span data-stu-id="41766-147">passthru</span></span>

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

### <span data-ttu-id="41766-148">-Path</span><span class="sxs-lookup"><span data-stu-id="41766-148">-Path</span></span>
<span data-ttu-id="41766-149">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="41766-150">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="41766-151">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="41766-152">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="41766-152">-Protocols</span></span>
<span data-ttu-id="41766-153">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="41766-154">http 및 https를 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="41766-155">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="41766-156">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-156">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41766-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="41766-157">-ServiceUrl</span></span>
<span data-ttu-id="41766-158">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="41766-159">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41766-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="41766-160">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="41766-161">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="41766-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="41766-162">구독 키 헤더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="41766-163">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="41766-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="41766-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="41766-165">구독 키 쿼리 문자열 매개 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="41766-166">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="41766-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="41766-167">-SubscriptionRequired</span></span>
<span data-ttu-id="41766-168">Api에 대 한 요청에 SubscriptionRequired 구독을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="41766-169">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="41766-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="41766-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41766-170">CommonParameters</span></span>
<span data-ttu-id="41766-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41766-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41766-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="41766-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41766-173">입력</span><span class="sxs-lookup"><span data-stu-id="41766-173">INPUTS</span></span>

### <span data-ttu-id="41766-174">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41766-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41766-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41766-175">System.String</span></span>

### <span data-ttu-id="41766-176">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="41766-177">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="41766-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="41766-178">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="41766-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41766-179">출력</span><span class="sxs-lookup"><span data-stu-id="41766-179">OUTPUTS</span></span>

### <span data-ttu-id="41766-180">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="41766-181">상속자</span><span class="sxs-lookup"><span data-stu-id="41766-181">NOTES</span></span>

## <span data-ttu-id="41766-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41766-182">RELATED LINKS</span></span>

[<span data-ttu-id="41766-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="41766-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="41766-185">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="41766-186">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="41766-187">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="41766-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


