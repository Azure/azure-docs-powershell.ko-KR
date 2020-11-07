---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 85b6472cd6dd99210e188f6fc9b66ba4b00e3198
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870029"
---
# <span data-ttu-id="d89db-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d89db-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="d89db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89db-102">SYNOPSIS</span></span>
<span data-ttu-id="d89db-103">이름으로 vpn 연결을 가져오거나 VpnGateway에 연결 된 모든 vpn 연결 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="d89db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d89db-104">SYNTAX</span></span>

### <span data-ttu-id="d89db-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d89db-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d89db-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d89db-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d89db-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d89db-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d89db-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d89db-108">DESCRIPTION</span></span>
<span data-ttu-id="d89db-109">이름으로 vpn 연결을 가져오거나 VpnGateway에 연결 된 모든 vpn 연결 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="d89db-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d89db-110">EXAMPLES</span></span>

### <span data-ttu-id="d89db-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d89db-111">Example 1</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="d89db-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d89db-113">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d89db-114">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="d89db-115">그런 다음 연결 이름을 사용 하 여 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="d89db-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="d89db-116">Example 2</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="d89db-117">이 cmdlet은 "test"로 시작 하는 모든 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="d89db-118">변수</span><span class="sxs-lookup"><span data-stu-id="d89db-118">PARAMETERS</span></span>

### <span data-ttu-id="d89db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89db-119">-DefaultProfile</span></span>
<span data-ttu-id="d89db-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d89db-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d89db-121">-Name</span></span>
<span data-ttu-id="d89db-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-122">The resource name.</span></span>

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

### <span data-ttu-id="d89db-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d89db-123">-ParentObject</span></span>
<span data-ttu-id="d89db-124">이 연결에 대 한 부모 VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d89db-124">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="d89db-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d89db-125">-ParentResourceId</span></span>
<span data-ttu-id="d89db-126">이 연결에 대 한 부모 VpnGateway의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-126">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="d89db-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d89db-127">-ParentResourceName</span></span>
<span data-ttu-id="d89db-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-128">The parent resource name.</span></span>

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

### <span data-ttu-id="d89db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d89db-129">-ResourceGroupName</span></span>
<span data-ttu-id="d89db-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-130">The resource group name.</span></span>

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

### <span data-ttu-id="d89db-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89db-131">CommonParameters</span></span>
<span data-ttu-id="d89db-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d89db-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89db-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d89db-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89db-134">입력</span><span class="sxs-lookup"><span data-stu-id="d89db-134">INPUTS</span></span>

### <span data-ttu-id="d89db-135">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d89db-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d89db-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d89db-136">System.String</span></span>

## <span data-ttu-id="d89db-137">출력</span><span class="sxs-lookup"><span data-stu-id="d89db-137">OUTPUTS</span></span>

### <span data-ttu-id="d89db-138">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d89db-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="d89db-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d89db-139">NOTES</span></span>

## <span data-ttu-id="d89db-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d89db-140">RELATED LINKS</span></span>

[<span data-ttu-id="d89db-141">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d89db-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="d89db-142">제거-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d89db-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="d89db-143">업데이트-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d89db-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
