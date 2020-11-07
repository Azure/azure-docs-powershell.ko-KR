---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ecbd0d101db979d5982891bbfbd4ad1e3083ee8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700023"
---
# <span data-ttu-id="4df97-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4df97-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4df97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df97-102">SYNOPSIS</span></span>
<span data-ttu-id="4df97-103">수정 된 Express 경로 링 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="4df97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4df97-104">SYNTAX</span></span>

### <span data-ttu-id="4df97-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="4df97-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4df97-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4df97-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4df97-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4df97-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df97-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4df97-108">DESCRIPTION</span></span>
<span data-ttu-id="4df97-109">AzExpressRouteCircuitPeeringConfig cmdlet은 수정 된 Express 경로 **설정** 피어 링 구성을 Azure에 다시 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="4df97-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4df97-110">EXAMPLES</span></span>

### <span data-ttu-id="4df97-111">예제 1: 기존 피어 링 구성 변경</span><span class="sxs-lookup"><span data-stu-id="4df97-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="4df97-112">변수</span><span class="sxs-lookup"><span data-stu-id="4df97-112">PARAMETERS</span></span>

### <span data-ttu-id="4df97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df97-113">-DefaultProfile</span></span>
<span data-ttu-id="4df97-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df97-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df97-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4df97-116">수정할 피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4df97-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="4df97-117">-LegacyMode</span></span>
<span data-ttu-id="4df97-118">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4df97-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4df97-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4df97-120">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4df97-121">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4df97-122">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4df97-123">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4df97-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4df97-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4df97-125">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4df97-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4df97-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4df97-127">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4df97-128">-이름</span><span class="sxs-lookup"><span data-stu-id="4df97-128">-Name</span></span>
<span data-ttu-id="4df97-129">수정할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="4df97-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4df97-130">-PeerAddressType</span></span>
<span data-ttu-id="4df97-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4df97-131">PeerAddressType</span></span>

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

### <span data-ttu-id="4df97-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="4df97-132">-PeerASN</span></span>
<span data-ttu-id="4df97-133">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4df97-134">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4df97-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4df97-135">-PeeringType</span></span>
<span data-ttu-id="4df97-136">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4df97-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4df97-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4df97-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4df97-138">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4df97-139">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4df97-140">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4df97-141">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4df97-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4df97-142">-RouteFilter</span></span>
<span data-ttu-id="4df97-143">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4df97-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4df97-144">-RouteFilterId</span></span>
<span data-ttu-id="4df97-145">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4df97-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4df97-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4df97-147">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4df97-148">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4df97-149">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4df97-150">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4df97-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4df97-151">-SharedKey</span></span>
<span data-ttu-id="4df97-152">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4df97-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4df97-153">-VlanId</span></span>
<span data-ttu-id="4df97-154">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4df97-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df97-155">CommonParameters</span></span>
<span data-ttu-id="4df97-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df97-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df97-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df97-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df97-158">입력</span><span class="sxs-lookup"><span data-stu-id="4df97-158">INPUTS</span></span>

### <span data-ttu-id="4df97-159">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4df97-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4df97-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4df97-160">System.String</span></span>

### <span data-ttu-id="4df97-161">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4df97-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4df97-162">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4df97-162">System.Boolean</span></span>

## <span data-ttu-id="4df97-163">출력</span><span class="sxs-lookup"><span data-stu-id="4df97-163">OUTPUTS</span></span>

### <span data-ttu-id="4df97-164">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4df97-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4df97-165">상속자</span><span class="sxs-lookup"><span data-stu-id="4df97-165">NOTES</span></span>

## <span data-ttu-id="4df97-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4df97-166">RELATED LINKS</span></span>

[<span data-ttu-id="4df97-167">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4df97-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4df97-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df97-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4df97-169">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4df97-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4df97-170">제거-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4df97-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
