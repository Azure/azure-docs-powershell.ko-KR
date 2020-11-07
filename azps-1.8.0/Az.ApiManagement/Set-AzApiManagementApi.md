---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869377"
---
# <span data-ttu-id="07bcf-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="07bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="07bcf-103">API를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-103">Modifies an API.</span></span>

## <span data-ttu-id="07bcf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07bcf-104">SYNTAX</span></span>

### <span data-ttu-id="07bcf-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="07bcf-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07bcf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07bcf-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07bcf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="07bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="07bcf-108">**AzApiManagementApi** Cmdlet은 Azure API Management api를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="07bcf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="07bcf-109">EXAMPLES</span></span>

### <span data-ttu-id="07bcf-110">예제 1 API 수정</span><span class="sxs-lookup"><span data-stu-id="07bcf-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="07bcf-111">변수</span><span class="sxs-lookup"><span data-stu-id="07bcf-111">PARAMETERS</span></span>

### <span data-ttu-id="07bcf-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="07bcf-112">-ApiId</span></span>
<span data-ttu-id="07bcf-113">수정할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="07bcf-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="07bcf-114">-AuthorizationScope</span></span>
<span data-ttu-id="07bcf-115">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="07bcf-116">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="07bcf-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="07bcf-117">-AuthorizationServerId</span></span>
<span data-ttu-id="07bcf-118">OAuth 권한 부여 서버 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="07bcf-119">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-119">The default value is $Null.</span></span>
<span data-ttu-id="07bcf-120">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="07bcf-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="07bcf-121">-Context</span></span>
<span data-ttu-id="07bcf-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="07bcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bcf-123">-DefaultProfile</span></span>
<span data-ttu-id="07bcf-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bcf-125">-설명</span><span class="sxs-lookup"><span data-stu-id="07bcf-125">-Description</span></span>
<span data-ttu-id="07bcf-126">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="07bcf-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07bcf-127">-InputObject</span></span>
<span data-ttu-id="07bcf-128">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="07bcf-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-129">This parameter is required.</span></span>

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

### <span data-ttu-id="07bcf-130">-이름</span><span class="sxs-lookup"><span data-stu-id="07bcf-130">-Name</span></span>
<span data-ttu-id="07bcf-131">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="07bcf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07bcf-132">-PassThru</span></span>
<span data-ttu-id="07bcf-133">passthru</span><span class="sxs-lookup"><span data-stu-id="07bcf-133">passthru</span></span>

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

### <span data-ttu-id="07bcf-134">-Path</span><span class="sxs-lookup"><span data-stu-id="07bcf-134">-Path</span></span>
<span data-ttu-id="07bcf-135">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="07bcf-136">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="07bcf-137">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="07bcf-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="07bcf-138">-Protocols</span></span>
<span data-ttu-id="07bcf-139">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="07bcf-140">http 및 https를 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="07bcf-141">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="07bcf-142">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="07bcf-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="07bcf-143">-ServiceUrl</span></span>
<span data-ttu-id="07bcf-144">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="07bcf-145">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="07bcf-146">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="07bcf-147">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="07bcf-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="07bcf-148">구독 키 헤더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="07bcf-149">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="07bcf-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="07bcf-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="07bcf-151">구독 키 쿼리 문자열 매개 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="07bcf-152">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="07bcf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bcf-153">CommonParameters</span></span>
<span data-ttu-id="07bcf-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bcf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bcf-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bcf-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bcf-156">입력</span><span class="sxs-lookup"><span data-stu-id="07bcf-156">INPUTS</span></span>

### <span data-ttu-id="07bcf-157">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07bcf-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07bcf-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07bcf-158">System.String</span></span>

### <span data-ttu-id="07bcf-159">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="07bcf-160">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="07bcf-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="07bcf-161">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="07bcf-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07bcf-162">출력</span><span class="sxs-lookup"><span data-stu-id="07bcf-162">OUTPUTS</span></span>

### <span data-ttu-id="07bcf-163">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="07bcf-164">상속자</span><span class="sxs-lookup"><span data-stu-id="07bcf-164">NOTES</span></span>

## <span data-ttu-id="07bcf-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07bcf-165">RELATED LINKS</span></span>

[<span data-ttu-id="07bcf-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="07bcf-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="07bcf-168">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="07bcf-169">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="07bcf-170">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07bcf-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


