---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533460"
---
# <span data-ttu-id="db636-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="db636-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="db636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db636-102">SYNOPSIS</span></span>
<span data-ttu-id="db636-103">API 수정 버전 수정</span><span class="sxs-lookup"><span data-stu-id="db636-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db636-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db636-104">SYNTAX</span></span>

### <span data-ttu-id="db636-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="db636-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db636-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db636-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db636-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db636-107">DESCRIPTION</span></span>
<span data-ttu-id="db636-108">**AzureRmApiManagementApiRevision** Cmdlet은 Azure API Management api 수정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="db636-109">예제의</span><span class="sxs-lookup"><span data-stu-id="db636-109">EXAMPLES</span></span>

### <span data-ttu-id="db636-110">예제 1 API 수정 수정</span><span class="sxs-lookup"><span data-stu-id="db636-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="db636-111">Cmdlet은 `2` `echo-api` 새 설명, 프로토콜 및 경로를 사용 하 여 API의 수정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="db636-112">변수</span><span class="sxs-lookup"><span data-stu-id="db636-112">PARAMETERS</span></span>

### <span data-ttu-id="db636-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="db636-113">-ApiId</span></span>
<span data-ttu-id="db636-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-114">Identifier of existing API.</span></span>
<span data-ttu-id="db636-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-115">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="db636-116">-ApiRevision</span></span>
<span data-ttu-id="db636-117">기존 API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="db636-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-118">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="db636-119">-AuthorizationScope</span></span>
<span data-ttu-id="db636-120">OAuth 작업 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-120">OAuth operations scope.</span></span>
<span data-ttu-id="db636-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-121">This parameter is optional.</span></span>
<span data-ttu-id="db636-122">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-122">Default value is $null.</span></span>

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

### <span data-ttu-id="db636-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="db636-123">-AuthorizationServerId</span></span>
<span data-ttu-id="db636-124">OAuth 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="db636-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-125">This parameter is optional.</span></span>
<span data-ttu-id="db636-126">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-126">Default value is $null.</span></span>
<span data-ttu-id="db636-127">AuthorizationScope가 지정 된 경우이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="db636-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="db636-128">-Context</span></span>
<span data-ttu-id="db636-129">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db636-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-130">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db636-131">-DefaultProfile</span></span>
<span data-ttu-id="db636-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db636-133">-설명</span><span class="sxs-lookup"><span data-stu-id="db636-133">-Description</span></span>
<span data-ttu-id="db636-134">웹 API 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-134">Web API description.</span></span>
<span data-ttu-id="db636-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="db636-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db636-136">-InputObject</span></span>
<span data-ttu-id="db636-137">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="db636-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-138">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-139">-이름</span><span class="sxs-lookup"><span data-stu-id="db636-139">-Name</span></span>
<span data-ttu-id="db636-140">웹 API 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-140">Web API name.</span></span>
<span data-ttu-id="db636-141">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="db636-142">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-142">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db636-143">-PassThru</span></span>
<span data-ttu-id="db636-144">지정한 경우, set API를 나타내는 ApiManagement의 인스턴스를 PsApiManagementApi 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="db636-145">-Path</span><span class="sxs-lookup"><span data-stu-id="db636-145">-Path</span></span>
<span data-ttu-id="db636-146">웹 API 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-146">Web API Path.</span></span>
<span data-ttu-id="db636-147">API 공용 URL의 마지막 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="db636-148">이 URL은 웹 서비스에 대 한 요청을 보내기 위해 API 소비자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="db636-149">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="db636-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-150">This parameter is optional.</span></span>
<span data-ttu-id="db636-151">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-151">Default value is $null.</span></span>

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

### <span data-ttu-id="db636-152">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="db636-152">-Protocols</span></span>
<span data-ttu-id="db636-153">웹 API 프로토콜 (http, https).</span><span class="sxs-lookup"><span data-stu-id="db636-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="db636-154">사용할 수 있는 API에 대 한 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="db636-155">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-155">This parameter is required.</span></span>
<span data-ttu-id="db636-156">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-156">Default value is $null.</span></span>

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

### <span data-ttu-id="db636-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="db636-157">-ServiceUrl</span></span>
<span data-ttu-id="db636-158">API를 노출 하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="db636-159">이 URL은 Azure API Management에만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db636-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="db636-160">1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="db636-161">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-161">This parameter is required.</span></span>

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

### <span data-ttu-id="db636-162">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="db636-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="db636-163">구독 키 헤더 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-163">Subscription key header name.</span></span>
<span data-ttu-id="db636-164">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-164">This parameter is optional.</span></span>
<span data-ttu-id="db636-165">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-165">Default value is $null.</span></span>

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

### <span data-ttu-id="db636-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="db636-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="db636-167">구독 키 쿼리 문자열 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="db636-168">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-168">This parameter is optional.</span></span>
<span data-ttu-id="db636-169">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="db636-169">Default value is $null.</span></span>

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

### <span data-ttu-id="db636-170">-확인</span><span class="sxs-lookup"><span data-stu-id="db636-170">-Confirm</span></span>
<span data-ttu-id="db636-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db636-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db636-172">-WhatIf</span></span>
<span data-ttu-id="db636-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db636-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db636-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db636-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db636-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db636-175">CommonParameters</span></span>
<span data-ttu-id="db636-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db636-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db636-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db636-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db636-178">입력</span><span class="sxs-lookup"><span data-stu-id="db636-178">INPUTS</span></span>

### <span data-ttu-id="db636-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db636-179">System.String</span></span>

### <span data-ttu-id="db636-180">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db636-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db636-181">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="db636-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="db636-182">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db636-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="db636-183">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="db636-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="db636-184">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="db636-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db636-185">출력</span><span class="sxs-lookup"><span data-stu-id="db636-185">OUTPUTS</span></span>

### <span data-ttu-id="db636-186">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="db636-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="db636-187">상속자</span><span class="sxs-lookup"><span data-stu-id="db636-187">NOTES</span></span>

## <span data-ttu-id="db636-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db636-188">RELATED LINKS</span></span>

[<span data-ttu-id="db636-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="db636-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="db636-190">새로운 AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="db636-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="db636-191">제거-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="db636-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
