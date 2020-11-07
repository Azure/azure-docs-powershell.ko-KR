---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: ec568878c6ecd1d7f80caeb3a77c16c0838373a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702571"
---
# <span data-ttu-id="ebe5b-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe5b-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ebe5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe5b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe5b-103">응용 프로그램 게이트웨이의 WAF 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebe5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebe5b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebe5b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebe5b-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe5b-106">**AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 응용 프로그램 게이트웨이의 waf (웹 응용 프로그램 방화벽) 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ebe5b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ebe5b-107">EXAMPLES</span></span>

### <span data-ttu-id="ebe5b-108">예제 1: 응용 프로그램 게이트웨이 웹 응용 프로그램 방화벽 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="ebe5b-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="ebe5b-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGW 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="ebe5b-110">두 번째 명령은 $AppGW에서 응용 프로그램 게이트웨이의 방화벽 구성을 가져온 다음 $FirewallConfig에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="ebe5b-111">변수</span><span class="sxs-lookup"><span data-stu-id="ebe5b-111">PARAMETERS</span></span>

### <span data-ttu-id="ebe5b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe5b-112">-ApplicationGateway</span></span>
<span data-ttu-id="ebe5b-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ebe5b-114">Get-AzureRmApplicationGateway cmdlet을 사용 하 여 응용 프로그램 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="ebe5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe5b-115">-DefaultProfile</span></span>
<span data-ttu-id="ebe5b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe5b-117">CommonParameters</span></span>
<span data-ttu-id="ebe5b-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe5b-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe5b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe5b-120">입력</span><span class="sxs-lookup"><span data-stu-id="ebe5b-120">INPUTS</span></span>

### <span data-ttu-id="ebe5b-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe5b-121">PSApplicationGateway</span></span>
<span data-ttu-id="ebe5b-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ebe5b-123">출력</span><span class="sxs-lookup"><span data-stu-id="ebe5b-123">OUTPUTS</span></span>

### <span data-ttu-id="ebe5b-124">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ebe5b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ebe5b-125">NOTES</span></span>

## <span data-ttu-id="ebe5b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebe5b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ebe5b-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe5b-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ebe5b-128">새로운 AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe5b-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ebe5b-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe5b-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


