---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045000"
---
# <span data-ttu-id="75c0e-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="75c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="75c0e-103">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-103">Creates an API.</span></span>

## <span data-ttu-id="75c0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75c0e-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75c0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="75c0e-106">**AzApiManagementApi** Cmdlet은 Azure API Management api를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="75c0e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="75c0e-108">예제 1: API 만들기</span><span class="sxs-lookup"><span data-stu-id="75c0e-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="75c0e-109">이 명령은 지정 된 URL을 사용 하 여 EchoApi 라는 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="75c0e-110">예제 1: 모든 작업, 태그, 제품 및 정책을 echo-API에서 ApiVersionSet으로 복사 하 여 API 만들기</span><span class="sxs-lookup"><span data-stu-id="75c0e-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="75c0e-111">이 명령은 `echoapiv3` ApiVersionSet에서 API를 만들고 `xmsVersionSet` 소스 API에서 모든 작업, 태그 및 정책을 복사 `echo-api` 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="75c0e-112">이 메서드는 SubscriptionRequired, ServiceUrl, Path, 프로토콜을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="75c0e-113">변수</span><span class="sxs-lookup"><span data-stu-id="75c0e-113">PARAMETERS</span></span>

### <span data-ttu-id="75c0e-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="75c0e-114">-ApiId</span></span>
<span data-ttu-id="75c0e-115">만들 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="75c0e-116">이 매개 변수를 지정 하지 않으면이 cmdlet이 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="75c0e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75c0e-117">-ApiVersion</span></span>
<span data-ttu-id="75c0e-118">만들 Api의 api 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-118">Api Version of the Api to create.</span></span> <span data-ttu-id="75c0e-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="75c0e-120">-ApiVersionDescription</span></span>
<span data-ttu-id="75c0e-121">Api 버전 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-121">Api Version Description.</span></span> <span data-ttu-id="75c0e-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="75c0e-123">-ApiVersionSetId</span></span>
<span data-ttu-id="75c0e-124">관련 Api 버전 집합에 대 한 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="75c0e-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="75c0e-126">-AuthorizationScope</span></span>
<span data-ttu-id="75c0e-127">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="75c0e-128">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="75c0e-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="75c0e-129">-AuthorizationServerId</span></span>
<span data-ttu-id="75c0e-130">OAuth 권한 부여 서버 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="75c0e-131">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-131">The default value is $Null.</span></span>
<span data-ttu-id="75c0e-132">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="75c0e-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="75c0e-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="75c0e-134">API에 액세스 토큰을 전달 하는 데 사용 되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="75c0e-135">를 참조 http://tools.ietf.org/html/rfc6749#section-4 하세요.</span><span class="sxs-lookup"><span data-stu-id="75c0e-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="75c0e-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-136">This parameter is optional.</span></span> <span data-ttu-id="75c0e-137">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-137">Default value is $null.</span></span>

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

### <span data-ttu-id="75c0e-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="75c0e-138">-Context</span></span>
<span data-ttu-id="75c0e-139">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-139">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="75c0e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c0e-140">-DefaultProfile</span></span>
<span data-ttu-id="75c0e-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c0e-142">-설명</span><span class="sxs-lookup"><span data-stu-id="75c0e-142">-Description</span></span>
<span data-ttu-id="75c0e-143">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="75c0e-144">-이름</span><span class="sxs-lookup"><span data-stu-id="75c0e-144">-Name</span></span>
<span data-ttu-id="75c0e-145">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="75c0e-146">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="75c0e-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="75c0e-147">-OpenIdProviderId</span></span>
<span data-ttu-id="75c0e-148">OpenId 인증 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="75c0e-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-149">This parameter is optional.</span></span> <span data-ttu-id="75c0e-150">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-150">Default value is $null.</span></span> <span data-ttu-id="75c0e-151">BearerTokenSendingMethods가 지정 된 경우를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="75c0e-152">-Path</span><span class="sxs-lookup"><span data-stu-id="75c0e-152">-Path</span></span>
<span data-ttu-id="75c0e-153">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 하 고 관리 포털의 웹 API URL 접미사 필드에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="75c0e-154">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="75c0e-155">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="75c0e-156">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="75c0e-156">-ProductIds</span></span>
<span data-ttu-id="75c0e-157">새 API를 추가할 제품 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="75c0e-158">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="75c0e-158">-Protocols</span></span>
<span data-ttu-id="75c0e-159">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="75c0e-160">유효한 값은 http, https입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-160">Valid values are http, https.</span></span>
<span data-ttu-id="75c0e-161">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="75c0e-162">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-162">The default value is $Null.</span></span>

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

### <span data-ttu-id="75c0e-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="75c0e-163">-ServiceUrl</span></span>
<span data-ttu-id="75c0e-164">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="75c0e-165">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="75c0e-166">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="75c0e-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="75c0e-167">-SourceApiId</span></span>
<span data-ttu-id="75c0e-168">원본 API의 Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-168">Api identifier of the source API.</span></span> <span data-ttu-id="75c0e-169">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="75c0e-170">-SourceApiRevision</span></span>
<span data-ttu-id="75c0e-171">원본 API의 Api 수정 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-171">Api Revision of the source API.</span></span> <span data-ttu-id="75c0e-172">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-173">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="75c0e-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="75c0e-174">구독 키 헤더 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="75c0e-175">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="75c0e-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="75c0e-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="75c0e-177">구독 키 쿼리 문자열 매개 변수 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="75c0e-178">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="75c0e-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="75c0e-179">-SubscriptionRequired</span></span>
<span data-ttu-id="75c0e-180">Api에 대 한 요청에 SubscriptionRequired 구독을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="75c0e-181">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="75c0e-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c0e-182">CommonParameters</span></span>
<span data-ttu-id="75c0e-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75c0e-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c0e-184">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75c0e-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c0e-185">입력</span><span class="sxs-lookup"><span data-stu-id="75c0e-185">INPUTS</span></span>

### <span data-ttu-id="75c0e-186">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75c0e-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75c0e-187">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75c0e-187">System.String</span></span>

### <span data-ttu-id="75c0e-188">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="75c0e-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="75c0e-189">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="75c0e-189">System.String[]</span></span>

## <span data-ttu-id="75c0e-190">출력</span><span class="sxs-lookup"><span data-stu-id="75c0e-190">OUTPUTS</span></span>

### <span data-ttu-id="75c0e-191">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="75c0e-192">상속자</span><span class="sxs-lookup"><span data-stu-id="75c0e-192">NOTES</span></span>

## <span data-ttu-id="75c0e-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75c0e-193">RELATED LINKS</span></span>

[<span data-ttu-id="75c0e-194">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="75c0e-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="75c0e-196">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="75c0e-197">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="75c0e-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="75c0e-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


