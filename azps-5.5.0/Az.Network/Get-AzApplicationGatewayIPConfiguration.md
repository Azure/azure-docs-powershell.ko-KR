---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184769"
---
# <span data-ttu-id="5da2f-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5da2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da2f-102">SYNOPSIS</span></span>
<span data-ttu-id="5da2f-103">애플리케이션 게이트웨이의 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="5da2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5da2f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da2f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5da2f-105">DESCRIPTION</span></span>
<span data-ttu-id="5da2f-106">**Get-AzApplicationGatewayIPConfiguration** cmdlet은 애플리케이션 게이트웨이의 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="5da2f-107">IP 구성에는 애플리케이션 게이트웨이가 배포된 서브넷이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="5da2f-108">예제</span><span class="sxs-lookup"><span data-stu-id="5da2f-108">EXAMPLES</span></span>

### <span data-ttu-id="5da2f-109">예제 1: 특정 IP 구성을 갖기</span><span class="sxs-lookup"><span data-stu-id="5da2f-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="5da2f-110">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 게이트웨이에 저장된 게이트웨이에서 GateSubnet01이라는 IP 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5da2f-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="5da2f-111">예제 2: IP 구성 목록 확인</span><span class="sxs-lookup"><span data-stu-id="5da2f-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="5da2f-112">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 모든 IP 구성의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="5da2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da2f-113">PARAMETERS</span></span>

### <span data-ttu-id="5da2f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da2f-114">-ApplicationGateway</span></span>
<span data-ttu-id="5da2f-115">IP 구성을 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="5da2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da2f-116">-DefaultProfile</span></span>
<span data-ttu-id="5da2f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da2f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5da2f-118">-Name</span></span>
<span data-ttu-id="5da2f-119">이 cmdlet이 얻을 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="5da2f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da2f-120">CommonParameters</span></span>
<span data-ttu-id="5da2f-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5da2f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da2f-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5da2f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da2f-123">입력</span><span class="sxs-lookup"><span data-stu-id="5da2f-123">INPUTS</span></span>

### <span data-ttu-id="5da2f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da2f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5da2f-125">출력</span><span class="sxs-lookup"><span data-stu-id="5da2f-125">OUTPUTS</span></span>

### <span data-ttu-id="5da2f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5da2f-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5da2f-127">NOTES</span></span>

## <span data-ttu-id="5da2f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5da2f-128">RELATED LINKS</span></span>

[<span data-ttu-id="5da2f-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5da2f-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5da2f-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5da2f-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da2f-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


