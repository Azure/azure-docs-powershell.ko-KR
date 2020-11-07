---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: e62e697deec0d7e3894e7eaf787790f64d72641b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871317"
---
# <span data-ttu-id="18cc0-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="18cc0-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="18cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="18cc0-103">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="18cc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18cc0-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18cc0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="18cc0-106">Azure VpnSiteLinkConnection 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="18cc0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="18cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="18cc0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="18cc0-108">Example 1</span></span>
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

<span data-ttu-id="18cc0-109">위의 작업을 통해 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브, Azure의 "testRG" 리소스 그룹에 VpnSiteLinks 1 인 "VpnSite"를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="18cc0-110">가상 허브에서 VPN 게이트웨이는 이후에 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="18cc0-111">게이트웨이가 만들어지면 VpnSite의 VpnSiteLink에 대 한 1 VpnSiteLinkConnections New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="18cc0-112">변수</span><span class="sxs-lookup"><span data-stu-id="18cc0-112">PARAMETERS</span></span>

### <span data-ttu-id="18cc0-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="18cc0-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="18cc0-114">이 링크 연결에서 처리 해야 하는 대역폭 (mbps 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="18cc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cc0-115">-DefaultProfile</span></span>
<span data-ttu-id="18cc0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18cc0-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="18cc0-117">-EnableBgp</span></span>
<span data-ttu-id="18cc0-118">이 링크 연결에 BGP 사용</span><span class="sxs-lookup"><span data-stu-id="18cc0-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="18cc0-119">-정책</span><span class="sxs-lookup"><span data-stu-id="18cc0-119">-IpSecPolicy</span></span>
<span data-ttu-id="18cc0-120">이 링크 연결에 대해 고려할 IpSec 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="18cc0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="18cc0-121">-Name</span></span>
<span data-ttu-id="18cc0-122">성을</span><span class="sxs-lookup"><span data-stu-id="18cc0-122">Name</span></span>

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

### <span data-ttu-id="18cc0-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="18cc0-123">-RoutingWeight</span></span>
<span data-ttu-id="18cc0-124">라우팅 가중치</span><span class="sxs-lookup"><span data-stu-id="18cc0-124">Routing Weight</span></span>

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

### <span data-ttu-id="18cc0-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="18cc0-125">-SharedKey</span></span>
<span data-ttu-id="18cc0-126">이 링크 연결을 설정 하는 데 필요한 공유 키입니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="18cc0-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="18cc0-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="18cc0-128">로컬 azure ip 주소를이 링크 연결에 대 한 원본 ip로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="18cc0-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="18cc0-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="18cc0-130">이 링크 연결에 정책 기반 트래픽 선택기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="18cc0-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="18cc0-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="18cc0-132">게이트웨이 연결 프로토콜: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="18cc0-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="18cc0-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="18cc0-133">-VpnSiteLink</span></span>
<span data-ttu-id="18cc0-134">연결할 vpn 사이트 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="18cc0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cc0-135">CommonParameters</span></span>
<span data-ttu-id="18cc0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18cc0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cc0-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18cc0-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cc0-138">입력</span><span class="sxs-lookup"><span data-stu-id="18cc0-138">INPUTS</span></span>

### <span data-ttu-id="18cc0-139">PSVpnSiteLink에 대 한.</span><span class="sxs-lookup"><span data-stu-id="18cc0-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="18cc0-140">출력</span><span class="sxs-lookup"><span data-stu-id="18cc0-140">OUTPUTS</span></span>

### <span data-ttu-id="18cc0-141">PSVpnSiteLinkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="18cc0-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="18cc0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="18cc0-142">NOTES</span></span>

## <span data-ttu-id="18cc0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18cc0-143">RELATED LINKS</span></span>

[<span data-ttu-id="18cc0-144">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="18cc0-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)