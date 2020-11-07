---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cf8d7453961796afb4b0aa94d549d80eb9279ab5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869606"
---
# <span data-ttu-id="ccb85-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ccb85-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="ccb85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb85-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb85-103">응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="ccb85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccb85-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccb85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ccb85-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb85-106">**AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="ccb85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ccb85-107">EXAMPLES</span></span>

### <span data-ttu-id="ccb85-108">예제 1: http 수신기에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="ccb85-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="ccb85-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 업데이트 하 고 업데이트 된 수신기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="ccb85-110">변수</span><span class="sxs-lookup"><span data-stu-id="ccb85-110">PARAMETERS</span></span>

### <span data-ttu-id="ccb85-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ccb85-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ccb85-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ccb85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb85-113">-DefaultProfile</span></span>
<span data-ttu-id="ccb85-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccb85-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ccb85-115">-HttpListener</span></span>
<span data-ttu-id="ccb85-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="ccb85-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="ccb85-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ccb85-117">-StatusCode</span></span>
<span data-ttu-id="ccb85-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ccb85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb85-119">CommonParameters</span></span>
<span data-ttu-id="ccb85-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb85-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb85-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb85-122">입력</span><span class="sxs-lookup"><span data-stu-id="ccb85-122">INPUTS</span></span>

### <span data-ttu-id="ccb85-123">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ccb85-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ccb85-124">출력</span><span class="sxs-lookup"><span data-stu-id="ccb85-124">OUTPUTS</span></span>

### <span data-ttu-id="ccb85-125">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ccb85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ccb85-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ccb85-126">NOTES</span></span>

## <span data-ttu-id="ccb85-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccb85-127">RELATED LINKS</span></span>

[<span data-ttu-id="ccb85-128">추가-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ccb85-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ccb85-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ccb85-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ccb85-130">제거-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ccb85-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
