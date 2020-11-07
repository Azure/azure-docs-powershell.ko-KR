---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 870caec4cad2bd4d64c00a2b0bf3423f080b98ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877650"
---
# <span data-ttu-id="456df-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="456df-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="456df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456df-102">SYNOPSIS</span></span>
<span data-ttu-id="456df-103">VpnGateway를 RM에 VpnSite로 표시 되는 원격 고객 분기에 연결 하는 IPSec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="456df-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="456df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="456df-104">SYNTAX</span></span>

### <span data-ttu-id="456df-105">ByVpnGatewayNameByVpnSiteObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="456df-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="456df-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="456df-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="456df-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456df-111">설명은</span><span class="sxs-lookup"><span data-stu-id="456df-111">DESCRIPTION</span></span>
<span data-ttu-id="456df-112">VpnGateway를 RM에 VpnSite로 표시 되는 원격 고객 분기에 연결 하는 IPSec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="456df-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="456df-113">예제의</span><span class="sxs-lookup"><span data-stu-id="456df-113">EXAMPLES</span></span>

### <span data-ttu-id="456df-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="456df-114">Example 1</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="456df-115">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="456df-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="456df-116">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="456df-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="456df-117">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="456df-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="456df-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="456df-118">Example 2</span></span>
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

<span data-ttu-id="456df-119">위의 작업을 통해 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브, Azure의 "testRG" 리소스 그룹에 VpnSiteLinks 1 인 "VpnSite"를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="456df-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="456df-120">가상 허브에서 VPN 게이트웨이는 이후에 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="456df-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="456df-121">게이트웨이가 만들어지면 VpnSite의 VpnSiteLink에 대 한 1 VpnSiteLinkConnections New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="456df-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="456df-122">변수</span><span class="sxs-lookup"><span data-stu-id="456df-122">PARAMETERS</span></span>

### <span data-ttu-id="456df-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456df-123">-AsJob</span></span>
<span data-ttu-id="456df-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="456df-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="456df-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="456df-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="456df-126">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="456df-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456df-127">-DefaultProfile</span></span>
<span data-ttu-id="456df-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456df-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="456df-129">-EnableBgp</span></span>
<span data-ttu-id="456df-130">이 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="456df-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="456df-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="456df-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="456df-132">이 연결에 인터넷 보안 설정</span><span class="sxs-lookup"><span data-stu-id="456df-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="456df-133">-정책</span><span class="sxs-lookup"><span data-stu-id="456df-133">-IpSecPolicy</span></span>
<span data-ttu-id="456df-134">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="456df-135">-이름</span><span class="sxs-lookup"><span data-stu-id="456df-135">-Name</span></span>
<span data-ttu-id="456df-136">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-136">The resource name.</span></span>

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

### <span data-ttu-id="456df-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="456df-137">-ParentObject</span></span>
<span data-ttu-id="456df-138">이 연결에 대 한 부모 VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="456df-138">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="456df-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-139">-ParentResourceId</span></span>
<span data-ttu-id="456df-140">이 연결에 대 한 부모 VpnGateway의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-140">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="456df-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="456df-141">-ParentResourceName</span></span>
<span data-ttu-id="456df-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-142">The resource group name.</span></span>

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

### <span data-ttu-id="456df-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456df-143">-ResourceGroupName</span></span>
<span data-ttu-id="456df-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-144">The resource group name.</span></span>

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

### <span data-ttu-id="456df-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="456df-145">-SharedKey</span></span>
<span data-ttu-id="456df-146">이 연결을 설정 하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="456df-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="456df-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="456df-148">연결을 시작 하는 동안 로컬 azure ip 주소를 원본 주소로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="456df-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="456df-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="456df-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="456df-150">이 연결에 정책 기반 트래픽 선택기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="456df-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="456df-151">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="456df-151">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="456df-152">게이트웨이 연결 프로토콜: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="456df-152">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="456df-153">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="456df-153">-VpnSite</span></span>
<span data-ttu-id="456df-154">이 허브 가상 네트워크 연결이 연결 된 원격 vpn 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-154">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="456df-155">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="456df-155">-VpnSiteId</span></span>
<span data-ttu-id="456df-156">이 허브 가상 네트워크 연결이 연결 된 원격 vpn 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="456df-157">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="456df-157">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="456df-158">이 VpnConnection에 있는 VpnSiteLinkConnections의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="456df-158">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

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

### <span data-ttu-id="456df-159">-확인</span><span class="sxs-lookup"><span data-stu-id="456df-159">-Confirm</span></span>
<span data-ttu-id="456df-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="456df-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456df-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456df-161">-WhatIf</span></span>
<span data-ttu-id="456df-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="456df-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456df-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="456df-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456df-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456df-164">CommonParameters</span></span>
<span data-ttu-id="456df-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="456df-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456df-166">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="456df-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456df-167">입력</span><span class="sxs-lookup"><span data-stu-id="456df-167">INPUTS</span></span>

### <span data-ttu-id="456df-168">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="456df-168">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="456df-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="456df-169">System.String</span></span>

## <span data-ttu-id="456df-170">출력</span><span class="sxs-lookup"><span data-stu-id="456df-170">OUTPUTS</span></span>

### <span data-ttu-id="456df-171">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="456df-171">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="456df-172">상속자</span><span class="sxs-lookup"><span data-stu-id="456df-172">NOTES</span></span>

## <span data-ttu-id="456df-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="456df-173">RELATED LINKS</span></span>

[<span data-ttu-id="456df-174">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="456df-174">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="456df-175">제거-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="456df-175">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="456df-176">업데이트-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="456df-176">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
