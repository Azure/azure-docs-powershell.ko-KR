---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364799"
---
# <span data-ttu-id="90dd9-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="90dd9-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="90dd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="90dd9-103">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="90dd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="90dd9-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90dd9-105">설명</span><span class="sxs-lookup"><span data-stu-id="90dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="90dd9-106">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="90dd9-107">예제</span><span class="sxs-lookup"><span data-stu-id="90dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="90dd9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90dd9-108">Example 1</span></span>
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

<span data-ttu-id="90dd9-109">위에서는 Azure의 "testRG" 리소스 그룹에 미국 서부에 VpnSiteLinks 1개가 있는 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="90dd9-110">VPN 게이트웨이는 가상 허브에서 이후에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="90dd9-111">게이트웨이가 생성되면 VpnSiteLink에 대한 vpnSiteLink에 New-AzVpnConnection 1개와 함께 New-AzVpnConnection 명령을 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="90dd9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90dd9-112">PARAMETERS</span></span>

### <span data-ttu-id="90dd9-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="90dd9-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="90dd9-114">이 링크 연결에서 처리해야 하는 대역폭(mbps)입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="90dd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dd9-115">-DefaultProfile</span></span>
<span data-ttu-id="90dd9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90dd9-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="90dd9-117">-EnableBgp</span></span>
<span data-ttu-id="90dd9-118">이 링크 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="90dd9-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="90dd9-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="90dd9-119">-IpSecPolicy</span></span>
<span data-ttu-id="90dd9-120">이 연결에 대해 고려할 IpSec 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="90dd9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90dd9-121">-Name</span></span>
<span data-ttu-id="90dd9-122">이름</span><span class="sxs-lookup"><span data-stu-id="90dd9-122">Name</span></span>

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

### <span data-ttu-id="90dd9-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="90dd9-123">-RoutingWeight</span></span>
<span data-ttu-id="90dd9-124">라우팅 가중치</span><span class="sxs-lookup"><span data-stu-id="90dd9-124">Routing Weight</span></span>

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

### <span data-ttu-id="90dd9-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="90dd9-125">-SharedKey</span></span>
<span data-ttu-id="90dd9-126">이 연결 연결을 설정하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="90dd9-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="90dd9-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="90dd9-128">이 연결에 대한 원본 IP로 로컬 Azure IP 주소를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="90dd9-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="90dd9-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="90dd9-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="90dd9-130">이 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="90dd9-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="90dd9-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="90dd9-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="90dd9-132">게이트웨이 연결 프로토콜:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="90dd9-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="90dd9-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="90dd9-133">-VpnSiteLink</span></span>
<span data-ttu-id="90dd9-134">연결할 vpn 사이트 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="90dd9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dd9-135">CommonParameters</span></span>
<span data-ttu-id="90dd9-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90dd9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dd9-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90dd9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dd9-138">입력</span><span class="sxs-lookup"><span data-stu-id="90dd9-138">INPUTS</span></span>

### <span data-ttu-id="90dd9-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="90dd9-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="90dd9-140">출력</span><span class="sxs-lookup"><span data-stu-id="90dd9-140">OUTPUTS</span></span>

### <span data-ttu-id="90dd9-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="90dd9-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="90dd9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90dd9-142">NOTES</span></span>

## <span data-ttu-id="90dd9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90dd9-143">RELATED LINKS</span></span>

[<span data-ttu-id="90dd9-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="90dd9-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)