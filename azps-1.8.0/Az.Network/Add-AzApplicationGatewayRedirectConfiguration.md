---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 6db510e79d2c1796cf62a1fd00e55e7860164af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700737"
---
# <span data-ttu-id="79e92-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e92-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="79e92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e92-102">SYNOPSIS</span></span>
<span data-ttu-id="79e92-103">응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="79e92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79e92-104">SYNTAX</span></span>

### <span data-ttu-id="79e92-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79e92-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e92-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="79e92-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e92-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="79e92-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e92-108">설명은</span><span class="sxs-lookup"><span data-stu-id="79e92-108">DESCRIPTION</span></span>
<span data-ttu-id="79e92-109">**Add-AzApplicationGatewayRedirectConfiguration** Cmdlet은 응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="79e92-110">예제의</span><span class="sxs-lookup"><span data-stu-id="79e92-110">EXAMPLES</span></span>

### <span data-ttu-id="79e92-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="79e92-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="79e92-112">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="79e92-113">두 번째 명령은 응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="79e92-114">변수</span><span class="sxs-lookup"><span data-stu-id="79e92-114">PARAMETERS</span></span>

### <span data-ttu-id="79e92-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e92-115">-ApplicationGateway</span></span>
<span data-ttu-id="79e92-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e92-116">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e92-117">-DefaultProfile</span></span>
<span data-ttu-id="79e92-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e92-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="79e92-119">-IncludePath</span></span>
<span data-ttu-id="79e92-120">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-120">Include path in the redirected url.</span></span>
<span data-ttu-id="79e92-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-121">Default is true.</span></span>

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

### <span data-ttu-id="79e92-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="79e92-122">-IncludeQueryString</span></span>
<span data-ttu-id="79e92-123">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="79e92-124">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-124">Default is true.</span></span>

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

### <span data-ttu-id="79e92-125">-이름</span><span class="sxs-lookup"><span data-stu-id="79e92-125">-Name</span></span>
<span data-ttu-id="79e92-126">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="79e92-127">RedirectType</span><span class="sxs-lookup"><span data-stu-id="79e92-127">-RedirectType</span></span>
<span data-ttu-id="79e92-128">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="79e92-128">The type of redirect</span></span>

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

### <span data-ttu-id="79e92-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="79e92-129">-TargetListener</span></span>
<span data-ttu-id="79e92-130">요청을 리디렉션할 HTTP 수신기</span><span class="sxs-lookup"><span data-stu-id="79e92-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="79e92-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="79e92-131">-TargetListenerID</span></span>
<span data-ttu-id="79e92-132">요청을 리디렉션할 HTTP 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="79e92-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="79e92-133">-TargetUrl</span></span>
<span data-ttu-id="79e92-134">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="79e92-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="79e92-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e92-135">CommonParameters</span></span>
<span data-ttu-id="79e92-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e92-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e92-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e92-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e92-138">입력</span><span class="sxs-lookup"><span data-stu-id="79e92-138">INPUTS</span></span>

### <span data-ttu-id="79e92-139">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e92-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79e92-140">출력</span><span class="sxs-lookup"><span data-stu-id="79e92-140">OUTPUTS</span></span>

### <span data-ttu-id="79e92-141">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e92-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79e92-142">상속자</span><span class="sxs-lookup"><span data-stu-id="79e92-142">NOTES</span></span>

## <span data-ttu-id="79e92-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79e92-143">RELATED LINKS</span></span>

[<span data-ttu-id="79e92-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e92-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="79e92-145">새로운 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e92-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="79e92-146">제거-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e92-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="79e92-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e92-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
