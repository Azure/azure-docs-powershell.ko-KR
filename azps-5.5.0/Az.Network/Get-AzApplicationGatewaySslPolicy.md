---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192001"
---
# <span data-ttu-id="5942f-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5942f-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5942f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5942f-102">SYNOPSIS</span></span>
<span data-ttu-id="5942f-103">애플리케이션 게이트웨이의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5942f-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5942f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5942f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5942f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5942f-105">DESCRIPTION</span></span>
<span data-ttu-id="5942f-106">**Get-AzApplicationGatewaySslPolicy** cmdlet은 애플리케이션 게이트웨이의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5942f-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5942f-107">예제</span><span class="sxs-lookup"><span data-stu-id="5942f-107">EXAMPLES</span></span>

### <span data-ttu-id="5942f-108">1:</span><span class="sxs-lookup"><span data-stu-id="5942f-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="5942f-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 해당 애플리케이션이라는 변수에 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5942f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5942f-110">두 번째 명령은 애플리케이션이라는 변수에 저장된 Application Gateway에서 ssl 정책을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5942f-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="5942f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5942f-111">PARAMETERS</span></span>

### <span data-ttu-id="5942f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5942f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5942f-113">이 cmdlet에서 얻을 SSL 정책의 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5942f-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5942f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5942f-114">-DefaultProfile</span></span>
<span data-ttu-id="5942f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5942f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5942f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5942f-116">CommonParameters</span></span>
<span data-ttu-id="5942f-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5942f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5942f-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5942f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5942f-119">입력</span><span class="sxs-lookup"><span data-stu-id="5942f-119">INPUTS</span></span>

### <span data-ttu-id="5942f-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5942f-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5942f-121">출력</span><span class="sxs-lookup"><span data-stu-id="5942f-121">OUTPUTS</span></span>

### <span data-ttu-id="5942f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5942f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5942f-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5942f-123">NOTES</span></span>
* <span data-ttu-id="5942f-124">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="5942f-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5942f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5942f-125">RELATED LINKS</span></span>

[<span data-ttu-id="5942f-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5942f-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5942f-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5942f-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


