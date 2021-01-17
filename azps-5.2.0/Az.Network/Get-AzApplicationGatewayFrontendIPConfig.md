---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326325"
---
# <span data-ttu-id="bfc3a-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bfc3a-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="bfc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc3a-103">애플리케이션 게이트웨이의 프런트 엔드 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="bfc3a-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfc3a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc3a-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc3a-106">**Get-AzApplicationGatewayFrontendIPConfig** cmdlet은 애플리케이션 게이트웨이의 프런트 엔드 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="bfc3a-107">예제</span><span class="sxs-lookup"><span data-stu-id="bfc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc3a-108">예제 1: 지정된 프런트 엔드 IP 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="bfc3a-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 프런트 엔드 IP 구성인 FrontEndIP01을 $AppGw 변수에 $FrontEndIP 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="bfc3a-110">예제 2: 프런트 엔드 IP 구성 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="bfc3a-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="bfc3a-111">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 프런트 엔드 IP 구성의 목록을 $AppGw 변수에 $FrontEndIPs 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="bfc3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfc3a-112">PARAMETERS</span></span>

### <span data-ttu-id="bfc3a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfc3a-113">-ApplicationGateway</span></span>
<span data-ttu-id="bfc3a-114">프런트 엔드 IP 구성을 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="bfc3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc3a-115">-DefaultProfile</span></span>
<span data-ttu-id="bfc3a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc3a-117">-Name</span></span>
<span data-ttu-id="bfc3a-118">이 cmdlet에서 얻을 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc3a-119">CommonParameters</span></span>
<span data-ttu-id="bfc3a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc3a-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfc3a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc3a-122">입력</span><span class="sxs-lookup"><span data-stu-id="bfc3a-122">INPUTS</span></span>

### <span data-ttu-id="bfc3a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfc3a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfc3a-124">출력</span><span class="sxs-lookup"><span data-stu-id="bfc3a-124">OUTPUTS</span></span>

### <span data-ttu-id="bfc3a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfc3a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="bfc3a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfc3a-126">NOTES</span></span>

## <span data-ttu-id="bfc3a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfc3a-127">RELATED LINKS</span></span>

[<span data-ttu-id="bfc3a-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bfc3a-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bfc3a-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bfc3a-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bfc3a-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bfc3a-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="bfc3a-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bfc3a-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


