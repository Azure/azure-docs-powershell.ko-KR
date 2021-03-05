---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 4f61bce910a2dc0f2b177423a5dc199103da378d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984304"
---
# <span data-ttu-id="e33c4-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e33c4-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="e33c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e33c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e33c4-103">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="e33c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="e33c4-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e33c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="e33c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e33c4-106">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="e33c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="e33c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e33c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e33c4-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="e33c4-109">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite를 Azure의 "testRG" 리소스 그룹에서 미국 서부에 1개 VpnSiteLinks를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="e33c4-110">가상 허브에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="e33c4-111">게이트웨이가 만들어지면 VpnSite의 VpnSiteLink에 New-AzVpnConnection 1개 vpnSiteLink를 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="e33c4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e33c4-112">PARAMETERS</span></span>

### <span data-ttu-id="e33c4-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="e33c4-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="e33c4-114">이 링크 연결에서 처리해야 하는 대역폭은 mbps입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e33c4-115">-DefaultProfile</span></span>
<span data-ttu-id="e33c4-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e33c4-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="e33c4-117">-EgressNatRule</span></span>
<span data-ttu-id="e33c4-118">이 연결 연결과 연결된 NAT 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e33c4-119">-EnableBgp</span></span>
<span data-ttu-id="e33c4-120">이 연결에 대해 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="e33c4-120">Enable BGP for this link connection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="e33c4-121">-IngressNatRule</span></span>
<span data-ttu-id="e33c4-122">이 연결 연결과 연결된 NAT 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="e33c4-123">-IpSecPolicy</span></span>
<span data-ttu-id="e33c4-124">이 연결에 대해 고려할 IpSec 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-124">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e33c4-125">-Name</span></span>
<span data-ttu-id="e33c4-126">이름</span><span class="sxs-lookup"><span data-stu-id="e33c4-126">Name</span></span>

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

### <span data-ttu-id="e33c4-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="e33c4-127">-RoutingWeight</span></span>
<span data-ttu-id="e33c4-128">라우팅 가중치</span><span class="sxs-lookup"><span data-stu-id="e33c4-128">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e33c4-129">-SharedKey</span></span>
<span data-ttu-id="e33c4-130">이 연결 연결을 설정하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-130">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="e33c4-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="e33c4-132">이 링크 연결에 대해 로컬 Azure IP 주소를 원본 IP로 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="e33c4-132">Use local azure ip address as source ip for this link connection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e33c4-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e33c4-134">이 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="e33c4-134">Use policy based traffic selectors for this link connection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="e33c4-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="e33c4-136">게이트웨이 연결 프로토콜:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="e33c4-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e33c4-137">-VpnSiteLink</span></span>
<span data-ttu-id="e33c4-138">연결할 VPN 사이트 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-138">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e33c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33c4-139">CommonParameters</span></span>
<span data-ttu-id="e33c4-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e33c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33c4-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e33c4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33c4-142">입력</span><span class="sxs-lookup"><span data-stu-id="e33c4-142">INPUTS</span></span>

### <span data-ttu-id="e33c4-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e33c4-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="e33c4-144">출력</span><span class="sxs-lookup"><span data-stu-id="e33c4-144">OUTPUTS</span></span>

### <span data-ttu-id="e33c4-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e33c4-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="e33c4-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e33c4-146">NOTES</span></span>

## <span data-ttu-id="e33c4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e33c4-147">RELATED LINKS</span></span>

[<span data-ttu-id="e33c4-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e33c4-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)