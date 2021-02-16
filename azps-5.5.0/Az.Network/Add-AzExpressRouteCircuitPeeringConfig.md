---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203216"
---
# <span data-ttu-id="a5203-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a5203-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a5203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5203-102">SYNOPSIS</span></span>
<span data-ttu-id="a5203-103">ExpressRoute 회로에 피어링 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a5203-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5203-104">SYNTAX</span></span>

### <span data-ttu-id="a5203-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5203-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5203-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="a5203-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5203-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="a5203-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5203-108">설명</span><span class="sxs-lookup"><span data-stu-id="a5203-108">DESCRIPTION</span></span>
<span data-ttu-id="a5203-109">**Add-AzExpressRouteCircuitPeeringConfig** cmdlet은 피어링 구성을 ExpressRoute 회로에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="a5203-110">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a5203-111">**Add-AzExpressRouteCircuitPeeringConfig를** 실행한 후 Set-AzExpressRouteCircuit cmdlet을 호출하여 구성을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="a5203-112">예제</span><span class="sxs-lookup"><span data-stu-id="a5203-112">EXAMPLES</span></span>

### <span data-ttu-id="a5203-113">예제 1: 기존 ExpressRoute 회로에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="a5203-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a5203-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5203-114">PARAMETERS</span></span>

### <span data-ttu-id="a5203-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5203-115">-DefaultProfile</span></span>
<span data-ttu-id="a5203-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5203-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a5203-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a5203-118">수정되는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="a5203-119">**Get-AzExpressRouteCircuit** cmdlet에서 반환된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="a5203-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="a5203-120">-LegacyMode</span></span>
<span data-ttu-id="a5203-121">피어링의 레거시 모드</span><span class="sxs-lookup"><span data-stu-id="a5203-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="a5203-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="a5203-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="a5203-123">MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전의 목록을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="a5203-124">공용 IP 주소 연결만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="a5203-125">콤마로 구분된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="a5203-126">이러한 사전은 RIR/IRR(라우팅 레지스트리 이름)에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="a5203-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="a5203-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="a5203-128">피어링 AS 번호에 등록되지 않은 광고의 경우 등록할 AS 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="a5203-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="a5203-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="a5203-130">AS 번호 및 prefix가 등록되는 RIR/IRR(라우팅 레지스트리 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="a5203-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a5203-131">-Name</span></span>
<span data-ttu-id="a5203-132">추가할 피어링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="a5203-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a5203-133">-PeerAddressType</span></span>
<span data-ttu-id="a5203-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a5203-134">PeerAddressType</span></span>

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

### <span data-ttu-id="a5203-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="a5203-135">-PeerASN</span></span>
<span data-ttu-id="a5203-136">ExpressRoute 회로의 AS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="a5203-137">PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="a5203-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a5203-138">-PeeringType</span></span>
<span data-ttu-id="a5203-139">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a5203-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a5203-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a5203-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="a5203-141">이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="a5203-142">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a5203-143">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a5203-144">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a5203-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a5203-145">-RouteFilter</span></span>
<span data-ttu-id="a5203-146">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a5203-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="a5203-147">-RouteFilterId</span></span>
<span data-ttu-id="a5203-148">기존 RouteFilter 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a5203-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a5203-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="a5203-150">이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="a5203-151">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a5203-152">이 서브넷의 첫 번째 홀수 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a5203-153">Azure는 Azure 라우터 인터페이스에 다음 even-numbered 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a5203-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a5203-154">-SharedKey</span></span>
<span data-ttu-id="a5203-155">피어링 구성에 대한 미리 공유된 키로 사용되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="a5203-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="a5203-156">-VlanId</span></span>
<span data-ttu-id="a5203-157">이 피어링에 할당된 VLAN의 ID 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="a5203-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5203-158">CommonParameters</span></span>
<span data-ttu-id="a5203-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5203-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5203-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5203-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5203-161">입력</span><span class="sxs-lookup"><span data-stu-id="a5203-161">INPUTS</span></span>

### <span data-ttu-id="a5203-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a5203-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="a5203-163">System.String</span><span class="sxs-lookup"><span data-stu-id="a5203-163">System.String</span></span>

### <span data-ttu-id="a5203-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a5203-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="a5203-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5203-165">System.Boolean</span></span>

## <span data-ttu-id="a5203-166">출력</span><span class="sxs-lookup"><span data-stu-id="a5203-166">OUTPUTS</span></span>

### <span data-ttu-id="a5203-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a5203-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a5203-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5203-168">NOTES</span></span>

## <span data-ttu-id="a5203-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5203-169">RELATED LINKS</span></span>

[<span data-ttu-id="a5203-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a5203-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a5203-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a5203-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a5203-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a5203-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a5203-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a5203-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
