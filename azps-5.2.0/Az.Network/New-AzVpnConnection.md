---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326227"
---
# <span data-ttu-id="78c0c-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="78c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="78c0c-103">VpnGateway를 VpnSite로 RM에 표현된 원격 고객 분기에 연결하는 IPSec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="78c0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="78c0c-104">SYNTAX</span></span>

### <span data-ttu-id="78c0c-105">ByVpnGatewayNameByVpnSiteObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="78c0c-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78c0c-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="78c0c-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c0c-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="78c0c-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c0c-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="78c0c-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c0c-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="78c0c-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c0c-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="78c0c-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c0c-111">설명</span><span class="sxs-lookup"><span data-stu-id="78c0c-111">DESCRIPTION</span></span>
<span data-ttu-id="78c0c-112">VpnGateway를 VpnSite로 RM에 표현된 원격 고객 분기에 연결하는 IPSec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="78c0c-113">예제</span><span class="sxs-lookup"><span data-stu-id="78c0c-113">EXAMPLES</span></span>

### <span data-ttu-id="78c0c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="78c0c-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="78c0c-115">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부에 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="78c0c-116">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="78c0c-117">게이트웨이를 만든 후 New-AzVpnConnection 명령을 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="78c0c-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="78c0c-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="78c0c-119">위에서는 Azure의 "testRG" 리소스 그룹에 미국 서부에 VpnSiteLinks 1개가 있는 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="78c0c-120">VPN 게이트웨이는 가상 허브에서 이후에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="78c0c-121">게이트웨이가 생성되면 VpnSiteLink에 대한 vpnSiteLink에 New-AzVpnConnection 1개와 함께 New-AzVpnConnection 명령을 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="78c0c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78c0c-122">PARAMETERS</span></span>

### <span data-ttu-id="78c0c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78c0c-123">-AsJob</span></span>
<span data-ttu-id="78c0c-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="78c0c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78c0c-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="78c0c-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="78c0c-126">이 연결에서 처리해야 하는 대역폭(mbps)입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c0c-127">-DefaultProfile</span></span>
<span data-ttu-id="78c0c-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="78c0c-129">-EnableBgp</span></span>
<span data-ttu-id="78c0c-130">이 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="78c0c-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="78c0c-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="78c0c-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="78c0c-132">이 연결에 대해 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="78c0c-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="78c0c-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="78c0c-133">-IpSecPolicy</span></span>
<span data-ttu-id="78c0c-134">이 연결에서 처리해야 하는 대역폭(mbps)입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="78c0c-135">-Name</span></span>
<span data-ttu-id="78c0c-136">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78c0c-137">-ParentObject</span></span>
<span data-ttu-id="78c0c-138">이 연결에 대한 부모 VpnGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="78c0c-139">-ParentResourceId</span></span>
<span data-ttu-id="78c0c-140">이 연결에 대한 부모 VpnGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="78c0c-141">-ParentResourceName</span></span>
<span data-ttu-id="78c0c-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c0c-143">-ResourceGroupName</span></span>
<span data-ttu-id="78c0c-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="78c0c-145">-RoutingConfiguration</span></span>
<span data-ttu-id="78c0c-146">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="78c0c-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="78c0c-147">-SharedKey</span></span>
<span data-ttu-id="78c0c-148">이 연결을 설정하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="78c0c-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="78c0c-150">연결을 시작하는 동안 로컬 Azure IP 주소를 원본 주소로 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="78c0c-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="78c0c-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="78c0c-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="78c0c-152">이 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="78c0c-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="78c0c-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="78c0c-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="78c0c-154">게이트웨이 연결 프로토콜:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="78c0c-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="78c0c-155">-VpnSite</span></span>
<span data-ttu-id="78c0c-156">이 허브 가상 네트워크 연결이 연결된 원격 VPN 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="78c0c-157">-VpnSiteId</span></span>
<span data-ttu-id="78c0c-158">이 허브 가상 네트워크 연결이 연결된 원격 VPN 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="78c0c-160">이 VpnConnection에 있는 VpnSiteLinkConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0c-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78c0c-161">-Confirm</span></span>
<span data-ttu-id="78c0c-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c0c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c0c-163">-WhatIf</span></span>
<span data-ttu-id="78c0c-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="78c0c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c0c-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c0c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c0c-166">CommonParameters</span></span>
<span data-ttu-id="78c0c-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78c0c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c0c-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78c0c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c0c-169">입력</span><span class="sxs-lookup"><span data-stu-id="78c0c-169">INPUTS</span></span>

### <span data-ttu-id="78c0c-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="78c0c-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="78c0c-171">System.String</span><span class="sxs-lookup"><span data-stu-id="78c0c-171">System.String</span></span>

## <span data-ttu-id="78c0c-172">출력</span><span class="sxs-lookup"><span data-stu-id="78c0c-172">OUTPUTS</span></span>

### <span data-ttu-id="78c0c-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="78c0c-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78c0c-174">NOTES</span></span>

## <span data-ttu-id="78c0c-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78c0c-175">RELATED LINKS</span></span>

[<span data-ttu-id="78c0c-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="78c0c-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="78c0c-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="78c0c-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="78c0c-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="78c0c-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)