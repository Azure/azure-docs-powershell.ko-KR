---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 013da22d02f091d49e9780585bb8648c9c895ad7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528912"
---
# <span data-ttu-id="813a8-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="813a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="813a8-102">SYNOPSIS</span></span>
<span data-ttu-id="813a8-103">가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="813a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="813a8-104">SYNTAX</span></span>

### <span data-ttu-id="813a8-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="813a8-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="813a8-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="813a8-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813a8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="813a8-107">DESCRIPTION</span></span>
<span data-ttu-id="813a8-108">**AzureRmVirtualNetworkGateway** cmdlet은 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="813a8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="813a8-109">EXAMPLES</span></span>

### <span data-ttu-id="813a8-110">예제 1: 목표 상태 설정 가상 네트워크 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="813a8-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="813a8-111">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고이를 명명 $Gateway 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="813a8-112">두 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="813a8-113">또한이 명령은 ASN을 1337로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="813a8-114">변수</span><span class="sxs-lookup"><span data-stu-id="813a8-114">PARAMETERS</span></span>

### <span data-ttu-id="813a8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="813a8-115">-AsJob</span></span>
<span data-ttu-id="813a8-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="813a8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="813a8-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="813a8-117">-Asn</span></span>
<span data-ttu-id="813a8-118">IPsec 터널 내에서 BGP (Border Gateway Protocol) 세션을 설정 하는 데 사용 되는 가상 ASN (네트워크 게이트웨이 익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="813a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813a8-119">-DefaultProfile</span></span>
<span data-ttu-id="813a8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="813a8-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="813a8-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="813a8-122">활성 활성 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-122">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="813a8-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="813a8-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="813a8-124">활성 활성 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-124">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="813a8-125">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="813a8-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="813a8-126">강제 터널링에 사용할 기본 사이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="813a8-127">기본 사이트를 지정 하면 게이트웨이의 VPN (가상 사설망)에 있는 모든 인터넷 트래픽이 해당 사이트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="813a8-128">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="813a8-128">-GatewaySku</span></span>
<span data-ttu-id="813a8-129">가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="813a8-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="813a8-131">기본적</span><span class="sxs-lookup"><span data-stu-id="813a8-131">Basic</span></span>
- <span data-ttu-id="813a8-132">표준이</span><span class="sxs-lookup"><span data-stu-id="813a8-132">Standard</span></span>
- <span data-ttu-id="813a8-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="813a8-133">HighPerformance</span></span>
- <span data-ttu-id="813a8-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="813a8-134">VpnGw1</span></span>
- <span data-ttu-id="813a8-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="813a8-135">VpnGw2</span></span>
- <span data-ttu-id="813a8-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="813a8-136">VpnGw3</span></span>

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

### <span data-ttu-id="813a8-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="813a8-137">-PeerWeight</span></span>
<span data-ttu-id="813a8-138">이 가상 네트워크 게이트웨이에서 BGP를 통해 얻은 경로에 추가 된 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="813a8-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="813a8-139">-RadiusServerAddress</span></span>
<span data-ttu-id="813a8-140">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-140">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="813a8-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="813a8-141">-RadiusServerSecret</span></span>
<span data-ttu-id="813a8-142">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="813a8-142">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="813a8-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="813a8-144">수정이 해제 되는 가상 네트워크 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="813a8-145">Get-AzureRmVirtualNetworkGateway cmdlet을 사용 하 여 가상 네트워크 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="813a8-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="813a8-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="813a8-147">이 cmdlet이 VPN 클라이언트 IP 주소를 할당 하는 데 사용 하는 주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="813a8-148">이는 가상 네트워크 또는 온-프레미스 범위와 중복 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="813a8-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="813a8-149">-VpnClientProtocol</span></span>
<span data-ttu-id="813a8-150">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="813a8-150">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="813a8-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="813a8-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="813a8-152">해지 된 VPN 클라이언트 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="813a8-153">이들 중 하 나와 일치 하는 인증서를 제시 하는 VPN 클라이언트는 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="813a8-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="813a8-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="813a8-155">VPN 클라이언트 인증에 사용할 VPN 클라이언트 루트 인증서의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="813a8-156">VPN 클라이언트를 연결 하는 것은 이러한 루트 인증서 중 하나에서 생성 된 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="813a8-157">-확인</span><span class="sxs-lookup"><span data-stu-id="813a8-157">-Confirm</span></span>
<span data-ttu-id="813a8-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="813a8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813a8-159">-WhatIf</span></span>
<span data-ttu-id="813a8-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="813a8-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="813a8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813a8-162">CommonParameters</span></span>
<span data-ttu-id="813a8-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813a8-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813a8-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813a8-165">입력</span><span class="sxs-lookup"><span data-stu-id="813a8-165">INPUTS</span></span>

### <span data-ttu-id="813a8-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="813a8-167">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="813a8-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="813a8-168">출력</span><span class="sxs-lookup"><span data-stu-id="813a8-168">OUTPUTS</span></span>

### <span data-ttu-id="813a8-169">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="813a8-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="813a8-170">상속자</span><span class="sxs-lookup"><span data-stu-id="813a8-170">NOTES</span></span>
* <span data-ttu-id="813a8-171">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="813a8-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="813a8-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="813a8-172">RELATED LINKS</span></span>

[<span data-ttu-id="813a8-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="813a8-174">새로운 AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="813a8-175">제거-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="813a8-176">다시 설정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="813a8-177">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="813a8-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


