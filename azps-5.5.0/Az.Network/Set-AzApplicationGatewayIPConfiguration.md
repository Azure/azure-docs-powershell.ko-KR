---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193401"
---
# <span data-ttu-id="92a01-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="92a01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a01-102">SYNOPSIS</span></span>
<span data-ttu-id="92a01-103">애플리케이션 게이트웨이에 대한 IP 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="92a01-104">구문</span><span class="sxs-lookup"><span data-stu-id="92a01-104">SYNTAX</span></span>

### <span data-ttu-id="92a01-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="92a01-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92a01-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="92a01-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92a01-107">설명</span><span class="sxs-lookup"><span data-stu-id="92a01-107">DESCRIPTION</span></span>
<span data-ttu-id="92a01-108">**Set-AzApplicationGatewayIPConfiguration** cmdlet은 IP 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="92a01-109">IP 구성에는 애플리케이션 게이트웨이가 배포되는 서브넷이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="92a01-110">예제</span><span class="sxs-lookup"><span data-stu-id="92a01-110">EXAMPLES</span></span>

### <span data-ttu-id="92a01-111">예제 1: 애플리케이션 게이트웨이에 대한 IP 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="92a01-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="92a01-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="92a01-113">두 번째 명령은 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="92a01-114">세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="92a01-115">첫 번째 명령은 애플리케이션에 저장된 애플리케이션 게이트웨이의 IP 구성을 $AppGw 서브넷 구성에 $Subnet.</span><span class="sxs-lookup"><span data-stu-id="92a01-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="92a01-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a01-116">PARAMETERS</span></span>

### <span data-ttu-id="92a01-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92a01-117">-ApplicationGateway</span></span>
<span data-ttu-id="92a01-118">이 cmdlet이 IP 구성을 연결한 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="92a01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a01-119">-DefaultProfile</span></span>
<span data-ttu-id="92a01-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92a01-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92a01-121">-Name</span></span>
<span data-ttu-id="92a01-122">IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="92a01-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="92a01-123">-Subnet</span></span>
<span data-ttu-id="92a01-124">서브넷을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-124">Specifies the subnet.</span></span>
<span data-ttu-id="92a01-125">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="92a01-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="92a01-126">-SubnetId</span></span>
<span data-ttu-id="92a01-127">서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="92a01-128">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="92a01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a01-129">CommonParameters</span></span>
<span data-ttu-id="92a01-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92a01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a01-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="92a01-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a01-132">입력</span><span class="sxs-lookup"><span data-stu-id="92a01-132">INPUTS</span></span>

### <span data-ttu-id="92a01-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92a01-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92a01-134">출력</span><span class="sxs-lookup"><span data-stu-id="92a01-134">OUTPUTS</span></span>

### <span data-ttu-id="92a01-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92a01-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92a01-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92a01-136">NOTES</span></span>

## <span data-ttu-id="92a01-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92a01-137">RELATED LINKS</span></span>

[<span data-ttu-id="92a01-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="92a01-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="92a01-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="92a01-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="92a01-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a01-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


