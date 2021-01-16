---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381872"
---
# <span data-ttu-id="27f83-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="27f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27f83-102">SYNOPSIS</span></span>
<span data-ttu-id="27f83-103">API를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-103">Modifies an API.</span></span>

## <span data-ttu-id="27f83-104">구문</span><span class="sxs-lookup"><span data-stu-id="27f83-104">SYNTAX</span></span>

### <span data-ttu-id="27f83-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="27f83-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27f83-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27f83-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f83-107">설명</span><span class="sxs-lookup"><span data-stu-id="27f83-107">DESCRIPTION</span></span>
<span data-ttu-id="27f83-108">**Set-AzApiManagementApi** cmdlet은 Azure API Management API를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="27f83-109">예제</span><span class="sxs-lookup"><span data-stu-id="27f83-109">EXAMPLES</span></span>

### <span data-ttu-id="27f83-110">예제 1: API 수정</span><span class="sxs-lookup"><span data-stu-id="27f83-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="27f83-111">예제 2: 기존 ApiVersionSet에 API 추가</span><span class="sxs-lookup"><span data-stu-id="27f83-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="27f83-112">이 예제에서는 기존 API 버전 집합에 API를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="27f83-113">예제 3: API가 지각하는 Backend ServiceUrl 변경</span><span class="sxs-lookup"><span data-stu-id="27f83-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="27f83-114">이 예제에서는 포인터가 있는 ServiceUrl을 `echo-api` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="27f83-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27f83-115">PARAMETERS</span></span>

### <span data-ttu-id="27f83-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="27f83-116">-ApiId</span></span>
<span data-ttu-id="27f83-117">수정할 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="27f83-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="27f83-118">-AuthorizationScope</span></span>
<span data-ttu-id="27f83-119">OAuth 작업 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="27f83-120">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="27f83-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="27f83-121">-AuthorizationServerId</span></span>
<span data-ttu-id="27f83-122">OAuth 권한 부여 서버 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="27f83-123">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-123">The default value is $Null.</span></span>
<span data-ttu-id="27f83-124">*AuthorizationScope가* 지정된 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="27f83-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="27f83-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="27f83-126">액세스 토큰이 API에 전달되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="27f83-127">.를 http://tools.ietf.org/html/rfc6749#section-4 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="27f83-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-128">This parameter is optional.</span></span> <span data-ttu-id="27f83-129">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="27f83-129">Default value is $null.</span></span>

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

### <span data-ttu-id="27f83-130">-Context</span><span class="sxs-lookup"><span data-stu-id="27f83-130">-Context</span></span>
<span data-ttu-id="27f83-131">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="27f83-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="27f83-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f83-132">-DefaultProfile</span></span>
<span data-ttu-id="27f83-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27f83-134">-Description</span><span class="sxs-lookup"><span data-stu-id="27f83-134">-Description</span></span>
<span data-ttu-id="27f83-135">웹 API에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="27f83-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27f83-136">-InputObject</span></span>
<span data-ttu-id="27f83-137">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="27f83-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-138">This parameter is required.</span></span>

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

### <span data-ttu-id="27f83-139">-Name</span><span class="sxs-lookup"><span data-stu-id="27f83-139">-Name</span></span>
<span data-ttu-id="27f83-140">웹 API의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="27f83-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="27f83-141">-OpenIdProviderId</span></span>
<span data-ttu-id="27f83-142">OpenId 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="27f83-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-143">This parameter is optional.</span></span> <span data-ttu-id="27f83-144">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="27f83-144">Default value is $null.</span></span> <span data-ttu-id="27f83-145">BearerTokenSendingMethods를 지정하는 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="27f83-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27f83-146">-PassThru</span></span>
<span data-ttu-id="27f83-147">passthru</span><span class="sxs-lookup"><span data-stu-id="27f83-147">passthru</span></span>

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

### <span data-ttu-id="27f83-148">-Path</span><span class="sxs-lookup"><span data-stu-id="27f83-148">-Path</span></span>
<span data-ttu-id="27f83-149">API 공용 URL의 마지막 부분인 웹 API 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="27f83-150">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용하며, 1~400자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="27f83-151">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="27f83-152">-Protocols</span><span class="sxs-lookup"><span data-stu-id="27f83-152">-Protocols</span></span>
<span data-ttu-id="27f83-153">Web API 프로토콜의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="27f83-154">psdx_paramvalues http 및 https를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="27f83-155">API를 사용할 수 있는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="27f83-156">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="27f83-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="27f83-157">-ServiceUrl</span></span>
<span data-ttu-id="27f83-158">API를 노출하는 웹 서비스의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="27f83-159">이 URL은 Azure API Management에서만 사용하며 공개되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="27f83-160">URL은 1~2,000자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="27f83-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="27f83-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="27f83-162">구독 키 헤더의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="27f83-163">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="27f83-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="27f83-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="27f83-165">구독 키 쿼리 문자열 매개 변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="27f83-166">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="27f83-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="27f83-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="27f83-167">-SubscriptionRequired</span></span>
<span data-ttu-id="27f83-168">Api에 대한 요청에 대한 SubscriptionRequired를 적용하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="27f83-169">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="27f83-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f83-170">CommonParameters</span></span>
<span data-ttu-id="27f83-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27f83-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f83-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27f83-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f83-173">입력</span><span class="sxs-lookup"><span data-stu-id="27f83-173">INPUTS</span></span>

### <span data-ttu-id="27f83-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27f83-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27f83-175">System.String</span><span class="sxs-lookup"><span data-stu-id="27f83-175">System.String</span></span>

### <span data-ttu-id="27f83-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="27f83-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="27f83-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="27f83-178">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="27f83-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="27f83-179">출력</span><span class="sxs-lookup"><span data-stu-id="27f83-179">OUTPUTS</span></span>

### <span data-ttu-id="27f83-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="27f83-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27f83-181">NOTES</span></span>

## <span data-ttu-id="27f83-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27f83-182">RELATED LINKS</span></span>

[<span data-ttu-id="27f83-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="27f83-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="27f83-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="27f83-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="27f83-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="27f83-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


