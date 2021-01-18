---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495145"
---
# <span data-ttu-id="93d4f-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="93d4f-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="93d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="93d4f-103">수정된 ExpressRoute 피어링 구성을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="93d4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="93d4f-104">SYNTAX</span></span>

### <span data-ttu-id="93d4f-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="93d4f-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d4f-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="93d4f-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d4f-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="93d4f-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93d4f-108">설명</span><span class="sxs-lookup"><span data-stu-id="93d4f-108">DESCRIPTION</span></span>
<span data-ttu-id="93d4f-109">**Set-AzExpressRouteCircuitPeeringConfig** cmdlet은 수정된 ExpressRoute 피어링 구성을 다시 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="93d4f-110">예제</span><span class="sxs-lookup"><span data-stu-id="93d4f-110">EXAMPLES</span></span>

### <span data-ttu-id="93d4f-111">예제 1: 기존 피어링 구성 변경</span><span class="sxs-lookup"><span data-stu-id="93d4f-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="93d4f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="93d4f-112">Example 2</span></span>

<span data-ttu-id="93d4f-113">수정된 ExpressRoute 피어링 구성을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="93d4f-114">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="93d4f-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="93d4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93d4f-115">PARAMETERS</span></span>

### <span data-ttu-id="93d4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d4f-116">-DefaultProfile</span></span>
<span data-ttu-id="93d4f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d4f-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="93d4f-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="93d4f-119">수정할 피어링 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d4f-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="93d4f-120">-LegacyMode</span></span>
<span data-ttu-id="93d4f-121">피어링의 레거시 모드</span><span class="sxs-lookup"><span data-stu-id="93d4f-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="93d4f-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="93d4f-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="93d4f-123">MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전의 목록을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="93d4f-124">공용 IP 주소 연결만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="93d4f-125">콤마로 구분된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="93d4f-126">이러한 사전은 RIR/IRR(라우팅 레지스트리 이름)에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="93d4f-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="93d4f-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="93d4f-128">피어링 AS 번호에 등록되지 않은 광고의 경우 등록할 AS 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="93d4f-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="93d4f-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="93d4f-130">AS 번호 및 prefix가 등록되는 RIR/IRR(라우팅 레지스트리 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="93d4f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="93d4f-131">-Name</span></span>
<span data-ttu-id="93d4f-132">수정할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="93d4f-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="93d4f-133">-PeerAddressType</span></span>
<span data-ttu-id="93d4f-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="93d4f-134">PeerAddressType</span></span>

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

### <span data-ttu-id="93d4f-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="93d4f-135">-PeerASN</span></span>
<span data-ttu-id="93d4f-136">ExpressRoute 회로의 AS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="93d4f-137">PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="93d4f-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="93d4f-138">-PeeringType</span></span>
<span data-ttu-id="93d4f-139">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="93d4f-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="93d4f-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="93d4f-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="93d4f-141">이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="93d4f-142">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="93d4f-143">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="93d4f-144">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="93d4f-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="93d4f-145">-RouteFilter</span></span>
<span data-ttu-id="93d4f-146">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="93d4f-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="93d4f-147">-RouteFilterId</span></span>
<span data-ttu-id="93d4f-148">기존 RouteFilter 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="93d4f-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="93d4f-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="93d4f-150">이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="93d4f-151">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="93d4f-152">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="93d4f-153">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="93d4f-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="93d4f-154">-SharedKey</span></span>
<span data-ttu-id="93d4f-155">피어링 구성에 대한 미리 공유된 키로 사용되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="93d4f-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="93d4f-156">-VlanId</span></span>
<span data-ttu-id="93d4f-157">이 피어링에 할당된 VLAN의 ID 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="93d4f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d4f-158">CommonParameters</span></span>
<span data-ttu-id="93d4f-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93d4f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d4f-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93d4f-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d4f-161">입력</span><span class="sxs-lookup"><span data-stu-id="93d4f-161">INPUTS</span></span>

### <span data-ttu-id="93d4f-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="93d4f-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="93d4f-163">System.String</span><span class="sxs-lookup"><span data-stu-id="93d4f-163">System.String</span></span>

### <span data-ttu-id="93d4f-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93d4f-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="93d4f-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93d4f-165">System.Boolean</span></span>

## <span data-ttu-id="93d4f-166">출력</span><span class="sxs-lookup"><span data-stu-id="93d4f-166">OUTPUTS</span></span>

### <span data-ttu-id="93d4f-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="93d4f-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="93d4f-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93d4f-168">NOTES</span></span>

## <span data-ttu-id="93d4f-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93d4f-169">RELATED LINKS</span></span>

[<span data-ttu-id="93d4f-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="93d4f-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="93d4f-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="93d4f-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="93d4f-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="93d4f-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="93d4f-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="93d4f-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
