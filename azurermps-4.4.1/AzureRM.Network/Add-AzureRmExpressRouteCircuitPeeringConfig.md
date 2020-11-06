---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537104"
---
# <span data-ttu-id="2b953-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2b953-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="2b953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b953-102">SYNOPSIS</span></span>
<span data-ttu-id="2b953-103">Express 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b953-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b953-104">SYNTAX</span></span>

### <span data-ttu-id="2b953-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b953-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b953-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="2b953-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b953-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="2b953-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b953-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b953-108">DESCRIPTION</span></span>
<span data-ttu-id="2b953-109">**AzureRmExpressRouteCircuitPeeringConfig** cmdlet은 대상 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="2b953-110">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2b953-111">**Add-AzureRmExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzureRmExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b953-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="2b953-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2b953-112">EXAMPLES</span></span>

### <span data-ttu-id="2b953-113">예제 1: 기존 Express 대상 회로에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="2b953-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="2b953-114">변수</span><span class="sxs-lookup"><span data-stu-id="2b953-114">PARAMETERS</span></span>

### <span data-ttu-id="2b953-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b953-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2b953-116">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="2b953-117">**AzureRmExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="2b953-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="2b953-118">-LegacyMode</span></span>
<span data-ttu-id="2b953-119">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="2b953-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="2b953-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="2b953-121">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="2b953-122">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="2b953-123">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="2b953-124">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b953-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="2b953-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="2b953-126">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="2b953-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="2b953-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="2b953-128">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="2b953-129">-이름</span><span class="sxs-lookup"><span data-stu-id="2b953-129">-Name</span></span>
<span data-ttu-id="2b953-130">추가할 피어 링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="2b953-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2b953-131">-PeerAddressType</span></span>
<span data-ttu-id="2b953-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2b953-132">PeerAddressType</span></span>

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

### <span data-ttu-id="2b953-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="2b953-133">-PeerASN</span></span>
<span data-ttu-id="2b953-134">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="2b953-135">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="2b953-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2b953-136">-PeeringType</span></span>
<span data-ttu-id="2b953-137">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2b953-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2b953-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b953-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="2b953-139">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="2b953-140">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2b953-141">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2b953-142">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2b953-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b953-143">-RouteFilter</span></span>
<span data-ttu-id="2b953-144">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2b953-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="2b953-145">-RouteFilterId</span></span>
<span data-ttu-id="2b953-146">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2b953-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b953-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="2b953-148">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="2b953-149">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2b953-150">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2b953-151">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2b953-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2b953-152">-SharedKey</span></span>
<span data-ttu-id="2b953-153">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="2b953-154">-VlanId</span><span class="sxs-lookup"><span data-stu-id="2b953-154">-VlanId</span></span>
<span data-ttu-id="2b953-155">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="2b953-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b953-156">-DefaultProfile</span></span>
<span data-ttu-id="2b953-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b953-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b953-158">CommonParameters</span></span>
<span data-ttu-id="2b953-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b953-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b953-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b953-161">입력</span><span class="sxs-lookup"><span data-stu-id="2b953-161">INPUTS</span></span>

### <span data-ttu-id="2b953-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b953-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2b953-163">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b953-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="2b953-164">출력</span><span class="sxs-lookup"><span data-stu-id="2b953-164">OUTPUTS</span></span>

### <span data-ttu-id="2b953-165">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2b953-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2b953-166">상속자</span><span class="sxs-lookup"><span data-stu-id="2b953-166">NOTES</span></span>

## <span data-ttu-id="2b953-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b953-167">RELATED LINKS</span></span>

[<span data-ttu-id="2b953-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b953-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2b953-169">새로운 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2b953-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2b953-170">제거-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2b953-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2b953-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b953-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
