---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869366"
---
# <span data-ttu-id="7720d-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7720d-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="7720d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7720d-102">SYNOPSIS</span></span>
<span data-ttu-id="7720d-103">API 수정 버전 수정</span><span class="sxs-lookup"><span data-stu-id="7720d-103">Modifies an API Revision</span></span>

## <span data-ttu-id="7720d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7720d-104">SYNTAX</span></span>

### <span data-ttu-id="7720d-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7720d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7720d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7720d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7720d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7720d-107">DESCRIPTION</span></span>
<span data-ttu-id="7720d-108">**AzApiManagementApiRevision** Cmdlet은 Azure API Management api 수정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="7720d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7720d-109">EXAMPLES</span></span>

### <span data-ttu-id="7720d-110">예제 1 API 수정 수정</span><span class="sxs-lookup"><span data-stu-id="7720d-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="7720d-111">Cmdlet은 `2` `echo-api` 새 설명, 프로토콜 및 경로를 사용 하 여 API의 수정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="7720d-112">변수</span><span class="sxs-lookup"><span data-stu-id="7720d-112">PARAMETERS</span></span>

### <span data-ttu-id="7720d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7720d-113">-ApiId</span></span>
<span data-ttu-id="7720d-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-114">Identifier of existing API.</span></span>
<span data-ttu-id="7720d-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7720d-116">-ApiRevision</span></span>
<span data-ttu-id="7720d-117">기존 API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="7720d-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="7720d-119">-AuthorizationScope</span></span>
<span data-ttu-id="7720d-120">OAuth 작업 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-120">OAuth operations scope.</span></span>
<span data-ttu-id="7720d-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-121">This parameter is optional.</span></span>
<span data-ttu-id="7720d-122">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-122">Default value is $null.</span></span>

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

### <span data-ttu-id="7720d-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="7720d-123">-AuthorizationServerId</span></span>
<span data-ttu-id="7720d-124">OAuth 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="7720d-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-125">This parameter is optional.</span></span>
<span data-ttu-id="7720d-126">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-126">Default value is $null.</span></span>
<span data-ttu-id="7720d-127">AuthorizationScope가 지정 된 경우이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="7720d-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7720d-128">-Context</span></span>
<span data-ttu-id="7720d-129">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7720d-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-130">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7720d-131">-DefaultProfile</span></span>
<span data-ttu-id="7720d-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7720d-133">-설명</span><span class="sxs-lookup"><span data-stu-id="7720d-133">-Description</span></span>
<span data-ttu-id="7720d-134">웹 API 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-134">Web API description.</span></span>
<span data-ttu-id="7720d-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="7720d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7720d-136">-InputObject</span></span>
<span data-ttu-id="7720d-137">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="7720d-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-138">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-139">-이름</span><span class="sxs-lookup"><span data-stu-id="7720d-139">-Name</span></span>
<span data-ttu-id="7720d-140">웹 API 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-140">Web API name.</span></span>
<span data-ttu-id="7720d-141">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="7720d-142">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-142">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7720d-143">-PassThru</span></span>
<span data-ttu-id="7720d-144">지정한 경우, set API를 나타내는 ApiManagement의 인스턴스를 PsApiManagementApi 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="7720d-145">-Path</span><span class="sxs-lookup"><span data-stu-id="7720d-145">-Path</span></span>
<span data-ttu-id="7720d-146">웹 API 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-146">Web API Path.</span></span>
<span data-ttu-id="7720d-147">API 공용 URL의 마지막 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="7720d-148">이 URL은 웹 서비스에 대 한 요청을 보내기 위해 API 소비자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="7720d-149">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="7720d-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-150">This parameter is optional.</span></span>
<span data-ttu-id="7720d-151">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-151">Default value is $null.</span></span>

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

### <span data-ttu-id="7720d-152">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7720d-152">-Protocols</span></span>
<span data-ttu-id="7720d-153">웹 API 프로토콜 (http, https).</span><span class="sxs-lookup"><span data-stu-id="7720d-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="7720d-154">사용할 수 있는 API에 대 한 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="7720d-155">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-155">This parameter is required.</span></span>
<span data-ttu-id="7720d-156">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-156">Default value is $null.</span></span>

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

### <span data-ttu-id="7720d-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7720d-157">-ServiceUrl</span></span>
<span data-ttu-id="7720d-158">API를 노출 하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="7720d-159">이 URL은 Azure API Management에만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="7720d-160">1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="7720d-161">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-161">This parameter is required.</span></span>

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

### <span data-ttu-id="7720d-162">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="7720d-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="7720d-163">구독 키 헤더 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-163">Subscription key header name.</span></span>
<span data-ttu-id="7720d-164">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-164">This parameter is optional.</span></span>
<span data-ttu-id="7720d-165">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-165">Default value is $null.</span></span>

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

### <span data-ttu-id="7720d-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="7720d-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="7720d-167">구독 키 쿼리 문자열 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="7720d-168">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-168">This parameter is optional.</span></span>
<span data-ttu-id="7720d-169">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-169">Default value is $null.</span></span>

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

### <span data-ttu-id="7720d-170">-확인</span><span class="sxs-lookup"><span data-stu-id="7720d-170">-Confirm</span></span>
<span data-ttu-id="7720d-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7720d-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7720d-172">-WhatIf</span></span>
<span data-ttu-id="7720d-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7720d-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7720d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7720d-175">CommonParameters</span></span>
<span data-ttu-id="7720d-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7720d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7720d-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7720d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7720d-178">입력</span><span class="sxs-lookup"><span data-stu-id="7720d-178">INPUTS</span></span>

### <span data-ttu-id="7720d-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7720d-179">System.String</span></span>

### <span data-ttu-id="7720d-180">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7720d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7720d-181">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7720d-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="7720d-182">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="7720d-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="7720d-183">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7720d-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7720d-184">출력</span><span class="sxs-lookup"><span data-stu-id="7720d-184">OUTPUTS</span></span>

### <span data-ttu-id="7720d-185">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7720d-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7720d-186">상속자</span><span class="sxs-lookup"><span data-stu-id="7720d-186">NOTES</span></span>

## <span data-ttu-id="7720d-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7720d-187">RELATED LINKS</span></span>

[<span data-ttu-id="7720d-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7720d-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="7720d-189">새로운 AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7720d-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="7720d-190">제거-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7720d-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)