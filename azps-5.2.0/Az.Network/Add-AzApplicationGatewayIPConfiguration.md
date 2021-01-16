---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329139"
---
# <span data-ttu-id="e2f1f-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1f-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e2f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f1f-103">애플리케이션 게이트웨이에 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="e2f1f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2f1f-104">SYNTAX</span></span>

### <span data-ttu-id="e2f1f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f1f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2f1f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2f1f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2f1f-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="e2f1f-108">**Add-AzApplicationGatewayIPConfiguration** cmdlet은 애플리케이션 게이트웨이에 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="e2f1f-109">IP 구성에는 애플리케이션 게이트웨이가 배포된 서브넷이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="e2f1f-110">예제</span><span class="sxs-lookup"><span data-stu-id="e2f1f-110">EXAMPLES</span></span>

### <span data-ttu-id="e2f1f-111">예제 1: 애플리케이션 게이트웨이에 가상 네트워크 구성 추가</span><span class="sxs-lookup"><span data-stu-id="e2f1f-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="e2f1f-112">첫 번째 명령은 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="e2f1f-113">두 번째 명령은 이전에 만든 가상 네트워크를 사용하여 서브넷을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="e2f1f-114">세 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2f1f-115">네 번째 명령은 애플리케이션 게이트웨이에 저장된 애플리케이션 게이트웨이에 IP 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e2f1f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2f1f-116">PARAMETERS</span></span>

### <span data-ttu-id="e2f1f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2f1f-117">-ApplicationGateway</span></span>
<span data-ttu-id="e2f1f-118">이 cmdlet이 IP 구성을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="e2f1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f1f-119">-DefaultProfile</span></span>
<span data-ttu-id="e2f1f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2f1f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2f1f-121">-Name</span></span>
<span data-ttu-id="e2f1f-122">추가할 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="e2f1f-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e2f1f-123">-Subnet</span></span>
<span data-ttu-id="e2f1f-124">서브넷을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-124">Specifies a subnet.</span></span>
<span data-ttu-id="e2f1f-125">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e2f1f-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e2f1f-126">-SubnetId</span></span>
<span data-ttu-id="e2f1f-127">서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="e2f1f-128">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e2f1f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f1f-129">CommonParameters</span></span>
<span data-ttu-id="e2f1f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f1f-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f1f-132">입력</span><span class="sxs-lookup"><span data-stu-id="e2f1f-132">INPUTS</span></span>

### <span data-ttu-id="e2f1f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2f1f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2f1f-134">출력</span><span class="sxs-lookup"><span data-stu-id="e2f1f-134">OUTPUTS</span></span>

### <span data-ttu-id="e2f1f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2f1f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2f1f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2f1f-136">NOTES</span></span>

## <span data-ttu-id="e2f1f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2f1f-137">RELATED LINKS</span></span>

[<span data-ttu-id="e2f1f-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1f-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e2f1f-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1f-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e2f1f-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1f-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e2f1f-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1f-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


