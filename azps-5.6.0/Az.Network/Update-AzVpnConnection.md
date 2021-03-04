---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 3de80ca92f86ab969b9d44ffc9f63871486d969a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951467"
---
# <span data-ttu-id="7f691-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="7f691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f691-102">SYNOPSIS</span></span>
<span data-ttu-id="7f691-103">VPN 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="7f691-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f691-104">SYNTAX</span></span>

### <span data-ttu-id="7f691-105">ByVpnConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f691-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f691-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7f691-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f691-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7f691-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f691-108">설명</span><span class="sxs-lookup"><span data-stu-id="7f691-108">DESCRIPTION</span></span>
<span data-ttu-id="7f691-109">**Update-AzVpnConnection** cmdlet은 VPN 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="7f691-110">VPN 연결은 VPN 게이트웨이를 VPN 사이트로 Azure로 나타내는 원격 고객 분기에 연결하는 IPsec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="7f691-111">예제</span><span class="sxs-lookup"><span data-stu-id="7f691-111">EXAMPLES</span></span>

### <span data-ttu-id="7f691-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f691-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="7f691-113">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 Azure의 "testRG" 리소스 그룹에서 미국 서부에 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7f691-114">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7f691-115">게이트웨이가 만들어지면 이 게이트웨이는 New-AzVpnConnection 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7f691-116">그런 다음, 새 IpSecPolicy를 갖기 위해 연결은 Set-AzVpnConnection 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="7f691-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="7f691-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="7f691-118">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 Azure의 "testRG" 리소스 그룹에서 미국 서부에 VpnSite를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7f691-119">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7f691-120">게이트웨이가 만들어지면 이 게이트웨이는 New-AzVpnConnection 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="7f691-121">그런 다음 보안 문자열 구문을 사용하여 새 공유 키를 하게 하여 연결이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="7f691-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f691-122">PARAMETERS</span></span>

### <span data-ttu-id="7f691-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f691-123">-AsJob</span></span>
<span data-ttu-id="7f691-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7f691-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f691-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="7f691-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="7f691-126">이 연결에서 처리해야 하는 대역폭은 mbps입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7f691-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f691-127">-DefaultProfile</span></span>
<span data-ttu-id="7f691-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f691-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7f691-129">-EnableBgp</span></span>
<span data-ttu-id="7f691-130">이 연결에 대해 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="7f691-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7f691-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="7f691-132">이 연결에 대한 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="7f691-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f691-133">-InputObject</span></span>
<span data-ttu-id="7f691-134">업데이트할 VpnConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="7f691-135">-IpSecPolicy</span></span>
<span data-ttu-id="7f691-136">이 연결에서 처리해야 하는 대역폭은 mbps입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="7f691-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7f691-137">-Name</span></span>
<span data-ttu-id="7f691-138">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7f691-139">-ParentResourceName</span></span>
<span data-ttu-id="7f691-140">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f691-141">-ResourceGroupName</span></span>
<span data-ttu-id="7f691-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f691-143">-ResourceId</span></span>
<span data-ttu-id="7f691-144">삭제할 VpnConnection 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-145">-라우팅Configuration</span><span class="sxs-lookup"><span data-stu-id="7f691-145">-RoutingConfiguration</span></span>
<span data-ttu-id="7f691-146">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="7f691-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="7f691-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7f691-147">-SharedKey</span></span>
<span data-ttu-id="7f691-148">이 연결을 설정하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="7f691-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f691-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7f691-150">연결을 시작하는 동안 로컬 Azure IP 주소를 원본 주소로 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="7f691-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7f691-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7f691-152">이 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="7f691-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f691-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="7f691-154">이 VpnConnection에 필요한 VpnSiteLinkConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="7f691-155">-확인</span><span class="sxs-lookup"><span data-stu-id="7f691-155">-Confirm</span></span>
<span data-ttu-id="7f691-156">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f691-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f691-157">-WhatIf</span></span>
<span data-ttu-id="7f691-158">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f691-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f691-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f691-160">CommonParameters</span></span>
<span data-ttu-id="7f691-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f691-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f691-162">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f691-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f691-163">입력</span><span class="sxs-lookup"><span data-stu-id="7f691-163">INPUTS</span></span>

### <span data-ttu-id="7f691-164">System.String</span><span class="sxs-lookup"><span data-stu-id="7f691-164">System.String</span></span>

### <span data-ttu-id="7f691-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7f691-166">출력</span><span class="sxs-lookup"><span data-stu-id="7f691-166">OUTPUTS</span></span>

### <span data-ttu-id="7f691-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="7f691-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f691-168">NOTES</span></span>

## <span data-ttu-id="7f691-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f691-169">RELATED LINKS</span></span>

[<span data-ttu-id="7f691-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="7f691-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="7f691-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7f691-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="7f691-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f691-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
