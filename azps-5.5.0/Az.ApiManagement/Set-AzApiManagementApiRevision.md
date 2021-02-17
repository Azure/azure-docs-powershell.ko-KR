---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210312"
---
# <span data-ttu-id="537d8-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="537d8-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="537d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="537d8-102">SYNOPSIS</span></span>
<span data-ttu-id="537d8-103">API 수정 수정</span><span class="sxs-lookup"><span data-stu-id="537d8-103">Modifies an API Revision</span></span>

## <span data-ttu-id="537d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="537d8-104">SYNTAX</span></span>

### <span data-ttu-id="537d8-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="537d8-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="537d8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="537d8-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="537d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="537d8-107">DESCRIPTION</span></span>
<span data-ttu-id="537d8-108">**Set-AzApiManagementApiRevision** cmdlet은 Azure API Management API 수정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="537d8-109">예제</span><span class="sxs-lookup"><span data-stu-id="537d8-109">EXAMPLES</span></span>

### <span data-ttu-id="537d8-110">예제 1: API 수정</span><span class="sxs-lookup"><span data-stu-id="537d8-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="537d8-111">cmdlet은 새 설명, 프로토콜 및 경로로 `2` API의 `echo-api` 개정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="537d8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="537d8-112">PARAMETERS</span></span>

### <span data-ttu-id="537d8-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="537d8-113">-ApiId</span></span>
<span data-ttu-id="537d8-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-114">Identifier of existing API.</span></span>
<span data-ttu-id="537d8-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-115">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="537d8-116">-ApiRevision</span></span>
<span data-ttu-id="537d8-117">기존 API 수정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="537d8-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="537d8-119">-AuthorizationScope</span></span>
<span data-ttu-id="537d8-120">OAuth 작업 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-120">OAuth operations scope.</span></span>
<span data-ttu-id="537d8-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-121">This parameter is optional.</span></span>
<span data-ttu-id="537d8-122">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-122">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="537d8-123">-AuthorizationServerId</span></span>
<span data-ttu-id="537d8-124">OAuth 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="537d8-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-125">This parameter is optional.</span></span>
<span data-ttu-id="537d8-126">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-126">Default value is $null.</span></span>
<span data-ttu-id="537d8-127">AuthorizationScope가 지정된 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="537d8-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="537d8-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="537d8-129">액세스 토큰이 API에 전달되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="537d8-130">.를 http://tools.ietf.org/html/rfc6749#section-4 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="537d8-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-131">This parameter is optional.</span></span> <span data-ttu-id="537d8-132">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-132">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-133">-Context</span><span class="sxs-lookup"><span data-stu-id="537d8-133">-Context</span></span>
<span data-ttu-id="537d8-134">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="537d8-135">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-135">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537d8-136">-DefaultProfile</span></span>
<span data-ttu-id="537d8-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537d8-138">-Description</span><span class="sxs-lookup"><span data-stu-id="537d8-138">-Description</span></span>
<span data-ttu-id="537d8-139">Web API 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-139">Web API description.</span></span>
<span data-ttu-id="537d8-140">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="537d8-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="537d8-141">-InputObject</span></span>
<span data-ttu-id="537d8-142">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="537d8-143">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-143">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-144">-Name</span><span class="sxs-lookup"><span data-stu-id="537d8-144">-Name</span></span>
<span data-ttu-id="537d8-145">Web API 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-145">Web API name.</span></span>
<span data-ttu-id="537d8-146">개발자 및 관리 포털에 나타나는 API의 공용 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="537d8-147">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-147">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="537d8-148">-OpenIdProviderId</span></span>
<span data-ttu-id="537d8-149">OpenId 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="537d8-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-150">This parameter is optional.</span></span> <span data-ttu-id="537d8-151">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-151">Default value is $null.</span></span> <span data-ttu-id="537d8-152">BearerTokenSendingMethods를 지정하는 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="537d8-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="537d8-153">-PassThru</span></span>
<span data-ttu-id="537d8-154">지정된 경우 집합 API를 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi 형식의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="537d8-155">-Path</span><span class="sxs-lookup"><span data-stu-id="537d8-155">-Path</span></span>
<span data-ttu-id="537d8-156">Web API 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-156">Web API Path.</span></span>
<span data-ttu-id="537d8-157">API의 공용 URL의 마지막 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="537d8-158">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="537d8-159">1~400자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="537d8-160">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-160">This parameter is optional.</span></span>
<span data-ttu-id="537d8-161">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-161">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="537d8-162">-Protocols</span></span>
<span data-ttu-id="537d8-163">Web API 프로토콜(http, https).</span><span class="sxs-lookup"><span data-stu-id="537d8-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="537d8-164">API를 사용할 수 있는 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="537d8-165">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-165">This parameter is required.</span></span>
<span data-ttu-id="537d8-166">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-166">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="537d8-167">-ServiceUrl</span></span>
<span data-ttu-id="537d8-168">API를 노출하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="537d8-169">이 URL은 Azure API Management에서만 사용하며 공개되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="537d8-170">1~2,000자 이상이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="537d8-171">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-171">This parameter is required.</span></span>

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

### <span data-ttu-id="537d8-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="537d8-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="537d8-173">구독 키 헤더 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-173">Subscription key header name.</span></span>
<span data-ttu-id="537d8-174">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-174">This parameter is optional.</span></span>
<span data-ttu-id="537d8-175">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-175">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="537d8-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="537d8-177">구독 키 쿼리 문자열 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="537d8-178">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-178">This parameter is optional.</span></span>
<span data-ttu-id="537d8-179">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="537d8-179">Default value is $null.</span></span>

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

### <span data-ttu-id="537d8-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="537d8-180">-SubscriptionRequired</span></span>
<span data-ttu-id="537d8-181">Api에 대한 요청에 대한 SubscriptionRequired를 적용하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="537d8-182">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="537d8-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="537d8-183">-Confirm</span></span>
<span data-ttu-id="537d8-184">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537d8-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="537d8-185">-WhatIf</span></span>
<span data-ttu-id="537d8-186">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="537d8-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="537d8-187">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537d8-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537d8-188">CommonParameters</span></span>
<span data-ttu-id="537d8-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="537d8-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537d8-190">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="537d8-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537d8-191">입력</span><span class="sxs-lookup"><span data-stu-id="537d8-191">INPUTS</span></span>

### <span data-ttu-id="537d8-192">System.String</span><span class="sxs-lookup"><span data-stu-id="537d8-192">System.String</span></span>

### <span data-ttu-id="537d8-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="537d8-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="537d8-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="537d8-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="537d8-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="537d8-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="537d8-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="537d8-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="537d8-197">출력</span><span class="sxs-lookup"><span data-stu-id="537d8-197">OUTPUTS</span></span>

### <span data-ttu-id="537d8-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="537d8-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="537d8-199">참고 사항</span><span class="sxs-lookup"><span data-stu-id="537d8-199">NOTES</span></span>

## <span data-ttu-id="537d8-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="537d8-200">RELATED LINKS</span></span>

[<span data-ttu-id="537d8-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="537d8-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="537d8-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="537d8-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="537d8-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="537d8-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)