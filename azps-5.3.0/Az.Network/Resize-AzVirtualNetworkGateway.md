---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496548"
---
# <span data-ttu-id="678b6-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="678b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678b6-102">SYNOPSIS</span></span>
<span data-ttu-id="678b6-103">기존 가상 네트워크 게이트웨이의 수를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="678b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="678b6-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678b6-105">설명</span><span class="sxs-lookup"><span data-stu-id="678b6-105">DESCRIPTION</span></span>
<span data-ttu-id="678b6-106">**Resize-AzVirtualNetworkGateway** cmdlet을 사용하면 가상 네트워크 게이트웨이에 대한 SKU(Stock Keeping Unit)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="678b6-107">SKUS는 허용되는 최대 IP 터널 수 및 같은 것을 포함하여 게이트웨이의 기능을 파악합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="678b6-108">Azure는 Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUS(Small, Medium 및 Large SKUS라고도 합니다)를 지원</span><span class="sxs-lookup"><span data-stu-id="678b6-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="678b6-109">각 SKU 유형의 기능에 대한 자세한 내용은 다음을 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="678b6-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="678b6-110">SKUS는 가격 책정 및 기능도 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="678b6-111">자세한 내용은 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="678b6-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="678b6-112">예제</span><span class="sxs-lookup"><span data-stu-id="678b6-112">EXAMPLES</span></span>

### <span data-ttu-id="678b6-113">예제 1: 가상 네트워크 게이트웨이의 크기 변경</span><span class="sxs-lookup"><span data-stu-id="678b6-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="678b6-114">이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이의 크기를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="678b6-115">첫 번째 명령은 ContosoVirtualGateway에 대한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway.</span><span class="sxs-lookup"><span data-stu-id="678b6-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="678b6-116">두 번째 명령은 **Resize-AzVirtualNetworkGateway** cmdlet을 사용하여 *GatewaySku* 속성을 Basic으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="678b6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="678b6-117">PARAMETERS</span></span>

### <span data-ttu-id="678b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678b6-118">-DefaultProfile</span></span>
<span data-ttu-id="678b6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="678b6-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="678b6-120">-GatewaySku</span></span>
<span data-ttu-id="678b6-121">새 유형의 게이트웨이 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="678b6-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="678b6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="678b6-123">기본</span><span class="sxs-lookup"><span data-stu-id="678b6-123">Basic</span></span>
- <span data-ttu-id="678b6-124">표준</span><span class="sxs-lookup"><span data-stu-id="678b6-124">Standard</span></span>
- <span data-ttu-id="678b6-125">고성능</span><span class="sxs-lookup"><span data-stu-id="678b6-125">High Performance</span></span>
- <span data-ttu-id="678b6-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="678b6-126">VpnGw1</span></span>
- <span data-ttu-id="678b6-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="678b6-127">VpnGw2</span></span>
- <span data-ttu-id="678b6-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="678b6-128">VpnGw3</span></span>
- <span data-ttu-id="678b6-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="678b6-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="678b6-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="678b6-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-132">ErGw1AZ</span></span> 
- <span data-ttu-id="678b6-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-133">ErGw2AZ</span></span> 
- <span data-ttu-id="678b6-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="678b6-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678b6-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="678b6-136">변경될 가상 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="678b6-137">이 개체 참조는 Get-AzVirtualNetworkGateway 게이트웨이의 이름을 지정하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678b6-138">CommonParameters</span></span>
<span data-ttu-id="678b6-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678b6-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="678b6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678b6-141">입력</span><span class="sxs-lookup"><span data-stu-id="678b6-141">INPUTS</span></span>

### <span data-ttu-id="678b6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="678b6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="678b6-143">System.String</span></span>

## <span data-ttu-id="678b6-144">출력</span><span class="sxs-lookup"><span data-stu-id="678b6-144">OUTPUTS</span></span>

### <span data-ttu-id="678b6-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="678b6-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="678b6-146">NOTES</span></span>
<span data-ttu-id="678b6-147">Basic/Standard/HighPerformance SKUS에서 새 VpnGw1/VpnGw2/VpnGw3 SKUS로는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="678b6-148">VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 또는 ErGw1AZ/ErGw2AZ/ErGw2AZ/ErGw3AZ에서/VpnGw3AZ로/에 대한 추가적 재조정은 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="678b6-149">SKU '시리즈' 내에서만 허용됩니다. 예: VpnGw1AZ는 VpnGw2AZ/VpnGw3AZ에서 또는 VpnGw3AZ에서, ErGw1AZ는 ErGw2AZ/ErGw3AZ에서 또는 그에 대한/ErGw3AZ로 또는 그 범위에서 ErGw1AZ로 또는 그에 대한/ErGw3AZ로 또는 그에 대한/ErGw1AZ로 또는 그에 대한 또는 그에 대한 재조정을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="678b6-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="678b6-150">지침을 https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="678b6-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="678b6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="678b6-151">RELATED LINKS</span></span>

[<span data-ttu-id="678b6-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="678b6-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="678b6-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="678b6-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="678b6-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="678b6-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="678b6-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="678b6-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="678b6-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="678b6-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
