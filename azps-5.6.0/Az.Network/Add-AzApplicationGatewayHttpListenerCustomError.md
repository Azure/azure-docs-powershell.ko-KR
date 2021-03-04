---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d7ca75fbd2d033f35fa237113bc32bdc4699955a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982624"
---
# <span data-ttu-id="f76ff-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f76ff-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f76ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f76ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f76ff-103">애플리케이션 게이트웨이의 http 수신기에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f76ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="f76ff-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f76ff-105">설명</span><span class="sxs-lookup"><span data-stu-id="f76ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f76ff-106">**Add-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f76ff-107">예제</span><span class="sxs-lookup"><span data-stu-id="f76ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f76ff-108">예제 1: http 수신기 수준에 사용자 지정 오류 추가</span><span class="sxs-lookup"><span data-stu-id="f76ff-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f76ff-109">이 명령은 http 수신기 $listener 01에 http 상태 코드 502의 사용자 지정 오류를 추가하고 업데이트된 수신기를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f76ff-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f76ff-110">PARAMETERS</span></span>

### <span data-ttu-id="f76ff-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f76ff-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f76ff-112">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f76ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76ff-113">-DefaultProfile</span></span>
<span data-ttu-id="f76ff-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f76ff-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f76ff-115">-HttpListener</span></span>
<span data-ttu-id="f76ff-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="f76ff-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f76ff-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f76ff-117">-StatusCode</span></span>
<span data-ttu-id="f76ff-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f76ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76ff-119">CommonParameters</span></span>
<span data-ttu-id="f76ff-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f76ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76ff-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f76ff-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76ff-122">입력</span><span class="sxs-lookup"><span data-stu-id="f76ff-122">INPUTS</span></span>

### <span data-ttu-id="f76ff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f76ff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f76ff-124">출력</span><span class="sxs-lookup"><span data-stu-id="f76ff-124">OUTPUTS</span></span>

### <span data-ttu-id="f76ff-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f76ff-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f76ff-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f76ff-126">NOTES</span></span>

## <span data-ttu-id="f76ff-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f76ff-127">RELATED LINKS</span></span>

[<span data-ttu-id="f76ff-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f76ff-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f76ff-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f76ff-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f76ff-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f76ff-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
