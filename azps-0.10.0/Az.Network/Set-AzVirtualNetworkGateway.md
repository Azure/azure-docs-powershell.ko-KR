---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 87840267cf85997da83af590664c473a61f74033
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876542"
---
# <span data-ttu-id="cc826-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="cc826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc826-102">SYNOPSIS</span></span>
<span data-ttu-id="cc826-103">가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="cc826-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc826-104">SYNTAX</span></span>

### <span data-ttu-id="cc826-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cc826-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc826-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc826-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc826-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cc826-107">DESCRIPTION</span></span>
<span data-ttu-id="cc826-108">**AzVirtualNetworkGateway** cmdlet은 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="cc826-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cc826-109">EXAMPLES</span></span>

### <span data-ttu-id="cc826-110">예제 1: 목표 상태 설정 가상 네트워크 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="cc826-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="cc826-111">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고이를 명명 $Gateway 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="cc826-112">두 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="cc826-113">또한이 명령은 ASN을 1337로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="cc826-114">변수</span><span class="sxs-lookup"><span data-stu-id="cc826-114">PARAMETERS</span></span>

### <span data-ttu-id="cc826-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc826-115">-AsJob</span></span>
<span data-ttu-id="cc826-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cc826-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="cc826-117">-Asn</span></span>
<span data-ttu-id="cc826-118">IPsec 터널 내에서 BGP (Border Gateway Protocol) 세션을 설정 하는 데 사용 되는 가상 ASN (네트워크 게이트웨이 익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc826-119">-DefaultProfile</span></span>
<span data-ttu-id="cc826-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="cc826-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="cc826-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="cc826-122">활성 활성 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="cc826-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="cc826-124">활성 활성 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-125">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="cc826-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="cc826-126">강제 터널링에 사용할 기본 사이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="cc826-127">기본 사이트를 지정 하면 게이트웨이의 VPN (가상 사설망)에 있는 모든 인터넷 트래픽이 해당 사이트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-128">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="cc826-128">-GatewaySku</span></span>
<span data-ttu-id="cc826-129">가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="cc826-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc826-131">기본적</span><span class="sxs-lookup"><span data-stu-id="cc826-131">Basic</span></span>
- <span data-ttu-id="cc826-132">표준이</span><span class="sxs-lookup"><span data-stu-id="cc826-132">Standard</span></span>
- <span data-ttu-id="cc826-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="cc826-133">HighPerformance</span></span>
- <span data-ttu-id="cc826-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="cc826-134">VpnGw1</span></span>
- <span data-ttu-id="cc826-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="cc826-135">VpnGw2</span></span>
- <span data-ttu-id="cc826-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="cc826-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="cc826-137">-PeerWeight</span></span>
<span data-ttu-id="cc826-138">이 가상 네트워크 게이트웨이에서 BGP를 통해 얻은 경로에 추가 된 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="cc826-139">-RadiusServerAddress</span></span>
<span data-ttu-id="cc826-140">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="cc826-141">-RadiusServerSecret</span></span>
<span data-ttu-id="cc826-142">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="cc826-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="cc826-144">수정이 해제 되는 가상 네트워크 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="cc826-145">Get-AzVirtualNetworkGateway cmdlet을 사용 하 여 가상 네트워크 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-145">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="cc826-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="cc826-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="cc826-147">이 cmdlet이 VPN 클라이언트 IP 주소를 할당 하는 데 사용 하는 주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="cc826-148">이는 가상 네트워크 또는 온-프레미스 범위와 중복 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-148">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="cc826-149">-VpnClientProtocol</span></span>
<span data-ttu-id="cc826-150">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="cc826-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="cc826-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="cc826-152">해지 된 VPN 클라이언트 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="cc826-153">이들 중 하 나와 일치 하는 인증서를 제시 하는 VPN 클라이언트는 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="cc826-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="cc826-155">VPN 클라이언트 인증에 사용할 VPN 클라이언트 루트 인증서의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="cc826-156">VPN 클라이언트를 연결 하는 것은 이러한 루트 인증서 중 하나에서 생성 된 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-157">-확인</span><span class="sxs-lookup"><span data-stu-id="cc826-157">-Confirm</span></span>
<span data-ttu-id="cc826-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc826-159">-WhatIf</span></span>
<span data-ttu-id="cc826-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc826-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc826-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc826-162">CommonParameters</span></span>
<span data-ttu-id="cc826-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc826-164">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc826-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc826-165">입력</span><span class="sxs-lookup"><span data-stu-id="cc826-165">INPUTS</span></span>

### <span data-ttu-id="cc826-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="cc826-167">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc826-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="cc826-168">출력</span><span class="sxs-lookup"><span data-stu-id="cc826-168">OUTPUTS</span></span>

### <span data-ttu-id="cc826-169">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cc826-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cc826-170">상속자</span><span class="sxs-lookup"><span data-stu-id="cc826-170">NOTES</span></span>
* <span data-ttu-id="cc826-171">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="cc826-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cc826-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc826-172">RELATED LINKS</span></span>

[<span data-ttu-id="cc826-173">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-173">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cc826-174">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-174">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cc826-175">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-175">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cc826-176">다시 설정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-176">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="cc826-177">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cc826-177">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


