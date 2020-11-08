---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c4c3abf1eeb387c700bb456b50887fdc9dd41c74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044749"
---
# <span data-ttu-id="b83b0-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b83b0-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b83b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b83b0-103">이 (가) Express 회로에 추가할 새 피어 링 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b83b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b83b0-104">SYNTAX</span></span>

### <span data-ttu-id="b83b0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b83b0-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b83b0-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b83b0-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b83b0-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b83b0-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b83b0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b83b0-108">DESCRIPTION</span></span>
<span data-ttu-id="b83b0-109">**AzExpressRouteCircuitPeeringConfig** cmdlet은 대상 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="b83b0-110">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="b83b0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b83b0-111">EXAMPLES</span></span>

### <span data-ttu-id="b83b0-112">예제 1: 피어 링 구성을 사용 하 여 새 Express 경로 만들기 회로</span><span class="sxs-lookup"><span data-stu-id="b83b0-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
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

## <span data-ttu-id="b83b0-113">변수</span><span class="sxs-lookup"><span data-stu-id="b83b0-113">PARAMETERS</span></span>

### <span data-ttu-id="b83b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83b0-114">-DefaultProfile</span></span>
<span data-ttu-id="b83b0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83b0-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="b83b0-116">-LegacyMode</span></span>
<span data-ttu-id="b83b0-117">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="b83b0-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b83b0-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b83b0-119">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b83b0-120">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b83b0-121">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b83b0-122">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="b83b0-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b83b0-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b83b0-124">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="b83b0-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b83b0-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b83b0-126">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b83b0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="b83b0-127">-Name</span></span>
<span data-ttu-id="b83b0-128">만들려는 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="b83b0-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b83b0-129">-PeerAddressType</span></span>
<span data-ttu-id="b83b0-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b83b0-130">PeerAddressType</span></span>

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

### <span data-ttu-id="b83b0-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b83b0-131">-PeerASN</span></span>
<span data-ttu-id="b83b0-132">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b83b0-133">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="b83b0-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b83b0-134">-PeeringType</span></span>
<span data-ttu-id="b83b0-135">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b83b0-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b83b0-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b83b0-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b83b0-137">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b83b0-138">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b83b0-139">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b83b0-140">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b83b0-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b83b0-141">-RouteFilter</span></span>
<span data-ttu-id="b83b0-142">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b83b0-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b83b0-143">-RouteFilterId</span></span>
<span data-ttu-id="b83b0-144">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b83b0-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b83b0-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b83b0-146">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b83b0-147">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b83b0-148">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b83b0-149">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b83b0-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b83b0-150">-SharedKey</span></span>
<span data-ttu-id="b83b0-151">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b83b0-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="b83b0-152">-VlanId</span></span>
<span data-ttu-id="b83b0-153">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="b83b0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83b0-154">CommonParameters</span></span>
<span data-ttu-id="b83b0-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b83b0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83b0-156">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83b0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83b0-157">입력</span><span class="sxs-lookup"><span data-stu-id="b83b0-157">INPUTS</span></span>

### <span data-ttu-id="b83b0-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b83b0-158">System.String</span></span>

### <span data-ttu-id="b83b0-159">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b83b0-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="b83b0-160">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b83b0-160">System.Boolean</span></span>

## <span data-ttu-id="b83b0-161">출력</span><span class="sxs-lookup"><span data-stu-id="b83b0-161">OUTPUTS</span></span>

### <span data-ttu-id="b83b0-162">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b83b0-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="b83b0-163">상속자</span><span class="sxs-lookup"><span data-stu-id="b83b0-163">NOTES</span></span>

## <span data-ttu-id="b83b0-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b83b0-164">RELATED LINKS</span></span>

[<span data-ttu-id="b83b0-165">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b83b0-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b83b0-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b83b0-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b83b0-167">제거-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b83b0-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b83b0-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b83b0-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
