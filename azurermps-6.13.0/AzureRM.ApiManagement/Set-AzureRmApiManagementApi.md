---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533463"
---
# <span data-ttu-id="0c397-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="0c397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c397-102">SYNOPSIS</span></span>
<span data-ttu-id="0c397-103">API를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c397-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c397-104">SYNTAX</span></span>

### <span data-ttu-id="0c397-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c397-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c397-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c397-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c397-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0c397-107">DESCRIPTION</span></span>
<span data-ttu-id="0c397-108">**AzureRmApiManagementApi** Cmdlet은 Azure API Management api를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="0c397-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c397-109">EXAMPLES</span></span>

### <span data-ttu-id="0c397-110">예제 1 API 수정</span><span class="sxs-lookup"><span data-stu-id="0c397-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="0c397-111">변수</span><span class="sxs-lookup"><span data-stu-id="0c397-111">PARAMETERS</span></span>

### <span data-ttu-id="0c397-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0c397-112">-ApiId</span></span>
<span data-ttu-id="0c397-113">수정할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="0c397-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="0c397-114">-AuthorizationScope</span></span>
<span data-ttu-id="0c397-115">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="0c397-116">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="0c397-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="0c397-117">-AuthorizationServerId</span></span>
<span data-ttu-id="0c397-118">OAuth 권한 부여 서버 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="0c397-119">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-119">The default value is $Null.</span></span>
<span data-ttu-id="0c397-120">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="0c397-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0c397-121">-Context</span></span>
<span data-ttu-id="0c397-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c397-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c397-123">-DefaultProfile</span></span>
<span data-ttu-id="0c397-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c397-125">-설명</span><span class="sxs-lookup"><span data-stu-id="0c397-125">-Description</span></span>
<span data-ttu-id="0c397-126">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="0c397-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c397-127">-InputObject</span></span>
<span data-ttu-id="0c397-128">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="0c397-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-129">This parameter is required.</span></span>

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

### <span data-ttu-id="0c397-130">-이름</span><span class="sxs-lookup"><span data-stu-id="0c397-130">-Name</span></span>
<span data-ttu-id="0c397-131">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="0c397-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c397-132">-PassThru</span></span>
<span data-ttu-id="0c397-133">passthru</span><span class="sxs-lookup"><span data-stu-id="0c397-133">passthru</span></span>

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

### <span data-ttu-id="0c397-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0c397-134">-Path</span></span>
<span data-ttu-id="0c397-135">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="0c397-136">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="0c397-137">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="0c397-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="0c397-138">-Protocols</span></span>
<span data-ttu-id="0c397-139">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="0c397-140">http 및 https를 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="0c397-141">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="0c397-142">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="0c397-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0c397-143">-ServiceUrl</span></span>
<span data-ttu-id="0c397-144">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="0c397-145">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="0c397-146">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="0c397-147">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="0c397-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="0c397-148">구독 키 헤더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="0c397-149">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="0c397-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="0c397-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="0c397-151">구독 키 쿼리 문자열 매개 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="0c397-152">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="0c397-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c397-153">CommonParameters</span></span>
<span data-ttu-id="0c397-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c397-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c397-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c397-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c397-156">입력</span><span class="sxs-lookup"><span data-stu-id="0c397-156">INPUTS</span></span>

### <span data-ttu-id="0c397-157">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c397-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c397-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c397-158">System.String</span></span>

### <span data-ttu-id="0c397-159">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="0c397-160">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c397-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0c397-161">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="0c397-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="0c397-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c397-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c397-163">출력</span><span class="sxs-lookup"><span data-stu-id="0c397-163">OUTPUTS</span></span>

### <span data-ttu-id="0c397-164">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0c397-165">상속자</span><span class="sxs-lookup"><span data-stu-id="0c397-165">NOTES</span></span>

## <span data-ttu-id="0c397-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c397-166">RELATED LINKS</span></span>

[<span data-ttu-id="0c397-167">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c397-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c397-169">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c397-170">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c397-171">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c397-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


