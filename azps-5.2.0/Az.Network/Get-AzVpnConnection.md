---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 6ad7f5fcdaafed47d7292444370e332188f444b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369902"
---
# <span data-ttu-id="31124-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="31124-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="31124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31124-102">SYNOPSIS</span></span>
<span data-ttu-id="31124-103">이름으로 VPN 연결을 얻거나 VpnGateway에 연결된 모든 VPN 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="31124-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="31124-104">구문</span><span class="sxs-lookup"><span data-stu-id="31124-104">SYNTAX</span></span>

### <span data-ttu-id="31124-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="31124-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31124-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="31124-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31124-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="31124-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31124-108">설명</span><span class="sxs-lookup"><span data-stu-id="31124-108">DESCRIPTION</span></span>
<span data-ttu-id="31124-109">이름으로 VPN 연결을 얻거나 VpnGateway에 연결된 모든 VPN 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="31124-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="31124-110">예제</span><span class="sxs-lookup"><span data-stu-id="31124-110">EXAMPLES</span></span>

### <span data-ttu-id="31124-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="31124-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
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

<span data-ttu-id="31124-112">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부에 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 VpnSite가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="31124-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="31124-113">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="31124-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="31124-114">게이트웨이를 만든 후 New-AzVpnConnection 명령을 사용하여 VpnSite에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="31124-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="31124-115">그런 다음 연결 이름을 사용하여 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31124-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="31124-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="31124-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
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

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
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

<span data-ttu-id="31124-117">이 cmdlet은 "test"로 시작하는 모든 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31124-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="31124-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31124-118">PARAMETERS</span></span>

### <span data-ttu-id="31124-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31124-119">-DefaultProfile</span></span>
<span data-ttu-id="31124-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31124-121">-Name</span><span class="sxs-lookup"><span data-stu-id="31124-121">-Name</span></span>
<span data-ttu-id="31124-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31124-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31124-123">-ParentObject</span></span>
<span data-ttu-id="31124-124">이 연결에 대한 부모 VpnGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31124-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="31124-125">-ParentResourceId</span></span>
<span data-ttu-id="31124-126">이 연결에 대한 부모 VpnGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31124-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="31124-127">-ParentResourceName</span></span>
<span data-ttu-id="31124-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31124-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31124-129">-ResourceGroupName</span></span>
<span data-ttu-id="31124-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31124-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31124-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31124-131">CommonParameters</span></span>
<span data-ttu-id="31124-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31124-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31124-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31124-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31124-134">입력</span><span class="sxs-lookup"><span data-stu-id="31124-134">INPUTS</span></span>

### <span data-ttu-id="31124-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="31124-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="31124-136">System.String</span><span class="sxs-lookup"><span data-stu-id="31124-136">System.String</span></span>

## <span data-ttu-id="31124-137">출력</span><span class="sxs-lookup"><span data-stu-id="31124-137">OUTPUTS</span></span>

### <span data-ttu-id="31124-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="31124-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="31124-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31124-139">NOTES</span></span>

## <span data-ttu-id="31124-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31124-140">RELATED LINKS</span></span>

[<span data-ttu-id="31124-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="31124-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="31124-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="31124-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="31124-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="31124-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
