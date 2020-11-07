---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689108"
---
# <span data-ttu-id="c3bc2-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c3bc2-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="c3bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bc2-103">기존 API의 새 수정 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="c3bc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3bc2-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3bc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c3bc2-105">DESCRIPTION</span></span>

<span data-ttu-id="c3bc2-106">**AzApiManagementApiRevision** CMDLET은 api Management 컨텍스트에서 기존 api에 대 한 api 수정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="c3bc2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c3bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="c3bc2-108">예제 1: API에 대 한 API 수정 버전 만들기</span><span class="sxs-lookup"><span data-stu-id="c3bc2-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="c3bc2-109">이 명령은 api의 API 수정을 만듭니다 `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="c3bc2-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="c3bc2-110">변수</span><span class="sxs-lookup"><span data-stu-id="c3bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="c3bc2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c3bc2-111">-ApiId</span></span>
<span data-ttu-id="c3bc2-112">수정을 만들 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="c3bc2-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c3bc2-113">-ApiRevision</span></span>
<span data-ttu-id="c3bc2-114">Api의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="c3bc2-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c3bc2-115">-Context</span></span>
<span data-ttu-id="c3bc2-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c3bc2-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c3bc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bc2-118">-DefaultProfile</span></span>
<span data-ttu-id="c3bc2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3bc2-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c3bc2-120">-Confirm</span></span>
<span data-ttu-id="c3bc2-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3bc2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3bc2-122">-WhatIf</span></span>
<span data-ttu-id="c3bc2-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3bc2-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3bc2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bc2-125">CommonParameters</span></span>
<span data-ttu-id="c3bc2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bc2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bc2-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3bc2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bc2-128">입력</span><span class="sxs-lookup"><span data-stu-id="c3bc2-128">INPUTS</span></span>

### <span data-ttu-id="c3bc2-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3bc2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3bc2-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3bc2-130">System.String</span></span>

## <span data-ttu-id="c3bc2-131">출력</span><span class="sxs-lookup"><span data-stu-id="c3bc2-131">OUTPUTS</span></span>

### <span data-ttu-id="c3bc2-132">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c3bc2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c3bc2-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c3bc2-133">NOTES</span></span>

## <span data-ttu-id="c3bc2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3bc2-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3bc2-135">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c3bc2-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="c3bc2-136">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c3bc2-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="c3bc2-137">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c3bc2-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
