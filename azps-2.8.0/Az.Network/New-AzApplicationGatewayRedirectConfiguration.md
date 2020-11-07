---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870525"
---
# <span data-ttu-id="96016-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="96016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96016-102">SYNOPSIS</span></span>
<span data-ttu-id="96016-103">응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96016-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="96016-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96016-104">SYNTAX</span></span>

### <span data-ttu-id="96016-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="96016-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96016-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="96016-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96016-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="96016-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96016-108">설명은</span><span class="sxs-lookup"><span data-stu-id="96016-108">DESCRIPTION</span></span>
<span data-ttu-id="96016-109">**AzApplicationGatewayRedirectConfiguration Cmdlet은** 응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96016-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="96016-110">예제의</span><span class="sxs-lookup"><span data-stu-id="96016-110">EXAMPLES</span></span>

### <span data-ttu-id="96016-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="96016-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="96016-112">이 명령은 Redirect01 이라는 리디렉션 구성을 만들고 그 결과를 $RedirectConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96016-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="96016-113">변수</span><span class="sxs-lookup"><span data-stu-id="96016-113">PARAMETERS</span></span>

### <span data-ttu-id="96016-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96016-114">-DefaultProfile</span></span>
<span data-ttu-id="96016-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96016-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="96016-116">-IncludePath</span></span>
<span data-ttu-id="96016-117">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-117">Include path in the redirected url.</span></span>
<span data-ttu-id="96016-118">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-118">Default is true.</span></span>

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

### <span data-ttu-id="96016-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="96016-119">-IncludeQueryString</span></span>
<span data-ttu-id="96016-120">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="96016-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="96016-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-121">Default is true.</span></span>

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

### <span data-ttu-id="96016-122">-이름</span><span class="sxs-lookup"><span data-stu-id="96016-122">-Name</span></span>
<span data-ttu-id="96016-123">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="96016-124">RedirectType</span><span class="sxs-lookup"><span data-stu-id="96016-124">-RedirectType</span></span>
<span data-ttu-id="96016-125">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="96016-125">The type of redirect</span></span>

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

### <span data-ttu-id="96016-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="96016-126">-TargetListener</span></span>
<span data-ttu-id="96016-127">요청을 리디렉션할 HTTP 수신기</span><span class="sxs-lookup"><span data-stu-id="96016-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="96016-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="96016-128">-TargetListenerID</span></span>
<span data-ttu-id="96016-129">요청을 리디렉션할 HTTP 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96016-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="96016-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="96016-130">-TargetUrl</span></span>
<span data-ttu-id="96016-131">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="96016-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="96016-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96016-132">CommonParameters</span></span>
<span data-ttu-id="96016-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96016-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96016-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96016-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96016-135">입력</span><span class="sxs-lookup"><span data-stu-id="96016-135">INPUTS</span></span>

### <span data-ttu-id="96016-136">않아야</span><span class="sxs-lookup"><span data-stu-id="96016-136">None</span></span>

## <span data-ttu-id="96016-137">출력</span><span class="sxs-lookup"><span data-stu-id="96016-137">OUTPUTS</span></span>

### <span data-ttu-id="96016-138">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="96016-139">상속자</span><span class="sxs-lookup"><span data-stu-id="96016-139">NOTES</span></span>

## <span data-ttu-id="96016-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96016-140">RELATED LINKS</span></span>

[<span data-ttu-id="96016-141">추가-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96016-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96016-143">제거-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96016-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96016-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
