---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 77a87d80e656098eeb9450b0ed612d82a8b9e7fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875606"
---
# <span data-ttu-id="2d258-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d258-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="2d258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d258-102">SYNOPSIS</span></span>
<span data-ttu-id="2d258-103">응용 프로그램 게이트웨이의 WAF 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="2d258-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d258-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d258-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d258-105">DESCRIPTION</span></span>
<span data-ttu-id="2d258-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 응용 프로그램 게이트웨이의 waf (웹 응용 프로그램 방화벽) 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="2d258-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d258-107">EXAMPLES</span></span>

### <span data-ttu-id="2d258-108">예제 1: 응용 프로그램 게이트웨이 웹 응용 프로그램 방화벽 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d258-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="2d258-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGW 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="2d258-110">두 번째 명령은 $AppGW에서 응용 프로그램 게이트웨이의 방화벽 구성을 가져온 다음 $FirewallConfig에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="2d258-111">변수</span><span class="sxs-lookup"><span data-stu-id="2d258-111">PARAMETERS</span></span>

### <span data-ttu-id="2d258-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d258-112">-ApplicationGateway</span></span>
<span data-ttu-id="2d258-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="2d258-114">Get-AzApplicationGateway cmdlet을 사용 하 여 응용 프로그램 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d258-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d258-115">-DefaultProfile</span></span>
<span data-ttu-id="2d258-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d258-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d258-117">CommonParameters</span></span>
<span data-ttu-id="2d258-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d258-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d258-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d258-120">입력</span><span class="sxs-lookup"><span data-stu-id="2d258-120">INPUTS</span></span>

### <span data-ttu-id="2d258-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d258-121">PSApplicationGateway</span></span>
<span data-ttu-id="2d258-122">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d258-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2d258-123">출력</span><span class="sxs-lookup"><span data-stu-id="2d258-123">OUTPUTS</span></span>

### <span data-ttu-id="2d258-124">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2d258-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="2d258-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2d258-125">NOTES</span></span>

## <span data-ttu-id="2d258-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d258-126">RELATED LINKS</span></span>

[<span data-ttu-id="2d258-127">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d258-127">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2d258-128">새로운 AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d258-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="2d258-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d258-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


