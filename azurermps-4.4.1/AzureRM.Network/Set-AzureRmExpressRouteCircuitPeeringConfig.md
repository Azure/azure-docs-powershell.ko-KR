---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 87c956769efb41485e43e65ff31d7a9cd7387d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535463"
---
# <span data-ttu-id="a34cd-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a34cd-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a34cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a34cd-103">수정 된 Express 경로 링 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a34cd-104">SYNTAX</span></span>

### <span data-ttu-id="a34cd-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a34cd-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a34cd-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="a34cd-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a34cd-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="a34cd-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a34cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a34cd-108">DESCRIPTION</span></span>
<span data-ttu-id="a34cd-109">AzureRmExpressRouteCircuitPeeringConfig cmdlet은 수정 된 Express 경로 **설정** 피어 링 구성을 Azure에 다시 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="a34cd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a34cd-110">EXAMPLES</span></span>

### <span data-ttu-id="a34cd-111">예제 1: 기존 피어 링 구성 변경</span><span class="sxs-lookup"><span data-stu-id="a34cd-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a34cd-112">변수</span><span class="sxs-lookup"><span data-stu-id="a34cd-112">PARAMETERS</span></span>

### <span data-ttu-id="a34cd-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a34cd-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a34cd-114">수정할 피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-114">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="a34cd-115">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="a34cd-115">-LegacyMode</span></span>
<span data-ttu-id="a34cd-116">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-116">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="a34cd-117">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="a34cd-117">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="a34cd-118">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-118">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="a34cd-119">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-119">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="a34cd-120">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-120">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="a34cd-121">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-121">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="a34cd-122">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="a34cd-122">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="a34cd-123">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-123">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="a34cd-124">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="a34cd-124">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="a34cd-125">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-125">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="a34cd-126">-이름</span><span class="sxs-lookup"><span data-stu-id="a34cd-126">-Name</span></span>
<span data-ttu-id="a34cd-127">수정할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-127">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="a34cd-128">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a34cd-128">-PeerAddressType</span></span>
<span data-ttu-id="a34cd-129">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a34cd-129">PeerAddressType</span></span>

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

### <span data-ttu-id="a34cd-130">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="a34cd-130">-PeerASN</span></span>
<span data-ttu-id="a34cd-131">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-131">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="a34cd-132">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-132">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="a34cd-133">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a34cd-133">-PeeringType</span></span>
<span data-ttu-id="a34cd-134">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a34cd-134">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a34cd-135">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a34cd-135">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="a34cd-136">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-136">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="a34cd-137">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-137">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a34cd-138">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-138">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a34cd-139">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-139">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a34cd-140">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a34cd-140">-RouteFilter</span></span>
<span data-ttu-id="a34cd-141">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-141">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a34cd-142">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="a34cd-142">-RouteFilterId</span></span>
<span data-ttu-id="a34cd-143">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-143">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a34cd-144">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a34cd-144">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="a34cd-145">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-145">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="a34cd-146">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-146">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a34cd-147">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-147">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a34cd-148">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-148">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a34cd-149">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a34cd-149">-SharedKey</span></span>
<span data-ttu-id="a34cd-150">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-150">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="a34cd-151">-VlanId</span><span class="sxs-lookup"><span data-stu-id="a34cd-151">-VlanId</span></span>
<span data-ttu-id="a34cd-152">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-152">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="a34cd-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34cd-153">-DefaultProfile</span></span>
<span data-ttu-id="a34cd-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a34cd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34cd-155">CommonParameters</span></span>
<span data-ttu-id="a34cd-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34cd-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34cd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34cd-158">입력</span><span class="sxs-lookup"><span data-stu-id="a34cd-158">INPUTS</span></span>

### <span data-ttu-id="a34cd-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a34cd-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="a34cd-160">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34cd-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="a34cd-161">출력</span><span class="sxs-lookup"><span data-stu-id="a34cd-161">OUTPUTS</span></span>

### <span data-ttu-id="a34cd-162">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a34cd-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a34cd-163">상속자</span><span class="sxs-lookup"><span data-stu-id="a34cd-163">NOTES</span></span>

## <span data-ttu-id="a34cd-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a34cd-164">RELATED LINKS</span></span>

[<span data-ttu-id="a34cd-165">추가-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a34cd-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a34cd-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a34cd-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a34cd-167">새로운 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a34cd-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a34cd-168">제거-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a34cd-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)
