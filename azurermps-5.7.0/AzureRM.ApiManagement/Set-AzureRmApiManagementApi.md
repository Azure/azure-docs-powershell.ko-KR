---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531790"
---
# <span data-ttu-id="2817b-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2817b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2817b-102">SYNOPSIS</span></span>
<span data-ttu-id="2817b-103">API를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2817b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2817b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2817b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2817b-105">DESCRIPTION</span></span>
<span data-ttu-id="2817b-106">**AzureRmApiManagementApi** Cmdlet은 Azure API Management api를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2817b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2817b-107">EXAMPLES</span></span>

### <span data-ttu-id="2817b-108">예제 1 API 수정</span><span class="sxs-lookup"><span data-stu-id="2817b-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="2817b-109">변수</span><span class="sxs-lookup"><span data-stu-id="2817b-109">PARAMETERS</span></span>

### <span data-ttu-id="2817b-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2817b-110">-ApiId</span></span>
<span data-ttu-id="2817b-111">수정할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2817b-112">-AuthorizationScope</span></span>
<span data-ttu-id="2817b-113">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2817b-114">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2817b-115">-AuthorizationServerId</span></span>
<span data-ttu-id="2817b-116">OAuth 권한 부여 서버 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2817b-117">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-117">The default value is $Null.</span></span>
<span data-ttu-id="2817b-118">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2817b-119">-Context</span></span>
<span data-ttu-id="2817b-120">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2817b-121">-DefaultProfile</span></span>
<span data-ttu-id="2817b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-123">-설명</span><span class="sxs-lookup"><span data-stu-id="2817b-123">-Description</span></span>
<span data-ttu-id="2817b-124">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2817b-125">-Name</span></span>
<span data-ttu-id="2817b-126">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2817b-127">-PassThru</span></span>
<span data-ttu-id="2817b-128">passthru</span><span class="sxs-lookup"><span data-stu-id="2817b-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="2817b-129">-Path</span></span>
<span data-ttu-id="2817b-130">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2817b-131">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2817b-132">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="2817b-133">-Protocols</span></span>
<span data-ttu-id="2817b-134">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2817b-135">http 및 https를 psdx_paramvalues 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2817b-136">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2817b-137">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2817b-138">-ServiceUrl</span></span>
<span data-ttu-id="2817b-139">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2817b-140">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2817b-141">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-142">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="2817b-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2817b-143">구독 키 헤더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2817b-144">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2817b-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2817b-146">구독 키 쿼리 문자열 매개 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2817b-147">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2817b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2817b-148">CommonParameters</span></span>
<span data-ttu-id="2817b-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2817b-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2817b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2817b-151">입력</span><span class="sxs-lookup"><span data-stu-id="2817b-151">INPUTS</span></span>

### <span data-ttu-id="2817b-152">않아야</span><span class="sxs-lookup"><span data-stu-id="2817b-152">None</span></span>
<span data-ttu-id="2817b-153">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2817b-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2817b-154">출력</span><span class="sxs-lookup"><span data-stu-id="2817b-154">OUTPUTS</span></span>

### <span data-ttu-id="2817b-155">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2817b-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2817b-156">NOTES</span></span>

## <span data-ttu-id="2817b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2817b-157">RELATED LINKS</span></span>

[<span data-ttu-id="2817b-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2817b-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2817b-160">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2817b-161">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2817b-162">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2817b-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


