---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 604ba6be4129b627f10f879e6272eb0bc1cfbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962544"
---
# <span data-ttu-id="51ba7-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="51ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="51ba7-103">파일 또는 URL에서 API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="51ba7-104">구문</span><span class="sxs-lookup"><span data-stu-id="51ba7-104">SYNTAX</span></span>

### <span data-ttu-id="51ba7-105">ImportFromLocalFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="51ba7-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ba7-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="51ba7-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ba7-107">설명</span><span class="sxs-lookup"><span data-stu-id="51ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="51ba7-108">**Import-AzApiManagementApi** cmdlet은 WADL(웹 애플리케이션 설명 언어), 웹 서비스 설명 언어(WSDL) 또는 Swagger 형식의 파일 또는 URL에서 Azure API Management API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="51ba7-109">예제</span><span class="sxs-lookup"><span data-stu-id="51ba7-109">EXAMPLES</span></span>

### <span data-ttu-id="51ba7-110">예제 1: WADL 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="51ba7-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="51ba7-111">이 명령은 지정된 WADL 파일에서 API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="51ba7-112">예제 2: Swagger 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="51ba7-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="51ba7-113">이 명령은 지정된 Swagger 파일에서 API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="51ba7-114">예제 3: WADL 링크에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="51ba7-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="51ba7-115">이 명령은 지정된 WADL 링크에서 API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="51ba7-116">예제 4: 오픈 API 링크에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="51ba7-116">Example 4: Import an API from a Open Api Link</span></span>
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

<span data-ttu-id="51ba7-117">이 명령은 지정된 Open 3.0 사양 링크에서 API를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="51ba7-118">예제 5: Open Api Link에서 ApiVersion 집합으로 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="51ba7-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

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

<span data-ttu-id="51ba7-119">이 명령은 지정된 Open 3.0 사양 문서에서 API를 가져오고 새 ApiVersion을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="51ba7-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51ba7-120">PARAMETERS</span></span>

### <span data-ttu-id="51ba7-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="51ba7-121">-ApiId</span></span>
<span data-ttu-id="51ba7-122">가져올 API에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="51ba7-123">이 매개 변수를 지정하지 않으면 ID가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="51ba7-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="51ba7-124">-ApiRevision</span></span>
<span data-ttu-id="51ba7-125">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-125">Identifier of API Revision.</span></span> <span data-ttu-id="51ba7-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-126">This parameter is optional.</span></span> <span data-ttu-id="51ba7-127">지정하지 않으면 가져오기가 현재 활성 개정 또는 새 API로 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="51ba7-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="51ba7-128">-ApiType</span></span>
<span data-ttu-id="51ba7-129">이 매개 변수는 Http의 기본값을 사용하는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="51ba7-130">Soap 옵션은 WSDL을 가져올 때만 적용될 수 있으며 SOAP Passthrough API를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="51ba7-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="51ba7-131">-ApiVersion</span></span>
<span data-ttu-id="51ba7-132">만들 Api의 Api 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-132">Api Version of the Api to create.</span></span> <span data-ttu-id="51ba7-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="51ba7-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="51ba7-134">-ApiVersionSetId</span></span>
<span data-ttu-id="51ba7-135">관련 Api 버전 집합에 대한 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="51ba7-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="51ba7-137">-Context</span><span class="sxs-lookup"><span data-stu-id="51ba7-137">-Context</span></span>
<span data-ttu-id="51ba7-138">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="51ba7-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="51ba7-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ba7-139">-DefaultProfile</span></span>
<span data-ttu-id="51ba7-140">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ba7-141">-Path</span><span class="sxs-lookup"><span data-stu-id="51ba7-141">-Path</span></span>
<span data-ttu-id="51ba7-142">API의 공용 URL의 마지막 부분으로 웹 API 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="51ba7-143">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="51ba7-144">1~400자 이상이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="51ba7-145">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="51ba7-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="51ba7-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="51ba7-146">-Protocol</span></span>
<span data-ttu-id="51ba7-147">웹 API 프로토콜(http, https)입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-147">Web API protocols (http, https).</span></span> <span data-ttu-id="51ba7-148">사용할 수 있는 API를 사용하는 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-148">Protocols over which API is made available.</span></span> <span data-ttu-id="51ba7-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-149">This parameter is optional.</span></span> <span data-ttu-id="51ba7-150">제공된 경우 사양 문서에 지정된 프로토콜을 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="51ba7-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="51ba7-151">-ServiceUrl</span></span>
<span data-ttu-id="51ba7-152">API를 노출하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="51ba7-153">이 URL은 Azure API Management에서만 사용하며 공개되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="51ba7-154">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-154">This parameter is optional.</span></span> <span data-ttu-id="51ba7-155">제공된 경우 사양 문서에 지정된 ServiceUrl을 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="51ba7-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="51ba7-156">-SpecificationFormat</span></span>
<span data-ttu-id="51ba7-157">사양 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-157">Specifies the specification format.</span></span>
<span data-ttu-id="51ba7-158">psdx_paramvalues Wadl, Wsdl 및 Swagger를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="51ba7-159">-사양 경로</span><span class="sxs-lookup"><span data-stu-id="51ba7-159">-SpecificationPath</span></span>
<span data-ttu-id="51ba7-160">사양 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-160">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="51ba7-161">-사양Url</span><span class="sxs-lookup"><span data-stu-id="51ba7-161">-SpecificationUrl</span></span>
<span data-ttu-id="51ba7-162">사양 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-162">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="51ba7-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="51ba7-163">-WsdlEndpointName</span></span>
<span data-ttu-id="51ba7-164">가져올 WSDL 엔드포인트(포트)의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="51ba7-165">1~400자 이상이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="51ba7-166">이 매개 변수는 선택 사항이며 Wsdl을 가져오는 데만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="51ba7-167">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="51ba7-167">Default value is $null.</span></span>

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

### <span data-ttu-id="51ba7-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="51ba7-168">-WsdlServiceName</span></span>
<span data-ttu-id="51ba7-169">가져올 WSDL 서비스의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="51ba7-170">1~400자 이상이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="51ba7-171">이 매개 변수는 선택 사항이며 Wsdl 을 가져오는 데만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="51ba7-172">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="51ba7-172">Default value is $null.</span></span>

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

### <span data-ttu-id="51ba7-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ba7-173">CommonParameters</span></span>
<span data-ttu-id="51ba7-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51ba7-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ba7-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51ba7-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ba7-176">입력</span><span class="sxs-lookup"><span data-stu-id="51ba7-176">INPUTS</span></span>

### <span data-ttu-id="51ba7-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="51ba7-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="51ba7-178">System.String</span><span class="sxs-lookup"><span data-stu-id="51ba7-178">System.String</span></span>

### <span data-ttu-id="51ba7-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="51ba7-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="51ba7-180">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="51ba7-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51ba7-181">출력</span><span class="sxs-lookup"><span data-stu-id="51ba7-181">OUTPUTS</span></span>

### <span data-ttu-id="51ba7-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="51ba7-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51ba7-183">NOTES</span></span>

## <span data-ttu-id="51ba7-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51ba7-184">RELATED LINKS</span></span>

[<span data-ttu-id="51ba7-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="51ba7-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="51ba7-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="51ba7-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="51ba7-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="51ba7-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


