---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044511"
---
# <span data-ttu-id="313d3-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="313d3-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="313d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="313d3-102">SYNOPSIS</span></span>
<span data-ttu-id="313d3-103">VPN 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="313d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="313d3-104">SYNTAX</span></span>

### <span data-ttu-id="313d3-105">ByVpnConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="313d3-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313d3-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="313d3-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="313d3-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="313d3-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313d3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="313d3-108">DESCRIPTION</span></span>
<span data-ttu-id="313d3-109">**업데이트 AzVpnConnection** CMDLET은 VPN 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="313d3-110">Vpn 연결을 통해 vpn 게이트웨이를 Azure에서 VPN 사이트로 표시 되는 원격 고객 분기로 연결 하는 IPsec 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="313d3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="313d3-111">EXAMPLES</span></span>

### <span data-ttu-id="313d3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="313d3-112">Example 1</span></span>

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
```

<span data-ttu-id="313d3-113">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="313d3-114">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="313d3-115">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="313d3-116">그런 다음 Set-AzVpnConnection 명령을 사용 하 여 새 정책 정책을 포함 하도록 연결이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="313d3-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="313d3-117">Example 2</span></span>

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
```

<span data-ttu-id="313d3-118">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="313d3-119">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="313d3-120">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="313d3-121">그런 다음 보안 문자열 구조를 사용 하 여 새 공유 키를 포함 하도록 연결이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="313d3-122">변수</span><span class="sxs-lookup"><span data-stu-id="313d3-122">PARAMETERS</span></span>

### <span data-ttu-id="313d3-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="313d3-123">-AsJob</span></span>
<span data-ttu-id="313d3-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="313d3-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="313d3-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="313d3-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="313d3-126">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="313d3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313d3-127">-DefaultProfile</span></span>
<span data-ttu-id="313d3-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313d3-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="313d3-129">-EnableBgp</span></span>
<span data-ttu-id="313d3-130">이 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="313d3-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="313d3-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="313d3-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="313d3-132">이 연결에 인터넷 보안 설정</span><span class="sxs-lookup"><span data-stu-id="313d3-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="313d3-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313d3-133">-InputObject</span></span>
<span data-ttu-id="313d3-134">업데이트할 VpnConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="313d3-135">-정책</span><span class="sxs-lookup"><span data-stu-id="313d3-135">-IpSecPolicy</span></span>
<span data-ttu-id="313d3-136">Mbps 단위로이 연결을 처리 해야 하는 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="313d3-137">-이름</span><span class="sxs-lookup"><span data-stu-id="313d3-137">-Name</span></span>
<span data-ttu-id="313d3-138">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-138">The resource name.</span></span>

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

### <span data-ttu-id="313d3-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="313d3-139">-ParentResourceName</span></span>
<span data-ttu-id="313d3-140">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-140">The parent resource name.</span></span>

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

### <span data-ttu-id="313d3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313d3-141">-ResourceGroupName</span></span>
<span data-ttu-id="313d3-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-142">The resource group name.</span></span>

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

### <span data-ttu-id="313d3-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="313d3-143">-ResourceId</span></span>
<span data-ttu-id="313d3-144">삭제할 VpnConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="313d3-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="313d3-145">-SharedKey</span></span>
<span data-ttu-id="313d3-146">이 연결을 설정 하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="313d3-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="313d3-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="313d3-148">연결을 시작 하는 동안 로컬 azure ip 주소를 원본 주소로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="313d3-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="313d3-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="313d3-150">이 연결에 정책 기반 트래픽 선택기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="313d3-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="313d3-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="313d3-152">이 VpnConnection에 있어야 하는 VpnSiteLinkConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="313d3-153">-확인</span><span class="sxs-lookup"><span data-stu-id="313d3-153">-Confirm</span></span>
<span data-ttu-id="313d3-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313d3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313d3-155">-WhatIf</span></span>
<span data-ttu-id="313d3-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313d3-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313d3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313d3-158">CommonParameters</span></span>
<span data-ttu-id="313d3-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="313d3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313d3-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="313d3-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313d3-161">입력</span><span class="sxs-lookup"><span data-stu-id="313d3-161">INPUTS</span></span>

### <span data-ttu-id="313d3-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="313d3-162">System.String</span></span>

### <span data-ttu-id="313d3-163">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="313d3-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="313d3-164">출력</span><span class="sxs-lookup"><span data-stu-id="313d3-164">OUTPUTS</span></span>

### <span data-ttu-id="313d3-165">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="313d3-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="313d3-166">상속자</span><span class="sxs-lookup"><span data-stu-id="313d3-166">NOTES</span></span>

## <span data-ttu-id="313d3-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="313d3-167">RELATED LINKS</span></span>

[<span data-ttu-id="313d3-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="313d3-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="313d3-169">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="313d3-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="313d3-170">제거-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="313d3-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
