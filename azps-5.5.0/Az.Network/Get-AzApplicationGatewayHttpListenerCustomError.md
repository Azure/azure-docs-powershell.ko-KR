---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184777"
---
# <span data-ttu-id="2e7bb-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2e7bb-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="2e7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7bb-103">애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="2e7bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e7bb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e7bb-105">설명</span><span class="sxs-lookup"><span data-stu-id="2e7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="2e7bb-106">**Get-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="2e7bb-107">예제</span><span class="sxs-lookup"><span data-stu-id="2e7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="2e7bb-108">예제 1: http 수신기에서 사용자 지정 오류 발생</span><span class="sxs-lookup"><span data-stu-id="2e7bb-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="2e7bb-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 $listener.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="2e7bb-110">예제 2: http 수신기에서 모든 사용자 지정 오류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="2e7bb-111">이 명령은 http listener $listener 01에서 모든 사용자 지정 오류 목록을 $listener.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="2e7bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e7bb-112">PARAMETERS</span></span>

### <span data-ttu-id="2e7bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7bb-113">-DefaultProfile</span></span>
<span data-ttu-id="2e7bb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e7bb-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="2e7bb-115">-HttpListener</span></span>
<span data-ttu-id="2e7bb-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="2e7bb-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="2e7bb-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="2e7bb-117">-StatusCode</span></span>
<span data-ttu-id="2e7bb-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="2e7bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7bb-119">CommonParameters</span></span>
<span data-ttu-id="2e7bb-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7bb-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7bb-122">입력</span><span class="sxs-lookup"><span data-stu-id="2e7bb-122">INPUTS</span></span>

### <span data-ttu-id="2e7bb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2e7bb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="2e7bb-124">출력</span><span class="sxs-lookup"><span data-stu-id="2e7bb-124">OUTPUTS</span></span>

### <span data-ttu-id="2e7bb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2e7bb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="2e7bb-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e7bb-126">NOTES</span></span>

## <span data-ttu-id="2e7bb-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e7bb-127">RELATED LINKS</span></span>

[<span data-ttu-id="2e7bb-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2e7bb-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="2e7bb-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2e7bb-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="2e7bb-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2e7bb-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
