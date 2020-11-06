---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535712"
---
# <span data-ttu-id="6af50-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6af50-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6af50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af50-102">SYNOPSIS</span></span>
<span data-ttu-id="6af50-103">기존 가상 네트워크 게이트웨이의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6af50-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6af50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6af50-105">DESCRIPTION</span></span>
<span data-ttu-id="6af50-106">**크기 조정-AzureRmVirtualNetworkGateway** cmdlet을 사용 하 여 가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="6af50-107">Sku는 처리량, 허용 되는 최대 IP 터널 수 등의 게이트웨이 기능을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="6af50-108">Azure는 Basic, Standard, 고성능, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ Sku (간혹 소형, 중형, 대형 Sku 라고도 함)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="6af50-109">각 SKU 유형의 기능에 대 한 자세한 내용은을 참조 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af50-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="6af50-110">Sku는 가격 및 기능에 차이가 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af50-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="6af50-111">자세한 내용은을 참조 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af50-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="6af50-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6af50-112">EXAMPLES</span></span>

### <span data-ttu-id="6af50-113">예제 1: 가상 네트워크 게이트웨이의 크기 변경</span><span class="sxs-lookup"><span data-stu-id="6af50-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="6af50-114">이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이의 크기를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="6af50-115">첫 번째 명령은 ContosoVirtualGateway에 대 한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="6af50-116">그런 다음 두 번째 명령은 **AzureRmVirtualNetworkGateway** cmdlet을 사용 하 여 하이 *속성을* Basic으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="6af50-117">변수</span><span class="sxs-lookup"><span data-stu-id="6af50-117">PARAMETERS</span></span>

### <span data-ttu-id="6af50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af50-118">-DefaultProfile</span></span>
<span data-ttu-id="6af50-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6af50-120">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="6af50-120">-GatewaySku</span></span>
<span data-ttu-id="6af50-121">게이트웨이 SKU의 새로운 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="6af50-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6af50-123">기본적</span><span class="sxs-lookup"><span data-stu-id="6af50-123">Basic</span></span>
- <span data-ttu-id="6af50-124">표준이</span><span class="sxs-lookup"><span data-stu-id="6af50-124">Standard</span></span>
- <span data-ttu-id="6af50-125">고성능</span><span class="sxs-lookup"><span data-stu-id="6af50-125">High Performance</span></span>
- <span data-ttu-id="6af50-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="6af50-126">VpnGw1</span></span>
- <span data-ttu-id="6af50-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="6af50-127">VpnGw2</span></span>
- <span data-ttu-id="6af50-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="6af50-128">VpnGw3</span></span>
- <span data-ttu-id="6af50-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="6af50-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="6af50-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="6af50-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-132">ErGw1AZ</span></span> 
- <span data-ttu-id="6af50-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-133">ErGw2AZ</span></span> 
- <span data-ttu-id="6af50-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="6af50-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="6af50-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6af50-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="6af50-136">크기를 조정할 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="6af50-137">Get-AzureRmVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여이 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="6af50-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af50-138">CommonParameters</span></span>
<span data-ttu-id="6af50-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af50-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af50-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af50-141">입력</span><span class="sxs-lookup"><span data-stu-id="6af50-141">INPUTS</span></span>

### <span data-ttu-id="6af50-142">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6af50-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="6af50-143">매개 변수: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6af50-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="6af50-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6af50-144">System.String</span></span>

## <span data-ttu-id="6af50-145">출력</span><span class="sxs-lookup"><span data-stu-id="6af50-145">OUTPUTS</span></span>

### <span data-ttu-id="6af50-146">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6af50-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6af50-147">상속자</span><span class="sxs-lookup"><span data-stu-id="6af50-147">NOTES</span></span>
<span data-ttu-id="6af50-148">기본/표준/HighPerformance Sku에서 new VpnGw1/VpnGw2/VpnGw3 Sku로 크기를 조정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="6af50-149">VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 또는 ErGw1AZ/ErGw2AZ/ErGw3AZ에는 추가 크기 조정이 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="6af50-150">크기 조정에는 SKU ' 계열 '에만 사용할 수 있습니다. 예를 들어 VpnGw1AZ에서 VpnGw2AZ/VpnGw3AZ로 크기를 조정 하거나 ErGw1AZ에서 ErGw2AZ/ErGw3AZ로 크기를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6af50-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="6af50-151"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways지침은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af50-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="6af50-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6af50-152">RELATED LINKS</span></span>

[<span data-ttu-id="6af50-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="6af50-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="6af50-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6af50-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="6af50-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="6af50-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


