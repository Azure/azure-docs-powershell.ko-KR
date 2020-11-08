---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216462"
---
# <span data-ttu-id="bc8e3-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="bc8e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8e3-103">파일 또는 URL에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="bc8e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc8e3-104">SYNTAX</span></span>

### <span data-ttu-id="bc8e3-105">ImportFromLocalFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc8e3-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc8e3-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="bc8e3-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc8e3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc8e3-107">DESCRIPTION</span></span>
<span data-ttu-id="bc8e3-108">**AzApiManagementApi** cmdlet은 파일 또는 URL에서 Azure API Management api를 가져옵니다 (웹 응용 프로그램 설명 언어 (WADL), WSDL (웹 서비스 설명 언어) 또는 Swagger 형식).</span><span class="sxs-lookup"><span data-stu-id="bc8e3-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="bc8e3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bc8e3-109">EXAMPLES</span></span>

### <span data-ttu-id="bc8e3-110">예제 1: WADL 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc8e3-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="bc8e3-111">이 명령은 지정 된 WADL 파일에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="bc8e3-112">예제 2: Swagger 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc8e3-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="bc8e3-113">이 명령은 지정 된 Swagger 파일에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="bc8e3-114">예제 3: WADL 링크에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc8e3-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="bc8e3-115">이 명령은 지정 된 WADL 링크에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="bc8e3-116">예제 4: Open Api 링크에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc8e3-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="bc8e3-117">이 명령은 지정 된 Open 3.0 specification 링크에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="bc8e3-118">예제 5: 열려 있는 Api 링크에서 ApiVersion 집합으로 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc8e3-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="bc8e3-119">이 명령은 지정 된 Open 3.0 사양 문서에서 API를 가져와 새 ApiVersion을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="bc8e3-120">변수</span><span class="sxs-lookup"><span data-stu-id="bc8e3-120">PARAMETERS</span></span>

### <span data-ttu-id="bc8e3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bc8e3-121">-ApiId</span></span>
<span data-ttu-id="bc8e3-122">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="bc8e3-123">이 매개 변수를 지정 하지 않으면 ID가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="bc8e3-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc8e3-124">-ApiRevision</span></span>
<span data-ttu-id="bc8e3-125">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-125">Identifier of API Revision.</span></span> <span data-ttu-id="bc8e3-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-126">This parameter is optional.</span></span> <span data-ttu-id="bc8e3-127">지정 하지 않으면 현재 활성 수정 버전이 나 새 api로 가져오기가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="bc8e3-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="bc8e3-128">-ApiType</span></span>
<span data-ttu-id="bc8e3-129">이 매개 변수는 기본값 Http 값으로 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="bc8e3-130">Soap 옵션은 WSDL을 가져오는 경우에만 적용 되며 SOAP 통과 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8e3-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc8e3-131">-ApiVersion</span></span>
<span data-ttu-id="bc8e3-132">만들 Api의 api 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-132">Api Version of the Api to create.</span></span> <span data-ttu-id="bc8e3-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc8e3-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="bc8e3-134">-ApiVersionSetId</span></span>
<span data-ttu-id="bc8e3-135">관련 Api 버전 집합에 대 한 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="bc8e3-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc8e3-137">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bc8e3-137">-Context</span></span>
<span data-ttu-id="bc8e3-138">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc8e3-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8e3-139">-DefaultProfile</span></span>
<span data-ttu-id="bc8e3-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc8e3-141">-Path</span><span class="sxs-lookup"><span data-stu-id="bc8e3-141">-Path</span></span>
<span data-ttu-id="bc8e3-142">웹 API 경로를 API 공용 URL의 마지막 부분으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="bc8e3-143">이 URL은 웹 서비스로 요청을 보내기 위해 API 소비자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="bc8e3-144">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="bc8e3-145">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="bc8e3-146">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="bc8e3-146">-Protocol</span></span>
<span data-ttu-id="bc8e3-147">웹 API 프로토콜 (http, https).</span><span class="sxs-lookup"><span data-stu-id="bc8e3-147">Web API protocols (http, https).</span></span> <span data-ttu-id="bc8e3-148">사용할 수 있는 API에 대 한 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-148">Protocols over which API is made available.</span></span> <span data-ttu-id="bc8e3-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-149">This parameter is optional.</span></span> <span data-ttu-id="bc8e3-150">제공 하는 경우 사양 문서에 지정 된 프로토콜을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="bc8e3-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="bc8e3-151">-ServiceUrl</span></span>
<span data-ttu-id="bc8e3-152">API를 노출 하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="bc8e3-153">이 URL은 Azure API Management에만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="bc8e3-154">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-154">This parameter is optional.</span></span> <span data-ttu-id="bc8e3-155">제공 하는 경우 사양 문서에 지정 된 ServiceUrl을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="bc8e3-156">-사양 형식</span><span class="sxs-lookup"><span data-stu-id="bc8e3-156">-SpecificationFormat</span></span>
<span data-ttu-id="bc8e3-157">사양 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-157">Specifies the specification format.</span></span>
<span data-ttu-id="bc8e3-158">psdx_paramvalues Wadl, Wsdl 및 Swagger.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8e3-159">-사양 경로</span><span class="sxs-lookup"><span data-stu-id="bc8e3-159">-SpecificationPath</span></span>
<span data-ttu-id="bc8e3-160">사양 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8e3-161">-사양 Url</span><span class="sxs-lookup"><span data-stu-id="bc8e3-161">-SpecificationUrl</span></span>
<span data-ttu-id="bc8e3-162">사양 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8e3-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="bc8e3-163">-WsdlEndpointName</span></span>
<span data-ttu-id="bc8e3-164">가져올 WSDL 끝점 (포트)의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="bc8e3-165">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="bc8e3-166">이 매개 변수는 선택적 이며 Wsdl을 가져오는 데만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="bc8e3-167">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-167">Default value is $null.</span></span>

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

### <span data-ttu-id="bc8e3-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="bc8e3-168">-WsdlServiceName</span></span>
<span data-ttu-id="bc8e3-169">가져올 WSDL 서비스의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="bc8e3-170">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="bc8e3-171">이 매개 변수는 선택적 이며 Wsdl을 가져오는 데만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="bc8e3-172">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-172">Default value is $null.</span></span>

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

### <span data-ttu-id="bc8e3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8e3-173">CommonParameters</span></span>
<span data-ttu-id="bc8e3-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8e3-175">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc8e3-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8e3-176">입력</span><span class="sxs-lookup"><span data-stu-id="bc8e3-176">INPUTS</span></span>

### <span data-ttu-id="bc8e3-177">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc8e3-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc8e3-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc8e3-178">System.String</span></span>

### <span data-ttu-id="bc8e3-179">ApiManagement. ServiceManagement. \ PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="bc8e3-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="bc8e3-180">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementApiType, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc8e3-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bc8e3-181">출력</span><span class="sxs-lookup"><span data-stu-id="bc8e3-181">OUTPUTS</span></span>

### <span data-ttu-id="bc8e3-182">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="bc8e3-183">상속자</span><span class="sxs-lookup"><span data-stu-id="bc8e3-183">NOTES</span></span>

## <span data-ttu-id="bc8e3-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc8e3-184">RELATED LINKS</span></span>

[<span data-ttu-id="bc8e3-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="bc8e3-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="bc8e3-187">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="bc8e3-188">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="bc8e3-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc8e3-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


