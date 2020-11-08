---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056170"
---
# <span data-ttu-id="234c6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="234c6-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="234c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="234c6-102">SYNOPSIS</span></span>
<span data-ttu-id="234c6-103">응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="234c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="234c6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="234c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="234c6-105">DESCRIPTION</span></span>
<span data-ttu-id="234c6-106">**AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="234c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="234c6-107">EXAMPLES</span></span>

### <span data-ttu-id="234c6-108">예제 1: http 수신기에서 사용자 지정 오류 제거</span><span class="sxs-lookup"><span data-stu-id="234c6-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="234c6-109">이 명령은 http 상태 코드 502의 사용자 지정 오류를 http 수신기 $listener 01에서 제거 하 고 업데이트 된 수신기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="234c6-110">변수</span><span class="sxs-lookup"><span data-stu-id="234c6-110">PARAMETERS</span></span>

### <span data-ttu-id="234c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234c6-111">-DefaultProfile</span></span>
<span data-ttu-id="234c6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="234c6-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="234c6-113">-HttpListener</span></span>
<span data-ttu-id="234c6-114">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="234c6-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="234c6-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="234c6-115">-StatusCode</span></span>
<span data-ttu-id="234c6-116">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="234c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234c6-117">CommonParameters</span></span>
<span data-ttu-id="234c6-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="234c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234c6-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="234c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234c6-120">입력</span><span class="sxs-lookup"><span data-stu-id="234c6-120">INPUTS</span></span>

### <span data-ttu-id="234c6-121">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="234c6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="234c6-122">출력</span><span class="sxs-lookup"><span data-stu-id="234c6-122">OUTPUTS</span></span>

### <span data-ttu-id="234c6-123">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="234c6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="234c6-124">상속자</span><span class="sxs-lookup"><span data-stu-id="234c6-124">NOTES</span></span>

## <span data-ttu-id="234c6-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="234c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="234c6-126">추가-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="234c6-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="234c6-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="234c6-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="234c6-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="234c6-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
