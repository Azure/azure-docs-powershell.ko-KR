---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215941"
---
# <span data-ttu-id="73cf9-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="73cf9-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="73cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="73cf9-103">VPN 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="73cf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73cf9-104">SYNTAX</span></span>

### <span data-ttu-id="73cf9-105">ByVpnConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="73cf9-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cf9-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="73cf9-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73cf9-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="73cf9-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73cf9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="73cf9-108">DESCRIPTION</span></span>
<span data-ttu-id="73cf9-109">**업데이트 AzVpnConnection** CMDLET은 VPN 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="73cf9-110">Vpn 연결을 통해 vpn 게이트웨이를 Azure에서 VPN 사이트로 표시 되는 원격 고객 분기로 연결 하는 IPsec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="73cf9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="73cf9-111">EXAMPLES</span></span>

### <span data-ttu-id="73cf9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="73cf9-112">Example 1</span></span>

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

<span data-ttu-id="73cf9-113">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="73cf9-114">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="73cf9-115">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="73cf9-116">그런 다음 Set-AzVpnConnection 명령을 사용 하 여 새 정책 정책을 포함 하도록 연결이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="73cf9-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="73cf9-117">Example 2</span></span>

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

<span data-ttu-id="73cf9-118">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="73cf9-119">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="73cf9-120">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="73cf9-121">그런 다음 보안 문자열 구조를 사용 하 여 새 공유 키를 포함 하도록 연결이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="73cf9-122">변수</span><span class="sxs-lookup"><span data-stu-id="73cf9-122">PARAMETERS</span></span>

### <span data-ttu-id="73cf9-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73cf9-123">-AsJob</span></span>
<span data-ttu-id="73cf9-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="73cf9-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73cf9-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="73cf9-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="73cf9-126">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="73cf9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cf9-127">-DefaultProfile</span></span>
<span data-ttu-id="73cf9-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73cf9-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="73cf9-129">-EnableBgp</span></span>
<span data-ttu-id="73cf9-130">이 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="73cf9-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="73cf9-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73cf9-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="73cf9-132">이 연결에 인터넷 보안 설정</span><span class="sxs-lookup"><span data-stu-id="73cf9-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="73cf9-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73cf9-133">-InputObject</span></span>
<span data-ttu-id="73cf9-134">업데이트할 VpnConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="73cf9-135">-정책</span><span class="sxs-lookup"><span data-stu-id="73cf9-135">-IpSecPolicy</span></span>
<span data-ttu-id="73cf9-136">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="73cf9-137">-이름</span><span class="sxs-lookup"><span data-stu-id="73cf9-137">-Name</span></span>
<span data-ttu-id="73cf9-138">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-138">The resource name.</span></span>

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

### <span data-ttu-id="73cf9-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="73cf9-139">-ParentResourceName</span></span>
<span data-ttu-id="73cf9-140">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-140">The parent resource name.</span></span>

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

### <span data-ttu-id="73cf9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73cf9-141">-ResourceGroupName</span></span>
<span data-ttu-id="73cf9-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-142">The resource group name.</span></span>

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

### <span data-ttu-id="73cf9-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73cf9-143">-ResourceId</span></span>
<span data-ttu-id="73cf9-144">삭제할 VpnConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="73cf9-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="73cf9-145">-RoutingConfiguration</span></span>
<span data-ttu-id="73cf9-146">이 연결에 대 한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="73cf9-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="73cf9-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="73cf9-147">-SharedKey</span></span>
<span data-ttu-id="73cf9-148">이 연결을 설정 하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="73cf9-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="73cf9-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="73cf9-150">연결을 시작 하는 동안 로컬 azure ip 주소를 원본 주소로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="73cf9-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="73cf9-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="73cf9-152">이 연결에 정책 기반 트래픽 선택기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="73cf9-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="73cf9-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="73cf9-154">이 VpnConnection에 있어야 하는 VpnSiteLinkConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="73cf9-155">-확인</span><span class="sxs-lookup"><span data-stu-id="73cf9-155">-Confirm</span></span>
<span data-ttu-id="73cf9-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73cf9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cf9-157">-WhatIf</span></span>
<span data-ttu-id="73cf9-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cf9-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73cf9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cf9-160">CommonParameters</span></span>
<span data-ttu-id="73cf9-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73cf9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cf9-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73cf9-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cf9-163">입력</span><span class="sxs-lookup"><span data-stu-id="73cf9-163">INPUTS</span></span>

### <span data-ttu-id="73cf9-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73cf9-164">System.String</span></span>

### <span data-ttu-id="73cf9-165">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73cf9-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="73cf9-166">출력</span><span class="sxs-lookup"><span data-stu-id="73cf9-166">OUTPUTS</span></span>

### <span data-ttu-id="73cf9-167">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73cf9-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="73cf9-168">상속자</span><span class="sxs-lookup"><span data-stu-id="73cf9-168">NOTES</span></span>

## <span data-ttu-id="73cf9-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73cf9-169">RELATED LINKS</span></span>

[<span data-ttu-id="73cf9-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="73cf9-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="73cf9-171">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="73cf9-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="73cf9-172">제거-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="73cf9-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="73cf9-173">새로운 AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="73cf9-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
