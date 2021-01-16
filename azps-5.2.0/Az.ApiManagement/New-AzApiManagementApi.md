---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364596"
---
# <span data-ttu-id="108e2-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="108e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108e2-102">SYNOPSIS</span></span>
<span data-ttu-id="108e2-103">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-103">Creates an API.</span></span>

## <span data-ttu-id="108e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="108e2-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="108e2-105">DESCRIPTION</span></span>
<span data-ttu-id="108e2-106">**New-AzApiManagementApi** cmdlet은 Azure API Management API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="108e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="108e2-107">EXAMPLES</span></span>

### <span data-ttu-id="108e2-108">예제 1: API 만들기</span><span class="sxs-lookup"><span data-stu-id="108e2-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="108e2-109">이 명령은 지정된 URL을 사용하여 EchoApi라는 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="108e2-110">예제 2: echo-api 및 ApiVersionSet에 모든 작업, 태그, 제품 및 정책을 복사하여 API 만들기</span><span class="sxs-lookup"><span data-stu-id="108e2-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="108e2-111">이 명령은 ApiVersionSet에서 API를 만들고 원본 API에서 모든 `echoapiv3` `xmsVersionSet` 작업, 태그 및 정책을 `echo-api` 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="108e2-112">SubscriptionRequired, ServiceUrl, Path, Protocols를 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="108e2-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="108e2-113">Example 3</span></span>

<span data-ttu-id="108e2-114">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-114">Creates an API.</span></span> <span data-ttu-id="108e2-115">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="108e2-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="108e2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108e2-116">PARAMETERS</span></span>

### <span data-ttu-id="108e2-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="108e2-117">-ApiId</span></span>
<span data-ttu-id="108e2-118">만들 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="108e2-119">이 매개 변수를 지정하지 않으면 이 cmdlet에서 ID를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="108e2-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="108e2-120">-ApiVersion</span></span>
<span data-ttu-id="108e2-121">만들 API의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-121">Api Version of the Api to create.</span></span> <span data-ttu-id="108e2-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="108e2-123">-ApiVersionDescription</span></span>
<span data-ttu-id="108e2-124">API 버전 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-124">Api Version Description.</span></span> <span data-ttu-id="108e2-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="108e2-126">-ApiVersionSetId</span></span>
<span data-ttu-id="108e2-127">관련 API 버전 집합에 대한 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="108e2-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="108e2-129">-AuthorizationScope</span></span>
<span data-ttu-id="108e2-130">OAuth 작업 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="108e2-131">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="108e2-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="108e2-132">-AuthorizationServerId</span></span>
<span data-ttu-id="108e2-133">OAuth 권한 부여 서버 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="108e2-134">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-134">The default value is $Null.</span></span>
<span data-ttu-id="108e2-135">*AuthorizationScope가* 지정된 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="108e2-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="108e2-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="108e2-137">액세스 토큰이 API에 전달되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="108e2-138">.를 http://tools.ietf.org/html/rfc6749#section-4 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="108e2-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-139">This parameter is optional.</span></span> <span data-ttu-id="108e2-140">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="108e2-140">Default value is $null.</span></span>

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

### <span data-ttu-id="108e2-141">-Context</span><span class="sxs-lookup"><span data-stu-id="108e2-141">-Context</span></span>
<span data-ttu-id="108e2-142">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="108e2-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="108e2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108e2-143">-DefaultProfile</span></span>
<span data-ttu-id="108e2-144">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="108e2-145">-Description</span><span class="sxs-lookup"><span data-stu-id="108e2-145">-Description</span></span>
<span data-ttu-id="108e2-146">웹 API에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="108e2-147">-Name</span><span class="sxs-lookup"><span data-stu-id="108e2-147">-Name</span></span>
<span data-ttu-id="108e2-148">웹 API의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="108e2-149">개발자 및 관리 포털에 나타나는 API의 공용 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="108e2-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="108e2-150">-OpenIdProviderId</span></span>
<span data-ttu-id="108e2-151">OpenId 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="108e2-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-152">This parameter is optional.</span></span> <span data-ttu-id="108e2-153">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="108e2-153">Default value is $null.</span></span> <span data-ttu-id="108e2-154">BearerTokenSendingMethods를 지정하는 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="108e2-155">-Path</span><span class="sxs-lookup"><span data-stu-id="108e2-155">-Path</span></span>
<span data-ttu-id="108e2-156">API의 공용 URL의 마지막 부분인 웹 API 경로를 지정하고 관리 포털의 Web API URL 접미사 필드에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="108e2-157">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용하며, 1~400자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="108e2-158">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="108e2-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="108e2-159">-ProductIds</span></span>
<span data-ttu-id="108e2-160">새 API를 추가할 제품 ID의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="108e2-161">-Protocols</span><span class="sxs-lookup"><span data-stu-id="108e2-161">-Protocols</span></span>
<span data-ttu-id="108e2-162">Web API 프로토콜의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="108e2-163">유효한 값은 http, https입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-163">Valid values are http, https.</span></span>
<span data-ttu-id="108e2-164">API를 사용할 수 있는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="108e2-165">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-165">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108e2-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="108e2-166">-ServiceUrl</span></span>
<span data-ttu-id="108e2-167">API를 노출하는 웹 서비스의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="108e2-168">이 URL은 Azure API Management에서만 사용하며 공개되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="108e2-169">URL은 1~2,000자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="108e2-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="108e2-170">-SourceApiId</span></span>
<span data-ttu-id="108e2-171">원본 API의 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-171">Api identifier of the source API.</span></span> <span data-ttu-id="108e2-172">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="108e2-173">-SourceApiRevision</span></span>
<span data-ttu-id="108e2-174">원본 API의 API 개정입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-174">Api Revision of the source API.</span></span> <span data-ttu-id="108e2-175">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="108e2-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="108e2-177">구독 키 헤더 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="108e2-178">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="108e2-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="108e2-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="108e2-180">구독 키 쿼리 문자열 매개 변수 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="108e2-181">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="108e2-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="108e2-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="108e2-182">-SubscriptionRequired</span></span>
<span data-ttu-id="108e2-183">Api에 대한 요청에 대한 SubscriptionRequired를 적용하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="108e2-184">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="108e2-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108e2-185">CommonParameters</span></span>
<span data-ttu-id="108e2-186">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="108e2-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108e2-187">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="108e2-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108e2-188">입력</span><span class="sxs-lookup"><span data-stu-id="108e2-188">INPUTS</span></span>

### <span data-ttu-id="108e2-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="108e2-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="108e2-190">System.String</span><span class="sxs-lookup"><span data-stu-id="108e2-190">System.String</span></span>

### <span data-ttu-id="108e2-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="108e2-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="108e2-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="108e2-192">System.String[]</span></span>

## <span data-ttu-id="108e2-193">출력</span><span class="sxs-lookup"><span data-stu-id="108e2-193">OUTPUTS</span></span>

### <span data-ttu-id="108e2-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="108e2-195">참고 사항</span><span class="sxs-lookup"><span data-stu-id="108e2-195">NOTES</span></span>

## <span data-ttu-id="108e2-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="108e2-196">RELATED LINKS</span></span>

[<span data-ttu-id="108e2-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="108e2-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="108e2-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="108e2-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="108e2-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108e2-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


