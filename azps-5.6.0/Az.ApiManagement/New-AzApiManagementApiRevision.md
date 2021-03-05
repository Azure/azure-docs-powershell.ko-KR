---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: d03253a608469ac111d04b837497375028b48fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009408"
---
# <span data-ttu-id="4a2b5-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4a2b5-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="4a2b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2b5-103">기존 API의 새 개정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="4a2b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a2b5-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a2b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a2b5-105">DESCRIPTION</span></span>

<span data-ttu-id="4a2b5-106">**New-AzApiManagementApiRevision** cmdlet은 API Management 컨텍스트에서 기존 API에 대한 API 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="4a2b5-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a2b5-107">EXAMPLES</span></span>

### <span data-ttu-id="4a2b5-108">예제 1: API에 대한 빈 API 개정 만들기</span><span class="sxs-lookup"><span data-stu-id="4a2b5-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="4a2b5-109">이 명령은 API의 API `2` 개정을 `echo-api` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="4a2b5-110">예제 2: 기존 Api에서 API 수정을 만들고 모든 작업, 태그 및 정책을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="4a2b5-111">이 명령은 API의 API `5` 개정을 `echo-api` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="4a2b5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a2b5-112">PARAMETERS</span></span>

### <span data-ttu-id="4a2b5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4a2b5-113">-ApiId</span></span>
<span data-ttu-id="4a2b5-114">개정을 만들 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="4a2b5-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4a2b5-115">-ApiRevision</span></span>
<span data-ttu-id="4a2b5-116">Api의 개정 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="4a2b5-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="4a2b5-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="4a2b5-118">Api 개정 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-118">Api Revision Description.</span></span> <span data-ttu-id="4a2b5-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a2b5-120">-Context</span><span class="sxs-lookup"><span data-stu-id="4a2b5-120">-Context</span></span>
<span data-ttu-id="4a2b5-121">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4a2b5-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2b5-123">-DefaultProfile</span></span>
<span data-ttu-id="4a2b5-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a2b5-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4a2b5-125">-ServiceUrl</span></span>
<span data-ttu-id="4a2b5-126">백end 서비스에 API를 노출하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="4a2b5-127">이 URL은 Azure API Management에서만 사용하며 공개되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="4a2b5-128">1~2000자 이상이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="4a2b5-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-129">This parameter is required.</span></span>

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

### <span data-ttu-id="4a2b5-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="4a2b5-130">-SourceApiRevision</span></span>
<span data-ttu-id="4a2b5-131">원본 API의 Api 개정 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="4a2b5-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a2b5-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4a2b5-133">-Confirm</span></span>
<span data-ttu-id="4a2b5-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a2b5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a2b5-135">-WhatIf</span></span>
<span data-ttu-id="4a2b5-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a2b5-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a2b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2b5-138">CommonParameters</span></span>
<span data-ttu-id="4a2b5-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a2b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2b5-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a2b5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2b5-141">입력</span><span class="sxs-lookup"><span data-stu-id="4a2b5-141">INPUTS</span></span>

### <span data-ttu-id="4a2b5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a2b5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a2b5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4a2b5-143">System.String</span></span>

## <span data-ttu-id="4a2b5-144">출력</span><span class="sxs-lookup"><span data-stu-id="4a2b5-144">OUTPUTS</span></span>

### <span data-ttu-id="4a2b5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4a2b5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4a2b5-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a2b5-146">NOTES</span></span>

## <span data-ttu-id="4a2b5-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a2b5-147">RELATED LINKS</span></span>

[<span data-ttu-id="4a2b5-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4a2b5-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4a2b5-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4a2b5-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="4a2b5-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4a2b5-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
