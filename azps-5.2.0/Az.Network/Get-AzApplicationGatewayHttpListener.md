---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326311"
---
# <span data-ttu-id="a9b0b-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a9b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b0b-103">애플리케이션 게이트웨이의 HTTP 수신기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a9b0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9b0b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b0b-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b0b-106">**Get-AzApplicationGatewayHttpListener** cmdlet은 애플리케이션 게이트웨이의 HTTP 수신기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a9b0b-107">예제</span><span class="sxs-lookup"><span data-stu-id="a9b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="a9b0b-108">예제 1: 특정 HTTP 수신기 얻기</span><span class="sxs-lookup"><span data-stu-id="a9b0b-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="a9b0b-109">이 명령은 Listener01이라는 HTTP 수신기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="a9b0b-110">예제 2: HTTP 수신기 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="a9b0b-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="a9b0b-111">이 명령은 HTTP 수신기 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="a9b0b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="a9b0b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9b0b-113">-ApplicationGateway</span></span>
<span data-ttu-id="a9b0b-114">HTTP 수신기를 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="a9b0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b0b-115">-DefaultProfile</span></span>
<span data-ttu-id="a9b0b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b0b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9b0b-117">-Name</span></span>
<span data-ttu-id="a9b0b-118">이 cmdlet이 수신하는 HTTP 수신기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="a9b0b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b0b-119">CommonParameters</span></span>
<span data-ttu-id="a9b0b-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b0b-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9b0b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b0b-122">입력</span><span class="sxs-lookup"><span data-stu-id="a9b0b-122">INPUTS</span></span>

### <span data-ttu-id="a9b0b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9b0b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9b0b-124">출력</span><span class="sxs-lookup"><span data-stu-id="a9b0b-124">OUTPUTS</span></span>

### <span data-ttu-id="a9b0b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a9b0b-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9b0b-126">NOTES</span></span>

## <span data-ttu-id="a9b0b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9b0b-127">RELATED LINKS</span></span>

[<span data-ttu-id="a9b0b-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9b0b-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9b0b-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9b0b-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9b0b-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


