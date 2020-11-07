---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697953"
---
# <span data-ttu-id="7ff35-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="7ff35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff35-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff35-103">API를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-103">Modifies an API.</span></span>

## <span data-ttu-id="7ff35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ff35-104">SYNTAX</span></span>

### <span data-ttu-id="7ff35-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ff35-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ff35-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7ff35-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ff35-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ff35-107">DESCRIPTION</span></span>
<span data-ttu-id="7ff35-108">**AzApiManagementApi** Cmdlet은 Azure API Management api를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="7ff35-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ff35-109">EXAMPLES</span></span>

### <span data-ttu-id="7ff35-110">예제 1 API 수정</span><span class="sxs-lookup"><span data-stu-id="7ff35-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="7ff35-111">예제 2 기존 ApiVersionSet에 API 추가</span><span class="sxs-lookup"><span data-stu-id="7ff35-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="7ff35-112">이 예제에서는 기존 API 버전 집합에 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="7ff35-113">변수</span><span class="sxs-lookup"><span data-stu-id="7ff35-113">PARAMETERS</span></span>

### <span data-ttu-id="7ff35-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7ff35-114">-ApiId</span></span>
<span data-ttu-id="7ff35-115">수정할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="7ff35-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="7ff35-116">-AuthorizationScope</span></span>
<span data-ttu-id="7ff35-117">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="7ff35-118">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="7ff35-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="7ff35-119">-AuthorizationServerId</span></span>
<span data-ttu-id="7ff35-120">OAuth 권한 부여 서버 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="7ff35-121">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-121">The default value is $Null.</span></span>
<span data-ttu-id="7ff35-122">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="7ff35-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="7ff35-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="7ff35-124">API에 액세스 토큰을 전달 하는 데 사용 되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="7ff35-125">를 참조 http://tools.ietf.org/html/rfc6749#section-4 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ff35-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="7ff35-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-126">This parameter is optional.</span></span> <span data-ttu-id="7ff35-127">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-127">Default value is $null.</span></span>

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

### <span data-ttu-id="7ff35-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7ff35-128">-Context</span></span>
<span data-ttu-id="7ff35-129">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7ff35-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff35-130">-DefaultProfile</span></span>
<span data-ttu-id="7ff35-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ff35-132">-설명</span><span class="sxs-lookup"><span data-stu-id="7ff35-132">-Description</span></span>
<span data-ttu-id="7ff35-133">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="7ff35-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ff35-134">-InputObject</span></span>
<span data-ttu-id="7ff35-135">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="7ff35-136">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-136">This parameter is required.</span></span>

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

### <span data-ttu-id="7ff35-137">-이름</span><span class="sxs-lookup"><span data-stu-id="7ff35-137">-Name</span></span>
<span data-ttu-id="7ff35-138">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="7ff35-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="7ff35-139">-OpenIdProviderId</span></span>
<span data-ttu-id="7ff35-140">OpenId 인증 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="7ff35-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-141">This parameter is optional.</span></span> <span data-ttu-id="7ff35-142">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-142">Default value is $null.</span></span> <span data-ttu-id="7ff35-143">BearerTokenSendingMethods가 지정 된 경우를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="7ff35-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ff35-144">-PassThru</span></span>
<span data-ttu-id="7ff35-145">passthru</span><span class="sxs-lookup"><span data-stu-id="7ff35-145">passthru</span></span>

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

### <span data-ttu-id="7ff35-146">-Path</span><span class="sxs-lookup"><span data-stu-id="7ff35-146">-Path</span></span>
<span data-ttu-id="7ff35-147">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="7ff35-148">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="7ff35-149">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="7ff35-150">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7ff35-150">-Protocols</span></span>
<span data-ttu-id="7ff35-151">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="7ff35-152">http 및 https를 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="7ff35-153">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="7ff35-154">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="7ff35-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7ff35-155">-ServiceUrl</span></span>
<span data-ttu-id="7ff35-156">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="7ff35-157">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="7ff35-158">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="7ff35-159">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="7ff35-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="7ff35-160">구독 키 헤더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="7ff35-161">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="7ff35-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="7ff35-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="7ff35-163">구독 키 쿼리 문자열 매개 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="7ff35-164">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="7ff35-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="7ff35-165">-SubscriptionRequired</span></span>
<span data-ttu-id="7ff35-166">Api에 대 한 요청에 SubscriptionRequired 구독을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="7ff35-167">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="7ff35-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff35-168">CommonParameters</span></span>
<span data-ttu-id="7ff35-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff35-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff35-170">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ff35-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff35-171">입력</span><span class="sxs-lookup"><span data-stu-id="7ff35-171">INPUTS</span></span>

### <span data-ttu-id="7ff35-172">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ff35-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7ff35-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7ff35-173">System.String</span></span>

### <span data-ttu-id="7ff35-174">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="7ff35-175">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="7ff35-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="7ff35-176">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ff35-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ff35-177">출력</span><span class="sxs-lookup"><span data-stu-id="7ff35-177">OUTPUTS</span></span>

### <span data-ttu-id="7ff35-178">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7ff35-179">상속자</span><span class="sxs-lookup"><span data-stu-id="7ff35-179">NOTES</span></span>

## <span data-ttu-id="7ff35-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ff35-180">RELATED LINKS</span></span>

[<span data-ttu-id="7ff35-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="7ff35-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="7ff35-183">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="7ff35-184">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="7ff35-185">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7ff35-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


