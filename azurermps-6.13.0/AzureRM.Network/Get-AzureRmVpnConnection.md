---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
ms.openlocfilehash: 7f4ba2cf4a57eedea41eccb8d5846129a80414d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529518"
---
# <span data-ttu-id="49627-101">Get-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="49627-101">Get-AzureRmVpnConnection</span></span>

## <span data-ttu-id="49627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49627-102">SYNOPSIS</span></span>
<span data-ttu-id="49627-103">이름으로 vpn 연결을 가져오거나 VpnGateway에 연결 된 모든 vpn 연결 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49627-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49627-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49627-104">SYNTAX</span></span>

### <span data-ttu-id="49627-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="49627-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49627-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="49627-106">ByVpnGatewayObject</span></span>
```
Get-AzureRmVpnConnection -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49627-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-107">ByVpnGatewayResourceId</span></span>
```
Get-AzureRmVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49627-108">설명은</span><span class="sxs-lookup"><span data-stu-id="49627-108">DESCRIPTION</span></span>
<span data-ttu-id="49627-109">이름으로 vpn 연결을 가져오거나 VpnGateway에 연결 된 모든 vpn 연결 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49627-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="49627-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49627-110">EXAMPLES</span></span>

### <span data-ttu-id="49627-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49627-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

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
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="49627-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49627-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="49627-113">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49627-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="49627-114">게이트웨이가 만들어지면 New-AzureRmVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49627-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="49627-115">그런 다음 연결 이름을 사용 하 여 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49627-115">Then it gets the connection using the connection name.</span></span>

## <span data-ttu-id="49627-116">변수</span><span class="sxs-lookup"><span data-stu-id="49627-116">PARAMETERS</span></span>

### <span data-ttu-id="49627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49627-117">-DefaultProfile</span></span>
<span data-ttu-id="49627-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49627-119">-이름</span><span class="sxs-lookup"><span data-stu-id="49627-119">-Name</span></span>
<span data-ttu-id="49627-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49627-120">The resource name.</span></span>

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

### <span data-ttu-id="49627-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49627-121">-ParentObject</span></span>
<span data-ttu-id="49627-122">이 연결에 대 한 부모 VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="49627-122">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="49627-123">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="49627-123">-ParentResourceId</span></span>
<span data-ttu-id="49627-124">이 연결에 대 한 부모 VpnGateway의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="49627-124">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="49627-125">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="49627-125">-ParentResourceName</span></span>
<span data-ttu-id="49627-126">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49627-126">The parent resource name.</span></span>

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

### <span data-ttu-id="49627-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49627-127">-ResourceGroupName</span></span>
<span data-ttu-id="49627-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49627-128">The resource group name.</span></span>

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

### <span data-ttu-id="49627-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49627-129">CommonParameters</span></span>
<span data-ttu-id="49627-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49627-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49627-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49627-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49627-132">입력</span><span class="sxs-lookup"><span data-stu-id="49627-132">INPUTS</span></span>

### <span data-ttu-id="49627-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49627-133">System.String</span></span>

## <span data-ttu-id="49627-134">출력</span><span class="sxs-lookup"><span data-stu-id="49627-134">OUTPUTS</span></span>

### <span data-ttu-id="49627-135">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49627-135">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="49627-136">상속자</span><span class="sxs-lookup"><span data-stu-id="49627-136">NOTES</span></span>

## <span data-ttu-id="49627-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49627-137">RELATED LINKS</span></span>
