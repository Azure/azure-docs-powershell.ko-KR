---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049245"
---
# <span data-ttu-id="2cd51-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="2cd51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cd51-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd51-103">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-103">Creates an API.</span></span>

## <span data-ttu-id="2cd51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cd51-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2cd51-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd51-106">**AzApiManagementApi** Cmdlet은 Azure API Management api를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="2cd51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2cd51-107">EXAMPLES</span></span>

### <span data-ttu-id="2cd51-108">예제 1: API 만들기</span><span class="sxs-lookup"><span data-stu-id="2cd51-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="2cd51-109">이 명령은 지정 된 URL을 사용 하 여 EchoApi 라는 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="2cd51-110">예제 2: 모든 작업, 태그, 제품 및 정책을 echo-API에서 ApiVersionSet으로 복사 하 여 API 만들기</span><span class="sxs-lookup"><span data-stu-id="2cd51-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="2cd51-111">이 명령은 `echoapiv3` ApiVersionSet에서 API를 만들고 `xmsVersionSet` 소스 API에서 모든 작업, 태그 및 정책을 복사 `echo-api` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="2cd51-112">이 메서드는 SubscriptionRequired, ServiceUrl, Path, 프로토콜을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="2cd51-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="2cd51-113">Example 3</span></span>

<span data-ttu-id="2cd51-114">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-114">Creates an API.</span></span> <span data-ttu-id="2cd51-115">생성</span><span class="sxs-lookup"><span data-stu-id="2cd51-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="2cd51-116">변수</span><span class="sxs-lookup"><span data-stu-id="2cd51-116">PARAMETERS</span></span>

### <span data-ttu-id="2cd51-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2cd51-117">-ApiId</span></span>
<span data-ttu-id="2cd51-118">만들 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="2cd51-119">이 매개 변수를 지정 하지 않으면이 cmdlet이 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="2cd51-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2cd51-120">-ApiVersion</span></span>
<span data-ttu-id="2cd51-121">만들 Api의 api 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-121">Api Version of the Api to create.</span></span> <span data-ttu-id="2cd51-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="2cd51-123">-ApiVersionDescription</span></span>
<span data-ttu-id="2cd51-124">Api 버전 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-124">Api Version Description.</span></span> <span data-ttu-id="2cd51-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2cd51-126">-ApiVersionSetId</span></span>
<span data-ttu-id="2cd51-127">관련 Api 버전 집합에 대 한 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="2cd51-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2cd51-129">-AuthorizationScope</span></span>
<span data-ttu-id="2cd51-130">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2cd51-131">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="2cd51-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2cd51-132">-AuthorizationServerId</span></span>
<span data-ttu-id="2cd51-133">OAuth 권한 부여 서버 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="2cd51-134">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-134">The default value is $Null.</span></span>
<span data-ttu-id="2cd51-135">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2cd51-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="2cd51-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="2cd51-137">API에 액세스 토큰을 전달 하는 데 사용 되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="2cd51-138">를 참조 http://tools.ietf.org/html/rfc6749#section-4 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cd51-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="2cd51-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-139">This parameter is optional.</span></span> <span data-ttu-id="2cd51-140">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-140">Default value is $null.</span></span>

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

### <span data-ttu-id="2cd51-141">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2cd51-141">-Context</span></span>
<span data-ttu-id="2cd51-142">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2cd51-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd51-143">-DefaultProfile</span></span>
<span data-ttu-id="2cd51-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cd51-145">-설명</span><span class="sxs-lookup"><span data-stu-id="2cd51-145">-Description</span></span>
<span data-ttu-id="2cd51-146">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2cd51-147">-이름</span><span class="sxs-lookup"><span data-stu-id="2cd51-147">-Name</span></span>
<span data-ttu-id="2cd51-148">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="2cd51-149">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="2cd51-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="2cd51-150">-OpenIdProviderId</span></span>
<span data-ttu-id="2cd51-151">OpenId 인증 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="2cd51-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-152">This parameter is optional.</span></span> <span data-ttu-id="2cd51-153">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-153">Default value is $null.</span></span> <span data-ttu-id="2cd51-154">BearerTokenSendingMethods가 지정 된 경우를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="2cd51-155">-Path</span><span class="sxs-lookup"><span data-stu-id="2cd51-155">-Path</span></span>
<span data-ttu-id="2cd51-156">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 하 고 관리 포털의 웹 API URL 접미사 필드에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="2cd51-157">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2cd51-158">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="2cd51-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="2cd51-159">-ProductIds</span></span>
<span data-ttu-id="2cd51-160">새 API를 추가할 제품 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="2cd51-161">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="2cd51-161">-Protocols</span></span>
<span data-ttu-id="2cd51-162">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2cd51-163">유효한 값은 http, https입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-163">Valid values are http, https.</span></span>
<span data-ttu-id="2cd51-164">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2cd51-165">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="2cd51-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2cd51-166">-ServiceUrl</span></span>
<span data-ttu-id="2cd51-167">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2cd51-168">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2cd51-169">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2cd51-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="2cd51-170">-SourceApiId</span></span>
<span data-ttu-id="2cd51-171">원본 API의 Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-171">Api identifier of the source API.</span></span> <span data-ttu-id="2cd51-172">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="2cd51-173">-SourceApiRevision</span></span>
<span data-ttu-id="2cd51-174">원본 API의 Api 수정 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-174">Api Revision of the source API.</span></span> <span data-ttu-id="2cd51-175">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-176">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="2cd51-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2cd51-177">구독 키 헤더 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="2cd51-178">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="2cd51-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2cd51-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2cd51-180">구독 키 쿼리 문자열 매개 변수 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="2cd51-181">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="2cd51-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2cd51-182">-SubscriptionRequired</span></span>
<span data-ttu-id="2cd51-183">Api에 대 한 요청에 SubscriptionRequired 구독을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="2cd51-184">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="2cd51-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd51-185">CommonParameters</span></span>
<span data-ttu-id="2cd51-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cd51-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd51-187">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cd51-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd51-188">입력</span><span class="sxs-lookup"><span data-stu-id="2cd51-188">INPUTS</span></span>

### <span data-ttu-id="2cd51-189">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2cd51-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2cd51-190">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2cd51-190">System.String</span></span>

### <span data-ttu-id="2cd51-191">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="2cd51-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2cd51-192">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2cd51-192">System.String[]</span></span>

## <span data-ttu-id="2cd51-193">출력</span><span class="sxs-lookup"><span data-stu-id="2cd51-193">OUTPUTS</span></span>

### <span data-ttu-id="2cd51-194">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2cd51-195">상속자</span><span class="sxs-lookup"><span data-stu-id="2cd51-195">NOTES</span></span>

## <span data-ttu-id="2cd51-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cd51-196">RELATED LINKS</span></span>

[<span data-ttu-id="2cd51-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2cd51-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2cd51-199">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2cd51-200">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="2cd51-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2cd51-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


