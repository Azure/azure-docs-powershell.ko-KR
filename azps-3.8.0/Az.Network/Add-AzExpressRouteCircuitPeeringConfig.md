---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877478"
---
# <span data-ttu-id="2c3c0-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2c3c0-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="2c3c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3c0-103">Express 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2c3c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c3c0-104">SYNTAX</span></span>

### <span data-ttu-id="2c3c0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c3c0-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3c0-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="2c3c0-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3c0-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="2c3c0-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3c0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c3c0-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3c0-109">**AzExpressRouteCircuitPeeringConfig** cmdlet은 대상 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="2c3c0-110">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2c3c0-111">**Add-AzExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="2c3c0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2c3c0-112">EXAMPLES</span></span>

### <span data-ttu-id="2c3c0-113">예제 1: 기존 Express 대상 회로에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="2c3c0-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="2c3c0-114">변수</span><span class="sxs-lookup"><span data-stu-id="2c3c0-114">PARAMETERS</span></span>

### <span data-ttu-id="2c3c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3c0-115">-DefaultProfile</span></span>
<span data-ttu-id="2c3c0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3c0-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2c3c0-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2c3c0-118">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="2c3c0-119">**AzExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="2c3c0-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="2c3c0-120">-LegacyMode</span></span>
<span data-ttu-id="2c3c0-121">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="2c3c0-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="2c3c0-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="2c3c0-123">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="2c3c0-124">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="2c3c0-125">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="2c3c0-126">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="2c3c0-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="2c3c0-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="2c3c0-128">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="2c3c0-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="2c3c0-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="2c3c0-130">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="2c3c0-131">-이름</span><span class="sxs-lookup"><span data-stu-id="2c3c0-131">-Name</span></span>
<span data-ttu-id="2c3c0-132">추가할 피어 링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="2c3c0-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2c3c0-133">-PeerAddressType</span></span>
<span data-ttu-id="2c3c0-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2c3c0-134">PeerAddressType</span></span>

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

### <span data-ttu-id="2c3c0-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="2c3c0-135">-PeerASN</span></span>
<span data-ttu-id="2c3c0-136">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="2c3c0-137">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="2c3c0-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2c3c0-138">-PeeringType</span></span>
<span data-ttu-id="2c3c0-139">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2c3c0-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2c3c0-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2c3c0-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="2c3c0-141">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="2c3c0-142">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2c3c0-143">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2c3c0-144">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2c3c0-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2c3c0-145">-RouteFilter</span></span>
<span data-ttu-id="2c3c0-146">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2c3c0-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="2c3c0-147">-RouteFilterId</span></span>
<span data-ttu-id="2c3c0-148">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2c3c0-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2c3c0-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="2c3c0-150">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="2c3c0-151">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2c3c0-152">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2c3c0-153">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2c3c0-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2c3c0-154">-SharedKey</span></span>
<span data-ttu-id="2c3c0-155">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="2c3c0-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="2c3c0-156">-VlanId</span></span>
<span data-ttu-id="2c3c0-157">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="2c3c0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3c0-158">CommonParameters</span></span>
<span data-ttu-id="2c3c0-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3c0-160">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3c0-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3c0-161">입력</span><span class="sxs-lookup"><span data-stu-id="2c3c0-161">INPUTS</span></span>

### <span data-ttu-id="2c3c0-162">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="2c3c0-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c3c0-163">System.String</span></span>

### <span data-ttu-id="2c3c0-164">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="2c3c0-165">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2c3c0-165">System.Boolean</span></span>

## <span data-ttu-id="2c3c0-166">출력</span><span class="sxs-lookup"><span data-stu-id="2c3c0-166">OUTPUTS</span></span>

### <span data-ttu-id="2c3c0-167">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2c3c0-168">상속자</span><span class="sxs-lookup"><span data-stu-id="2c3c0-168">NOTES</span></span>

## <span data-ttu-id="2c3c0-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c3c0-169">RELATED LINKS</span></span>

[<span data-ttu-id="2c3c0-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2c3c0-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2c3c0-171">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2c3c0-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2c3c0-172">제거-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2c3c0-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2c3c0-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2c3c0-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
