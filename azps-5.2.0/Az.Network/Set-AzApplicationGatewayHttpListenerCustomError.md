---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323770"
---
# <span data-ttu-id="1e59e-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1e59e-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1e59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e59e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e59e-103">애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="1e59e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e59e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e59e-105">설명</span><span class="sxs-lookup"><span data-stu-id="1e59e-105">DESCRIPTION</span></span>
<span data-ttu-id="1e59e-106">**Set-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="1e59e-107">예제</span><span class="sxs-lookup"><span data-stu-id="1e59e-107">EXAMPLES</span></span>

### <span data-ttu-id="1e59e-108">예제 1: http 수신기에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e59e-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="1e59e-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 업데이트하고 업데이트된 수신기 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="1e59e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e59e-110">PARAMETERS</span></span>

### <span data-ttu-id="1e59e-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="1e59e-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="1e59e-112">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1e59e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e59e-113">-DefaultProfile</span></span>
<span data-ttu-id="1e59e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e59e-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1e59e-115">-HttpListener</span></span>
<span data-ttu-id="1e59e-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="1e59e-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1e59e-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1e59e-117">-StatusCode</span></span>
<span data-ttu-id="1e59e-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1e59e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e59e-119">CommonParameters</span></span>
<span data-ttu-id="1e59e-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e59e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e59e-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e59e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e59e-122">입력</span><span class="sxs-lookup"><span data-stu-id="1e59e-122">INPUTS</span></span>

### <span data-ttu-id="1e59e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1e59e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1e59e-124">출력</span><span class="sxs-lookup"><span data-stu-id="1e59e-124">OUTPUTS</span></span>

### <span data-ttu-id="1e59e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1e59e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1e59e-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e59e-126">NOTES</span></span>

## <span data-ttu-id="1e59e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e59e-127">RELATED LINKS</span></span>

[<span data-ttu-id="1e59e-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1e59e-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1e59e-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1e59e-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1e59e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1e59e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
