---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882829"
---
# <span data-ttu-id="c7f04-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7f04-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="c7f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f04-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f04-103">기존 가상 네트워크 게이트웨이의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7f04-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7f04-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f04-106">**크기 조정-AzureRmVirtualNetworkGateway** cmdlet을 사용 하 여 가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="c7f04-107">Sku는 처리량, 허용 되는 최대 IP 터널 수 등의 게이트웨이 기능을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="c7f04-108">Azure는 기본, 표준, 고성능, VpnGw1, VpnGw2 및 VpnGw3 Sku (간혹 소형, 중형, 대형 Sku 라고도 함)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="c7f04-109">각 SKU 유형의 기능에 대 한 자세한 내용은을 참조 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f04-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="c7f04-110">Sku는 가격 및 기능에 차이가 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f04-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="c7f04-111">자세한 내용은을 참조 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f04-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="c7f04-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c7f04-112">EXAMPLES</span></span>

### <span data-ttu-id="c7f04-113">예제 1: 가상 네트워크 게이트웨이의 크기 변경</span><span class="sxs-lookup"><span data-stu-id="c7f04-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="c7f04-114">이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이의 크기를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="c7f04-115">첫 번째 명령은 ContosoVirtualGateway에 대 한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="c7f04-116">그런 다음 두 번째 명령은 **AzureRmVirtualNetworkGateway** cmdlet을 사용 하 여 하이 *속성을* Basic으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="c7f04-117">변수</span><span class="sxs-lookup"><span data-stu-id="c7f04-117">PARAMETERS</span></span>

### <span data-ttu-id="c7f04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f04-118">-DefaultProfile</span></span>
<span data-ttu-id="c7f04-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f04-120">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="c7f04-120">-GatewaySku</span></span>
<span data-ttu-id="c7f04-121">게이트웨이 SKU의 새로운 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="c7f04-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7f04-123">기본적</span><span class="sxs-lookup"><span data-stu-id="c7f04-123">Basic</span></span>
- <span data-ttu-id="c7f04-124">표준이</span><span class="sxs-lookup"><span data-stu-id="c7f04-124">Standard</span></span>
- <span data-ttu-id="c7f04-125">고성능</span><span class="sxs-lookup"><span data-stu-id="c7f04-125">High Performance</span></span>
- <span data-ttu-id="c7f04-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c7f04-126">VpnGw1</span></span>
- <span data-ttu-id="c7f04-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c7f04-127">VpnGw2</span></span>
- <span data-ttu-id="c7f04-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c7f04-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f04-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7f04-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c7f04-130">크기를 조정할 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="c7f04-131">Get-AzureRmVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여이 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f04-132">CommonParameters</span></span>
<span data-ttu-id="c7f04-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f04-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f04-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f04-135">입력</span><span class="sxs-lookup"><span data-stu-id="c7f04-135">INPUTS</span></span>

###  
<span data-ttu-id="c7f04-136">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="c7f04-137">출력</span><span class="sxs-lookup"><span data-stu-id="c7f04-137">OUTPUTS</span></span>

###  
<span data-ttu-id="c7f04-138">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 기존 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="c7f04-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c7f04-139">NOTES</span></span>
<span data-ttu-id="c7f04-140">기본/표준/HighPerformance Sku에서 new VpnGw1/VpnGw2/VpnGw3 Sku로 크기를 조정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f04-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="c7f04-141"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways지침은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7f04-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="c7f04-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7f04-142">RELATED LINKS</span></span>

[<span data-ttu-id="c7f04-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="c7f04-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="c7f04-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7f04-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c7f04-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="c7f04-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


