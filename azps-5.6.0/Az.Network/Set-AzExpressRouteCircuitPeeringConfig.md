---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 42a2ec1c3fb19647cc956c6b7321f52e6ad6e63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952043"
---
# <span data-ttu-id="4b6a3-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b6a3-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4b6a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6a3-103">수정된 ExpressRoute 피어링 구성을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="4b6a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b6a3-104">SYNTAX</span></span>

### <span data-ttu-id="4b6a3-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b6a3-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b6a3-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4b6a3-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b6a3-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4b6a3-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="4b6a3-108">DESCRIPTION</span></span>
<span data-ttu-id="4b6a3-109">**Set-AzExpressRouteCircuitPeeringConfig** cmdlet은 수정된 ExpressRoute 피어링 구성을 Azure에 다시 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="4b6a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="4b6a3-110">EXAMPLES</span></span>

### <span data-ttu-id="4b6a3-111">예제 1: 기존 피어링 구성 변경</span><span class="sxs-lookup"><span data-stu-id="4b6a3-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="4b6a3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4b6a3-112">Example 2</span></span>

<span data-ttu-id="4b6a3-113">수정된 ExpressRoute 피어링 구성을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="4b6a3-114">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="4b6a3-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="4b6a3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b6a3-115">PARAMETERS</span></span>

### <span data-ttu-id="4b6a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a3-116">-DefaultProfile</span></span>
<span data-ttu-id="4b6a3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6a3-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b6a3-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4b6a3-119">수정할 피어링 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4b6a3-120">-레거시모드</span><span class="sxs-lookup"><span data-stu-id="4b6a3-120">-LegacyMode</span></span>
<span data-ttu-id="4b6a3-121">피어링의 레거시 모드</span><span class="sxs-lookup"><span data-stu-id="4b6a3-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4b6a3-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4b6a3-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4b6a3-123">MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전 목록을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4b6a3-124">공용 IP 주소 도두사만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4b6a3-125">콤마로 구분된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4b6a3-126">이러한 사전은 라우팅 레지스트리 이름(RIR/IRR)에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4b6a3-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4b6a3-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4b6a3-128">피어링 AS 번호에 등록되지 않은 광고 도두사인 경우 등록된 AS 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4b6a3-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4b6a3-130">AS 번호 및 약어가 등록되는 라우팅 레지스트리 이름(RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4b6a3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4b6a3-131">-Name</span></span>
<span data-ttu-id="4b6a3-132">수정할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4b6a3-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4b6a3-133">-PeerAddressType</span></span>
<span data-ttu-id="4b6a3-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4b6a3-134">PeerAddressType</span></span>

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

### <span data-ttu-id="4b6a3-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="4b6a3-135">-PeerASN</span></span>
<span data-ttu-id="4b6a3-136">ExpressRoute 회로의 AS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4b6a3-137">PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4b6a3-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4b6a3-138">-PeeringType</span></span>
<span data-ttu-id="4b6a3-139">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4b6a3-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4b6a3-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4b6a3-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4b6a3-141">이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4b6a3-142">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4b6a3-143">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4b6a3-144">Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4b6a3-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b6a3-145">-RouteFilter</span></span>
<span data-ttu-id="4b6a3-146">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4b6a3-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4b6a3-147">-RouteFilterId</span></span>
<span data-ttu-id="4b6a3-148">기존 RouteFilter 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4b6a3-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4b6a3-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4b6a3-150">이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4b6a3-151">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4b6a3-152">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4b6a3-153">Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4b6a3-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4b6a3-154">-SharedKey</span></span>
<span data-ttu-id="4b6a3-155">피어링 구성에 대한 사전 공유 키로 사용되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4b6a3-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4b6a3-156">-VlanId</span></span>
<span data-ttu-id="4b6a3-157">이 피어링에 할당된 VLAN의 ID 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4b6a3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6a3-158">CommonParameters</span></span>
<span data-ttu-id="4b6a3-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6a3-160">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6a3-161">입력</span><span class="sxs-lookup"><span data-stu-id="4b6a3-161">INPUTS</span></span>

### <span data-ttu-id="4b6a3-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b6a3-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4b6a3-163">System.String</span><span class="sxs-lookup"><span data-stu-id="4b6a3-163">System.String</span></span>

### <span data-ttu-id="4b6a3-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b6a3-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4b6a3-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b6a3-165">System.Boolean</span></span>

## <span data-ttu-id="4b6a3-166">출력</span><span class="sxs-lookup"><span data-stu-id="4b6a3-166">OUTPUTS</span></span>

### <span data-ttu-id="4b6a3-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b6a3-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4b6a3-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b6a3-168">NOTES</span></span>

## <span data-ttu-id="4b6a3-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b6a3-169">RELATED LINKS</span></span>

[<span data-ttu-id="4b6a3-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b6a3-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4b6a3-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b6a3-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4b6a3-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b6a3-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4b6a3-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b6a3-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
