---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191881"
---
# <span data-ttu-id="fed9e-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fed9e-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="fed9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed9e-102">SYNOPSIS</span></span>
<span data-ttu-id="fed9e-103">ExpressRoute 회로에 추가할 새 피어링 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="fed9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="fed9e-104">SYNTAX</span></span>

### <span data-ttu-id="fed9e-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="fed9e-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed9e-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="fed9e-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed9e-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="fed9e-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed9e-108">설명</span><span class="sxs-lookup"><span data-stu-id="fed9e-108">DESCRIPTION</span></span>
<span data-ttu-id="fed9e-109">**New-AzExpressRouteCircuitPeeringConfig** cmdlet은 ExpressRoute 회로에 피어링 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="fed9e-110">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="fed9e-111">예제</span><span class="sxs-lookup"><span data-stu-id="fed9e-111">EXAMPLES</span></span>

### <span data-ttu-id="fed9e-112">예제 1: 피어링 구성을 사용하여 새 ExpressRoute 회로 만들기</span><span class="sxs-lookup"><span data-stu-id="fed9e-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="fed9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed9e-113">PARAMETERS</span></span>

### <span data-ttu-id="fed9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed9e-114">-DefaultProfile</span></span>
<span data-ttu-id="fed9e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed9e-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="fed9e-116">-LegacyMode</span></span>
<span data-ttu-id="fed9e-117">피어링의 레거시 모드</span><span class="sxs-lookup"><span data-stu-id="fed9e-117">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="fed9e-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="fed9e-119">MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전의 목록을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="fed9e-120">공용 IP 주소 연결만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="fed9e-121">콤마로 구분된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="fed9e-122">이러한 사전은 RIR/IRR(라우팅 레지스트리 이름)에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="fed9e-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="fed9e-124">피어링 AS 번호에 등록되지 않은 광고의 경우 등록할 AS 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="fed9e-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="fed9e-126">AS 번호 및 prefix가 등록되는 RIR/IRR(라우팅 레지스트리 이름)</span><span class="sxs-lookup"><span data-stu-id="fed9e-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="fed9e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fed9e-127">-Name</span></span>
<span data-ttu-id="fed9e-128">만들 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="fed9e-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="fed9e-129">-PeerAddressType</span></span>
<span data-ttu-id="fed9e-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="fed9e-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="fed9e-131">-PeerASN</span></span>
<span data-ttu-id="fed9e-132">ExpressRoute 회로의 AS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="fed9e-133">PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="fed9e-134">-PeeringType</span></span>
<span data-ttu-id="fed9e-135">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="fed9e-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fed9e-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="fed9e-137">이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="fed9e-138">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="fed9e-139">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="fed9e-140">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="fed9e-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="fed9e-141">-RouteFilter</span></span>
<span data-ttu-id="fed9e-142">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="fed9e-143">-RouteFilterId</span></span>
<span data-ttu-id="fed9e-144">기존 RouteFilter 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fed9e-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="fed9e-146">이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="fed9e-147">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="fed9e-148">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="fed9e-149">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="fed9e-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="fed9e-150">-SharedKey</span></span>
<span data-ttu-id="fed9e-151">피어링 구성에 대한 미리 공유된 키로 사용되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="fed9e-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="fed9e-152">-VlanId</span></span>
<span data-ttu-id="fed9e-153">이 피어링에 할당된 VLAN의 ID 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed9e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed9e-154">CommonParameters</span></span>
<span data-ttu-id="fed9e-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fed9e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed9e-156">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fed9e-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed9e-157">입력</span><span class="sxs-lookup"><span data-stu-id="fed9e-157">INPUTS</span></span>

### <span data-ttu-id="fed9e-158">System.String</span><span class="sxs-lookup"><span data-stu-id="fed9e-158">System.String</span></span>

### <span data-ttu-id="fed9e-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fed9e-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="fed9e-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fed9e-160">System.Boolean</span></span>

## <span data-ttu-id="fed9e-161">출력</span><span class="sxs-lookup"><span data-stu-id="fed9e-161">OUTPUTS</span></span>

### <span data-ttu-id="fed9e-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="fed9e-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="fed9e-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fed9e-163">NOTES</span></span>

## <span data-ttu-id="fed9e-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fed9e-164">RELATED LINKS</span></span>

[<span data-ttu-id="fed9e-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fed9e-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="fed9e-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fed9e-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="fed9e-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fed9e-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="fed9e-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fed9e-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
