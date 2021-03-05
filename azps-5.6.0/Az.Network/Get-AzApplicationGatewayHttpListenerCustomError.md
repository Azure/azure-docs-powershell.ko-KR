---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001216"
---
# <span data-ttu-id="77add-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77add-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="77add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77add-102">SYNOPSIS</span></span>
<span data-ttu-id="77add-103">애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="77add-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="77add-104">구문</span><span class="sxs-lookup"><span data-stu-id="77add-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77add-105">설명</span><span class="sxs-lookup"><span data-stu-id="77add-105">DESCRIPTION</span></span>
<span data-ttu-id="77add-106">**Get-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77add-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="77add-107">예제</span><span class="sxs-lookup"><span data-stu-id="77add-107">EXAMPLES</span></span>

### <span data-ttu-id="77add-108">예제 1: http 수신기에서 사용자 지정 오류 발생</span><span class="sxs-lookup"><span data-stu-id="77add-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="77add-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 $listener 01을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="77add-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="77add-110">예제 2: http 수신기에서 모든 사용자 지정 오류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77add-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="77add-111">이 명령은 http 수신기에서 모든 사용자 지정 오류 목록을 $listener 01을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="77add-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="77add-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="77add-112">PARAMETERS</span></span>

### <span data-ttu-id="77add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77add-113">-DefaultProfile</span></span>
<span data-ttu-id="77add-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77add-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77add-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="77add-115">-HttpListener</span></span>
<span data-ttu-id="77add-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="77add-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="77add-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="77add-117">-StatusCode</span></span>
<span data-ttu-id="77add-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="77add-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77add-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77add-119">CommonParameters</span></span>
<span data-ttu-id="77add-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77add-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77add-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77add-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77add-122">입력</span><span class="sxs-lookup"><span data-stu-id="77add-122">INPUTS</span></span>

### <span data-ttu-id="77add-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77add-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="77add-124">출력</span><span class="sxs-lookup"><span data-stu-id="77add-124">OUTPUTS</span></span>

### <span data-ttu-id="77add-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="77add-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="77add-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77add-126">NOTES</span></span>

## <span data-ttu-id="77add-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77add-127">RELATED LINKS</span></span>

[<span data-ttu-id="77add-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77add-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="77add-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77add-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="77add-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="77add-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
