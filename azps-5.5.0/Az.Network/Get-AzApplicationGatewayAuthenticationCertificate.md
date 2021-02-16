---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 00d5d84f3f9895aec42f9728de6eec1bf2ff9b06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189921"
---
# <span data-ttu-id="5f9fa-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5f9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9fa-103">애플리케이션 게이트웨이에 대한 인증 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5f9fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f9fa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f9fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="5f9fa-106">**Get-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 인증 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5f9fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="5f9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="5f9fa-108">예제 1: 지정된 인증 인증서를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="5f9fa-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="5f9fa-110">두 번째 명령은 cert01이라는 인증 인증서를 사용하여 $cert 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="5f9fa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f9fa-111">PARAMETERS</span></span>

### <span data-ttu-id="5f9fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f9fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="5f9fa-113">이 cmdlet이 인증 인증서를 받을 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="5f9fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9fa-114">-DefaultProfile</span></span>
<span data-ttu-id="5f9fa-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f9fa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5f9fa-116">-Name</span></span>
<span data-ttu-id="5f9fa-117">이 cmdlet에서 얻을 인증 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f9fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9fa-118">CommonParameters</span></span>
<span data-ttu-id="5f9fa-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9fa-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f9fa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9fa-121">입력</span><span class="sxs-lookup"><span data-stu-id="5f9fa-121">INPUTS</span></span>

### <span data-ttu-id="5f9fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f9fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f9fa-123">출력</span><span class="sxs-lookup"><span data-stu-id="5f9fa-123">OUTPUTS</span></span>

### <span data-ttu-id="5f9fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5f9fa-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f9fa-125">NOTES</span></span>
* <span data-ttu-id="5f9fa-126">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="5f9fa-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5f9fa-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f9fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f9fa-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f9fa-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f9fa-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5f9fa-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f9fa-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


