---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203261"
---
# <span data-ttu-id="edde1-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="edde1-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="edde1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edde1-102">SYNOPSIS</span></span>
<span data-ttu-id="edde1-103">애플리케이션 게이트웨이의 http 수신기에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="edde1-104">구문</span><span class="sxs-lookup"><span data-stu-id="edde1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edde1-105">설명</span><span class="sxs-lookup"><span data-stu-id="edde1-105">DESCRIPTION</span></span>
<span data-ttu-id="edde1-106">**Add-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="edde1-107">예제</span><span class="sxs-lookup"><span data-stu-id="edde1-107">EXAMPLES</span></span>

### <span data-ttu-id="edde1-108">예제 1: http 수신기 수준에 사용자 지정 오류 추가</span><span class="sxs-lookup"><span data-stu-id="edde1-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="edde1-109">이 명령은 http 상태 코드 502의 사용자 지정 오류를 http 수신기 $listener 01에 추가하고 업데이트된 수신기 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="edde1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edde1-110">PARAMETERS</span></span>

### <span data-ttu-id="edde1-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="edde1-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="edde1-112">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="edde1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edde1-113">-DefaultProfile</span></span>
<span data-ttu-id="edde1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edde1-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="edde1-115">-HttpListener</span></span>
<span data-ttu-id="edde1-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="edde1-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="edde1-117">-StatusCode</span></span>
<span data-ttu-id="edde1-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="edde1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edde1-119">CommonParameters</span></span>
<span data-ttu-id="edde1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edde1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edde1-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="edde1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edde1-122">입력</span><span class="sxs-lookup"><span data-stu-id="edde1-122">INPUTS</span></span>

### <span data-ttu-id="edde1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edde1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="edde1-124">출력</span><span class="sxs-lookup"><span data-stu-id="edde1-124">OUTPUTS</span></span>

### <span data-ttu-id="edde1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="edde1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="edde1-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edde1-126">NOTES</span></span>

## <span data-ttu-id="edde1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edde1-127">RELATED LINKS</span></span>

[<span data-ttu-id="edde1-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="edde1-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="edde1-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="edde1-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="edde1-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="edde1-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
