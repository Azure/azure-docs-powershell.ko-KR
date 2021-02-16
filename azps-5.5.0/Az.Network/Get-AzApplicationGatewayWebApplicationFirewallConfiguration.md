---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203111"
---
# <span data-ttu-id="65ea0-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="65ea0-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="65ea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="65ea0-103">애플리케이션 게이트웨이의 WAF 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="65ea0-104">구문</span><span class="sxs-lookup"><span data-stu-id="65ea0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ea0-105">설명</span><span class="sxs-lookup"><span data-stu-id="65ea0-105">DESCRIPTION</span></span>
<span data-ttu-id="65ea0-106">**Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 애플리케이션 게이트웨이의 WAF(웹 애플리케이션 방화벽) 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="65ea0-107">예제</span><span class="sxs-lookup"><span data-stu-id="65ea0-107">EXAMPLES</span></span>

### <span data-ttu-id="65ea0-108">예제 1: 애플리케이션 게이트웨이 웹 애플리케이션 방화벽 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="65ea0-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 구한 다음, 애플리케이션 $AppGW 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="65ea0-110">두 번째 명령은 애플리케이션 게이트웨이의 방화벽 구성을 $AppGW 다음, 애플리케이션 게이트웨이에 $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="65ea0-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="65ea0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65ea0-111">PARAMETERS</span></span>

### <span data-ttu-id="65ea0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65ea0-112">-ApplicationGateway</span></span>
<span data-ttu-id="65ea0-113">애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="65ea0-114">애플리케이션 게이트웨이 개체를 Get-AzApplicationGateway cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="65ea0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ea0-115">-DefaultProfile</span></span>
<span data-ttu-id="65ea0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ea0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ea0-117">CommonParameters</span></span>
<span data-ttu-id="65ea0-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ea0-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65ea0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ea0-120">입력</span><span class="sxs-lookup"><span data-stu-id="65ea0-120">INPUTS</span></span>

### <span data-ttu-id="65ea0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65ea0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65ea0-122">출력</span><span class="sxs-lookup"><span data-stu-id="65ea0-122">OUTPUTS</span></span>

### <span data-ttu-id="65ea0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="65ea0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="65ea0-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65ea0-124">NOTES</span></span>

## <span data-ttu-id="65ea0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65ea0-125">RELATED LINKS</span></span>

[<span data-ttu-id="65ea0-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65ea0-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="65ea0-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="65ea0-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="65ea0-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="65ea0-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


