---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495192"
---
# <span data-ttu-id="a953a-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a953a-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="a953a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a953a-102">SYNOPSIS</span></span>
<span data-ttu-id="a953a-103">애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="a953a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a953a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a953a-105">설명</span><span class="sxs-lookup"><span data-stu-id="a953a-105">DESCRIPTION</span></span>
<span data-ttu-id="a953a-106">**Remove-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="a953a-107">예제</span><span class="sxs-lookup"><span data-stu-id="a953a-107">EXAMPLES</span></span>

### <span data-ttu-id="a953a-108">예제 1: http 수신기에서 사용자 지정 오류를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="a953a-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 제거하고 업데이트된 수신기를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="a953a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a953a-110">PARAMETERS</span></span>

### <span data-ttu-id="a953a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a953a-111">-DefaultProfile</span></span>
<span data-ttu-id="a953a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a953a-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="a953a-113">-HttpListener</span></span>
<span data-ttu-id="a953a-114">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="a953a-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="a953a-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a953a-115">-StatusCode</span></span>
<span data-ttu-id="a953a-116">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a953a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a953a-117">CommonParameters</span></span>
<span data-ttu-id="a953a-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a953a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a953a-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a953a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a953a-120">입력</span><span class="sxs-lookup"><span data-stu-id="a953a-120">INPUTS</span></span>

### <span data-ttu-id="a953a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a953a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a953a-122">출력</span><span class="sxs-lookup"><span data-stu-id="a953a-122">OUTPUTS</span></span>

### <span data-ttu-id="a953a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a953a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a953a-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a953a-124">NOTES</span></span>

## <span data-ttu-id="a953a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a953a-125">RELATED LINKS</span></span>

[<span data-ttu-id="a953a-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a953a-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a953a-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a953a-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a953a-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a953a-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
