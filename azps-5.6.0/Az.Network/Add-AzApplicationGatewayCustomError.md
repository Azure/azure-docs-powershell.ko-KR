---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: f5c36cc9e6133fbde4e7bae34b4bc6b479afb96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967995"
---
# <span data-ttu-id="03c7f-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="03c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="03c7f-103">애플리케이션 게이트웨이에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="03c7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="03c7f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03c7f-105">설명</span><span class="sxs-lookup"><span data-stu-id="03c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="03c7f-106">**Add-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="03c7f-107">예제</span><span class="sxs-lookup"><span data-stu-id="03c7f-107">EXAMPLES</span></span>

### <span data-ttu-id="03c7f-108">예제 1: 애플리케이션 게이트웨이 수준에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="03c7f-109">이 명령은 애플리케이션 게이트웨이에 http 상태 코드 502의 사용자 지정 오류를 $appgw 업데이트된 게이트웨이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="03c7f-110">예제 2: 애플리케이션 게이트웨이 수신기 수준에 사용자 지정 오류를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="03c7f-111">이 명령은 수신기 수준에서 애플리케이션 게이트웨이에 http 상태 코드 502의 사용자 지정 $appgw 추가하고 업데이트된 게이트웨이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="03c7f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03c7f-112">PARAMETERS</span></span>

### <span data-ttu-id="03c7f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03c7f-113">-ApplicationGateway</span></span>
<span data-ttu-id="03c7f-114">애플리케이션 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="03c7f-114">The Application Gateway</span></span>

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

### <span data-ttu-id="03c7f-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="03c7f-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="03c7f-116">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="03c7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c7f-117">-DefaultProfile</span></span>
<span data-ttu-id="03c7f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c7f-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="03c7f-119">-StatusCode</span></span>
<span data-ttu-id="03c7f-120">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="03c7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c7f-121">CommonParameters</span></span>
<span data-ttu-id="03c7f-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03c7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c7f-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03c7f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c7f-124">입력</span><span class="sxs-lookup"><span data-stu-id="03c7f-124">INPUTS</span></span>

### <span data-ttu-id="03c7f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03c7f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03c7f-126">출력</span><span class="sxs-lookup"><span data-stu-id="03c7f-126">OUTPUTS</span></span>

### <span data-ttu-id="03c7f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="03c7f-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03c7f-128">NOTES</span></span>

## <span data-ttu-id="03c7f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03c7f-129">RELATED LINKS</span></span>

[<span data-ttu-id="03c7f-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="03c7f-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="03c7f-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="03c7f-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="03c7f-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
