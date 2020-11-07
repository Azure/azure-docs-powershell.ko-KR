---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 0df6ae98692b7497448b0d3f15e88f1a18a87ae8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870354"
---
# <span data-ttu-id="06f20-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="06f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f20-102">SYNOPSIS</span></span>
<span data-ttu-id="06f20-103">응용 프로그램 게이트웨이에 사용자 지정 오류를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="06f20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06f20-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06f20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06f20-105">DESCRIPTION</span></span>
<span data-ttu-id="06f20-106">**Add-AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에 사용자 지정 오류를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="06f20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06f20-107">EXAMPLES</span></span>

### <span data-ttu-id="06f20-108">예제 1: 사용자 지정 오류를 응용 프로그램 게이트웨이 수준에 추가</span><span class="sxs-lookup"><span data-stu-id="06f20-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="06f20-109">이 명령은 http 상태 코드 502의 사용자 지정 오류를 응용 프로그램 게이트웨이 $appgw에 추가 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="06f20-110">예제 2: 사용자 지정 오류를 응용 프로그램 게이트웨이 수신기 수준에 추가</span><span class="sxs-lookup"><span data-stu-id="06f20-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="06f20-111">이 명령은 http 상태 코드 502의 사용자 지정 오류를 수신기 수준에서 $appgw 응용 프로그램 게이트웨이에 추가 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="06f20-112">변수</span><span class="sxs-lookup"><span data-stu-id="06f20-112">PARAMETERS</span></span>

### <span data-ttu-id="06f20-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06f20-113">-ApplicationGateway</span></span>
<span data-ttu-id="06f20-114">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="06f20-114">The Application Gateway</span></span>

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

### <span data-ttu-id="06f20-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="06f20-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="06f20-116">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="06f20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f20-117">-DefaultProfile</span></span>
<span data-ttu-id="06f20-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f20-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="06f20-119">-StatusCode</span></span>
<span data-ttu-id="06f20-120">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="06f20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f20-121">CommonParameters</span></span>
<span data-ttu-id="06f20-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f20-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f20-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f20-124">입력</span><span class="sxs-lookup"><span data-stu-id="06f20-124">INPUTS</span></span>

### <span data-ttu-id="06f20-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06f20-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06f20-126">출력</span><span class="sxs-lookup"><span data-stu-id="06f20-126">OUTPUTS</span></span>

### <span data-ttu-id="06f20-127">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="06f20-128">상속자</span><span class="sxs-lookup"><span data-stu-id="06f20-128">NOTES</span></span>

## <span data-ttu-id="06f20-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06f20-129">RELATED LINKS</span></span>

[<span data-ttu-id="06f20-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06f20-131">새로운 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06f20-132">제거-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06f20-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06f20-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
