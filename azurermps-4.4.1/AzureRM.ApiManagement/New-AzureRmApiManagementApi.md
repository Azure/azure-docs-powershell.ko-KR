---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531282"
---
# <span data-ttu-id="5b825-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="5b825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b825-102">SYNOPSIS</span></span>
<span data-ttu-id="5b825-103">API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b825-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b825-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b825-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b825-105">DESCRIPTION</span></span>
<span data-ttu-id="5b825-106">**AzureRmApiManagementApi** Cmdlet은 Azure API Management api를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="5b825-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b825-107">EXAMPLES</span></span>

### <span data-ttu-id="5b825-108">예제 1: API 만들기</span><span class="sxs-lookup"><span data-stu-id="5b825-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="5b825-109">이 명령은 지정 된 URL을 사용 하 여 EchoApi 라는 API를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="5b825-110">변수</span><span class="sxs-lookup"><span data-stu-id="5b825-110">PARAMETERS</span></span>

### <span data-ttu-id="5b825-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5b825-111">-ApiId</span></span>
<span data-ttu-id="5b825-112">만들 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="5b825-113">이 매개 변수를 지정 하지 않으면이 cmdlet이 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="5b825-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5b825-114">-AuthorizationScope</span></span>
<span data-ttu-id="5b825-115">OAuth 작업 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="5b825-116">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="5b825-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5b825-117">-AuthorizationServerId</span></span>
<span data-ttu-id="5b825-118">OAuth 권한 부여 서버 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="5b825-119">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-119">The default value is $Null.</span></span>
<span data-ttu-id="5b825-120">*Authorizationscope* 가 지정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="5b825-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5b825-121">-Context</span></span>
<span data-ttu-id="5b825-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5b825-123">-설명</span><span class="sxs-lookup"><span data-stu-id="5b825-123">-Description</span></span>
<span data-ttu-id="5b825-124">웹 API에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="5b825-125">-이름</span><span class="sxs-lookup"><span data-stu-id="5b825-125">-Name</span></span>
<span data-ttu-id="5b825-126">웹 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="5b825-127">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="5b825-128">-Path</span><span class="sxs-lookup"><span data-stu-id="5b825-128">-Path</span></span>
<span data-ttu-id="5b825-129">API 공용 URL의 마지막 부분인 웹 API 경로를 지정 하 고 관리 포털의 웹 API URL 접미사 필드에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="5b825-130">이 URL은 API 소비자가 웹 서비스에 요청을 보내는 데 사용 되며 1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="5b825-131">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="5b825-132">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="5b825-132">-ProductIds</span></span>
<span data-ttu-id="5b825-133">새 API를 추가할 제품 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-133">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="5b825-134">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5b825-134">-Protocols</span></span>
<span data-ttu-id="5b825-135">웹 API 프로토콜의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="5b825-136">유효한 값은 http, https입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-136">Valid values are http, https.</span></span>
<span data-ttu-id="5b825-137">API를 사용할 수 있게 되는 웹 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="5b825-138">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="5b825-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5b825-139">-ServiceUrl</span></span>
<span data-ttu-id="5b825-140">API를 노출 하는 웹 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="5b825-141">이 URL은 Azure API Management 에서만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="5b825-142">URL은 1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="5b825-143">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="5b825-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5b825-144">구독 키 헤더 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="5b825-145">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="5b825-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5b825-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5b825-147">구독 키 쿼리 문자열 매개 변수 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="5b825-148">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="5b825-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b825-149">-DefaultProfile</span></span>
<span data-ttu-id="5b825-150">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b825-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b825-151">CommonParameters</span></span>
<span data-ttu-id="5b825-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b825-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b825-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b825-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b825-154">입력</span><span class="sxs-lookup"><span data-stu-id="5b825-154">INPUTS</span></span>

## <span data-ttu-id="5b825-155">출력</span><span class="sxs-lookup"><span data-stu-id="5b825-155">OUTPUTS</span></span>

### <span data-ttu-id="5b825-156">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5b825-157">상속자</span><span class="sxs-lookup"><span data-stu-id="5b825-157">NOTES</span></span>

## <span data-ttu-id="5b825-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b825-158">RELATED LINKS</span></span>

[<span data-ttu-id="5b825-159">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="5b825-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="5b825-161">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="5b825-162">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="5b825-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5b825-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


