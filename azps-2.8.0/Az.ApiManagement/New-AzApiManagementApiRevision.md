---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 1a58c34aac272f6c8278833cd356de66774c5a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698072"
---
# <span data-ttu-id="9f759-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f759-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="9f759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f759-102">SYNOPSIS</span></span>
<span data-ttu-id="9f759-103">기존 API의 새 수정 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="9f759-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f759-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f759-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9f759-105">DESCRIPTION</span></span>

<span data-ttu-id="9f759-106">**AzApiManagementApiRevision** CMDLET은 api Management 컨텍스트에서 기존 api에 대 한 api 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="9f759-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9f759-107">EXAMPLES</span></span>

### <span data-ttu-id="9f759-108">예제 1: API에 대 한 빈 API 수정 버전 만들기</span><span class="sxs-lookup"><span data-stu-id="9f759-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="9f759-109">이 명령은 api의 API 수정을 만듭니다 `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="9f759-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="9f759-110">예제 2: 기존 Api에서 API 수정 버전 만들기 및 모든 작업, 태그 및 정책 복사</span><span class="sxs-lookup"><span data-stu-id="9f759-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="9f759-111">이 명령은 api의 API 수정을 만듭니다 `5` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="9f759-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="9f759-112">변수</span><span class="sxs-lookup"><span data-stu-id="9f759-112">PARAMETERS</span></span>

### <span data-ttu-id="9f759-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9f759-113">-ApiId</span></span>
<span data-ttu-id="9f759-114">수정을 만들 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="9f759-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f759-115">-ApiRevision</span></span>
<span data-ttu-id="9f759-116">Api의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="9f759-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="9f759-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="9f759-118">Api 수정 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-118">Api Revision Description.</span></span> <span data-ttu-id="9f759-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f759-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9f759-120">-Context</span></span>
<span data-ttu-id="9f759-121">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f759-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-122">This parameter is required.</span></span>

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

### <span data-ttu-id="9f759-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f759-123">-DefaultProfile</span></span>
<span data-ttu-id="9f759-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f759-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9f759-125">-ServiceUrl</span></span>
<span data-ttu-id="9f759-126">백 엔드 서비스의 API를 노출 하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="9f759-127">이 URL은 Azure API Management에만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="9f759-128">1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="9f759-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-129">This parameter is required.</span></span>

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

### <span data-ttu-id="9f759-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f759-130">-SourceApiRevision</span></span>
<span data-ttu-id="9f759-131">원본 API의 Api 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="9f759-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f759-133">-확인</span><span class="sxs-lookup"><span data-stu-id="9f759-133">-Confirm</span></span>
<span data-ttu-id="9f759-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f759-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f759-135">-WhatIf</span></span>
<span data-ttu-id="9f759-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f759-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f759-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f759-138">CommonParameters</span></span>
<span data-ttu-id="9f759-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f759-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f759-140">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f759-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f759-141">입력</span><span class="sxs-lookup"><span data-stu-id="9f759-141">INPUTS</span></span>

### <span data-ttu-id="9f759-142">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f759-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f759-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f759-143">System.String</span></span>

## <span data-ttu-id="9f759-144">출력</span><span class="sxs-lookup"><span data-stu-id="9f759-144">OUTPUTS</span></span>

### <span data-ttu-id="9f759-145">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f759-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9f759-146">상속자</span><span class="sxs-lookup"><span data-stu-id="9f759-146">NOTES</span></span>

## <span data-ttu-id="9f759-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f759-147">RELATED LINKS</span></span>

[<span data-ttu-id="9f759-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f759-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9f759-149">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f759-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="9f759-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f759-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
