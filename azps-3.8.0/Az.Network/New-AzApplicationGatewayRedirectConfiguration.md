---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b6bfe8b7064324dea353543e0e9debe77e4b2edd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044788"
---
# <span data-ttu-id="fad48-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fad48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fad48-102">SYNOPSIS</span></span>
<span data-ttu-id="fad48-103">응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="fad48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fad48-104">SYNTAX</span></span>

### <span data-ttu-id="fad48-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fad48-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad48-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fad48-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad48-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="fad48-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fad48-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fad48-108">DESCRIPTION</span></span>
<span data-ttu-id="fad48-109">**AzApplicationGatewayRedirectConfiguration Cmdlet은** 응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="fad48-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fad48-110">EXAMPLES</span></span>

### <span data-ttu-id="fad48-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fad48-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="fad48-112">이 명령은 Redirect01 이라는 리디렉션 구성을 만들고 그 결과를 $RedirectConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="fad48-113">변수</span><span class="sxs-lookup"><span data-stu-id="fad48-113">PARAMETERS</span></span>

### <span data-ttu-id="fad48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad48-114">-DefaultProfile</span></span>
<span data-ttu-id="fad48-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad48-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="fad48-116">-IncludePath</span></span>
<span data-ttu-id="fad48-117">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-117">Include path in the redirected url.</span></span>
<span data-ttu-id="fad48-118">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-118">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="fad48-119">-IncludeQueryString</span></span>
<span data-ttu-id="fad48-120">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="fad48-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fad48-122">-Name</span></span>
<span data-ttu-id="fad48-123">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-123">The name of the Redirect Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-124">RedirectType</span><span class="sxs-lookup"><span data-stu-id="fad48-124">-RedirectType</span></span>
<span data-ttu-id="fad48-125">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="fad48-125">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="fad48-126">-TargetListener</span></span>
<span data-ttu-id="fad48-127">요청을 리디렉션할 HTTP 수신기</span><span class="sxs-lookup"><span data-stu-id="fad48-127">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="fad48-128">-TargetListenerID</span></span>
<span data-ttu-id="fad48-129">요청을 리디렉션할 HTTP 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-129">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="fad48-130">-TargetUrl</span></span>
<span data-ttu-id="fad48-131">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="fad48-131">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad48-132">CommonParameters</span></span>
<span data-ttu-id="fad48-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad48-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad48-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad48-135">입력</span><span class="sxs-lookup"><span data-stu-id="fad48-135">INPUTS</span></span>

### <span data-ttu-id="fad48-136">않아야</span><span class="sxs-lookup"><span data-stu-id="fad48-136">None</span></span>

## <span data-ttu-id="fad48-137">출력</span><span class="sxs-lookup"><span data-stu-id="fad48-137">OUTPUTS</span></span>

### <span data-ttu-id="fad48-138">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fad48-139">상속자</span><span class="sxs-lookup"><span data-stu-id="fad48-139">NOTES</span></span>

## <span data-ttu-id="fad48-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fad48-140">RELATED LINKS</span></span>

[<span data-ttu-id="fad48-141">추가-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fad48-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fad48-143">제거-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fad48-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad48-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
