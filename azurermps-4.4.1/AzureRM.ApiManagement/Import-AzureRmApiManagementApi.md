---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531285"
---
# <span data-ttu-id="42d82-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="42d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d82-102">SYNOPSIS</span></span>
<span data-ttu-id="42d82-103">파일 또는 URL에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42d82-104">SYNTAX</span></span>

### <span data-ttu-id="42d82-105">로컬 파일에서 (기본값)</span><span class="sxs-lookup"><span data-stu-id="42d82-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d82-106">URL에서</span><span class="sxs-lookup"><span data-stu-id="42d82-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d82-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42d82-107">DESCRIPTION</span></span>
<span data-ttu-id="42d82-108">**AzureRmApiManagementApi** cmdlet은 파일 또는 URL에서 Azure API Management api를 가져옵니다 (웹 응용 프로그램 설명 언어 (WADL), WSDL (웹 서비스 설명 언어) 또는 Swagger 형식).</span><span class="sxs-lookup"><span data-stu-id="42d82-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="42d82-109">예제의</span><span class="sxs-lookup"><span data-stu-id="42d82-109">EXAMPLES</span></span>

### <span data-ttu-id="42d82-110">예제 1 WADL 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="42d82-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="42d82-111">이 명령은 지정 된 WADL 파일에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="42d82-112">예제 2 Swagger 파일에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="42d82-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="42d82-113">이 명령은 지정 된 Swagger 파일에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="42d82-114">예제 3: WADL 링크에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="42d82-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="42d82-115">이 명령은 지정 된 WADL 링크에서 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="42d82-116">변수</span><span class="sxs-lookup"><span data-stu-id="42d82-116">PARAMETERS</span></span>

### <span data-ttu-id="42d82-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="42d82-117">-ApiId</span></span>
<span data-ttu-id="42d82-118">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="42d82-119">이 매개 변수를 지정 하지 않으면 ID가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="42d82-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="42d82-120">-ApiType</span></span>
<span data-ttu-id="42d82-121">이 매개 변수는 기본값 Http 값으로 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="42d82-122">Soap 옵션은 WSDL을 가져오는 경우에만 적용 되며 SOAP 통과 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="42d82-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="42d82-123">-Context</span></span>
<span data-ttu-id="42d82-124">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-124">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d82-125">-Path</span><span class="sxs-lookup"><span data-stu-id="42d82-125">-Path</span></span>
<span data-ttu-id="42d82-126">웹 API 경로를 API 공용 URL의 마지막 부분으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="42d82-127">이 URL은 웹 서비스로 요청을 보내기 위해 API 소비자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="42d82-128">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="42d82-129">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="42d82-130">-사양 형식</span><span class="sxs-lookup"><span data-stu-id="42d82-130">-SpecificationFormat</span></span>
<span data-ttu-id="42d82-131">사양 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-131">Specifies the specification format.</span></span>
<span data-ttu-id="42d82-132">psdx_paramvalues Wadl, Wsdl 및 Swagger.</span><span class="sxs-lookup"><span data-stu-id="42d82-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d82-133">-사양 경로</span><span class="sxs-lookup"><span data-stu-id="42d82-133">-SpecificationPath</span></span>
<span data-ttu-id="42d82-134">사양 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d82-135">-사양 Url</span><span class="sxs-lookup"><span data-stu-id="42d82-135">-SpecificationUrl</span></span>
<span data-ttu-id="42d82-136">사양 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d82-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="42d82-137">-WsdlEndpointName</span></span>
<span data-ttu-id="42d82-138">가져올 WSDL 끝점 (포트)의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="42d82-139">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="42d82-140">이 매개 변수는 선택적 이며 Wsdl을 가져오는 데만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="42d82-141">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-141">Default value is $null.</span></span>

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

### <span data-ttu-id="42d82-142">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="42d82-142">-WsdlServiceName</span></span>
<span data-ttu-id="42d82-143">가져올 WSDL 서비스의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="42d82-144">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="42d82-145">이 매개 변수는 선택적 이며 Wsdl을 가져오는 데만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="42d82-146">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-146">Default value is $null.</span></span>

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

### <span data-ttu-id="42d82-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d82-147">-DefaultProfile</span></span>
<span data-ttu-id="42d82-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d82-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d82-149">CommonParameters</span></span>
<span data-ttu-id="42d82-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d82-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d82-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d82-152">입력</span><span class="sxs-lookup"><span data-stu-id="42d82-152">INPUTS</span></span>

## <span data-ttu-id="42d82-153">출력</span><span class="sxs-lookup"><span data-stu-id="42d82-153">OUTPUTS</span></span>

### <span data-ttu-id="42d82-154">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="42d82-155">이 cmdlet은 가져온 API를 **PsApiManagementApi** 개체로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42d82-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="42d82-156">상속자</span><span class="sxs-lookup"><span data-stu-id="42d82-156">NOTES</span></span>

## <span data-ttu-id="42d82-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42d82-157">RELATED LINKS</span></span>

[<span data-ttu-id="42d82-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="42d82-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="42d82-160">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="42d82-161">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="42d82-162">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42d82-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


