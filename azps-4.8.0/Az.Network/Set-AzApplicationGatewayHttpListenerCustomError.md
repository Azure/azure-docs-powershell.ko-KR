---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214327"
---
# <span data-ttu-id="de8c3-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="de8c3-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="de8c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="de8c3-103">응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="de8c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de8c3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de8c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="de8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="de8c3-106">**AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이의 http 수신기에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="de8c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="de8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="de8c3-108">예제 1: http 수신기에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="de8c3-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="de8c3-109">이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 업데이트 하 고 업데이트 된 수신기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="de8c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="de8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="de8c3-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="de8c3-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="de8c3-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="de8c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8c3-113">-DefaultProfile</span></span>
<span data-ttu-id="de8c3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8c3-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="de8c3-115">-HttpListener</span></span>
<span data-ttu-id="de8c3-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="de8c3-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="de8c3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="de8c3-117">-StatusCode</span></span>
<span data-ttu-id="de8c3-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="de8c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8c3-119">CommonParameters</span></span>
<span data-ttu-id="de8c3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de8c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8c3-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8c3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8c3-122">입력</span><span class="sxs-lookup"><span data-stu-id="de8c3-122">INPUTS</span></span>

### <span data-ttu-id="de8c3-123">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="de8c3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="de8c3-124">출력</span><span class="sxs-lookup"><span data-stu-id="de8c3-124">OUTPUTS</span></span>

### <span data-ttu-id="de8c3-125">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="de8c3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="de8c3-126">상속자</span><span class="sxs-lookup"><span data-stu-id="de8c3-126">NOTES</span></span>

## <span data-ttu-id="de8c3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de8c3-127">RELATED LINKS</span></span>

[<span data-ttu-id="de8c3-128">추가-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="de8c3-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="de8c3-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="de8c3-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="de8c3-130">제거-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="de8c3-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
