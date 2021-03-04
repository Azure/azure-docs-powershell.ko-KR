---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 17661a05a970a9661543220c35b122638ddbc524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982619"
---
# <span data-ttu-id="c84d1-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84d1-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c84d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c84d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c84d1-103">애플리케이션 게이트웨이에 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="c84d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c84d1-104">SYNTAX</span></span>

### <span data-ttu-id="c84d1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d1-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c84d1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c84d1-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c84d1-107">설명</span><span class="sxs-lookup"><span data-stu-id="c84d1-107">DESCRIPTION</span></span>
<span data-ttu-id="c84d1-108">**Add-AzApplicationGatewayIPConfiguration** cmdlet은 애플리케이션 게이트웨이에 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="c84d1-109">IP 구성에는 애플리케이션 게이트웨이가 배포되는 서브넷이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="c84d1-110">예제</span><span class="sxs-lookup"><span data-stu-id="c84d1-110">EXAMPLES</span></span>

### <span data-ttu-id="c84d1-111">예제 1: 애플리케이션 게이트웨이에 가상 네트워크 구성 추가</span><span class="sxs-lookup"><span data-stu-id="c84d1-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="c84d1-112">첫 번째 명령은 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="c84d1-113">두 번째 명령은 이전에 만든 가상 네트워크를 사용하여 서브넷을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="c84d1-114">세 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c84d1-115">네 번째 명령은 에 저장된 애플리케이션 게이트웨이에 IP 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c84d1-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c84d1-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c84d1-116">PARAMETERS</span></span>

### <span data-ttu-id="c84d1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c84d1-117">-ApplicationGateway</span></span>
<span data-ttu-id="c84d1-118">이 cmdlet에서 IP 구성을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="c84d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84d1-119">-DefaultProfile</span></span>
<span data-ttu-id="c84d1-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c84d1-121">-Name</span></span>
<span data-ttu-id="c84d1-122">추가할 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="c84d1-123">-서브넷</span><span class="sxs-lookup"><span data-stu-id="c84d1-123">-Subnet</span></span>
<span data-ttu-id="c84d1-124">서브넷을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-124">Specifies a subnet.</span></span>
<span data-ttu-id="c84d1-125">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84d1-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c84d1-126">-SubnetId</span></span>
<span data-ttu-id="c84d1-127">서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="c84d1-128">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c84d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84d1-129">CommonParameters</span></span>
<span data-ttu-id="c84d1-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c84d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84d1-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c84d1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84d1-132">입력</span><span class="sxs-lookup"><span data-stu-id="c84d1-132">INPUTS</span></span>

### <span data-ttu-id="c84d1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c84d1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c84d1-134">출력</span><span class="sxs-lookup"><span data-stu-id="c84d1-134">OUTPUTS</span></span>

### <span data-ttu-id="c84d1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c84d1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c84d1-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c84d1-136">NOTES</span></span>

## <span data-ttu-id="c84d1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c84d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="c84d1-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84d1-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c84d1-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84d1-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c84d1-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84d1-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c84d1-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84d1-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


