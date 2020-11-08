---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056210"
---
# <span data-ttu-id="d3b11-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d3b11-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d3b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b11-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b11-103">응용 프로그램 게이트웨이의 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d3b11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3b11-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3b11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3b11-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b11-106">**Get-AzApplicationGatewayHttpListener** cmdlet은 응용 프로그램 게이트웨이의 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d3b11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3b11-107">EXAMPLES</span></span>

### <span data-ttu-id="d3b11-108">예제 1: 특정 HTTP 수신기 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3b11-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="d3b11-109">이 명령은 Listener01 이라는 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="d3b11-110">예제 2: HTTP 수신기 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3b11-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="d3b11-111">이 명령은 HTTP 수신기 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="d3b11-112">변수</span><span class="sxs-lookup"><span data-stu-id="d3b11-112">PARAMETERS</span></span>

### <span data-ttu-id="d3b11-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3b11-113">-ApplicationGateway</span></span>
<span data-ttu-id="d3b11-114">HTTP 수신기를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="d3b11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b11-115">-DefaultProfile</span></span>
<span data-ttu-id="d3b11-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3b11-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d3b11-117">-Name</span></span>
<span data-ttu-id="d3b11-118">이 cmdlet이 가져오는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3b11-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b11-119">CommonParameters</span></span>
<span data-ttu-id="d3b11-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b11-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b11-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3b11-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b11-122">입력</span><span class="sxs-lookup"><span data-stu-id="d3b11-122">INPUTS</span></span>

### <span data-ttu-id="d3b11-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3b11-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3b11-124">출력</span><span class="sxs-lookup"><span data-stu-id="d3b11-124">OUTPUTS</span></span>

### <span data-ttu-id="d3b11-125">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d3b11-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d3b11-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d3b11-126">NOTES</span></span>

## <span data-ttu-id="d3b11-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3b11-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3b11-128">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d3b11-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d3b11-129">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d3b11-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d3b11-130">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d3b11-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d3b11-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d3b11-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


