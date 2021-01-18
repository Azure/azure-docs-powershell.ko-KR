---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495076"
---
# <span data-ttu-id="1c032-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="1c032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c032-102">SYNOPSIS</span></span>
<span data-ttu-id="1c032-103">확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="1c032-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c032-104">SYNTAX</span></span>

### <span data-ttu-id="1c032-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c032-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c032-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1c032-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c032-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="1c032-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c032-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c032-108">DESCRIPTION</span></span>
<span data-ttu-id="1c032-109">**Update-AzVpnGateway** cmdlet은 확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="1c032-110">Azure VPN Gateway는 VirtualHub 내에서 사이트와 사이트 연결을 위한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="1c032-111">이 게이트웨이는 사용자가 지정한 배율 단위에 따라 크기 조정 및 크기 조정</span><span class="sxs-lookup"><span data-stu-id="1c032-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="1c032-112">VPN 사이트라고 하는 분기/사이트에서 확장 가능한 게이트웨이로 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="1c032-113">각 연결은 2개의 Active-Active 터널로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="1c032-114">예제</span><span class="sxs-lookup"><span data-stu-id="1c032-114">EXAMPLES</span></span>

### <span data-ttu-id="1c032-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c032-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="1c032-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1c032-117">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1c032-118">게이트웨이를 만든 후 게이트웨이를 Update-AzVpnGateway 3개 배율 단위로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="1c032-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c032-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="1c032-120">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1c032-121">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1c032-122">게이트웨이를 만든 후 게이트웨이를 사용하여 Set-AzVpnGateway BgpPeeringAddress를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="1c032-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c032-123">PARAMETERS</span></span>

### <span data-ttu-id="1c032-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c032-124">-AsJob</span></span>
<span data-ttu-id="1c032-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1c032-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c032-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1c032-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="1c032-127">이 VpnGateway bgpsettings에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c032-128">-Confirm</span></span>
<span data-ttu-id="1c032-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c032-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c032-130">-DefaultProfile</span></span>
<span data-ttu-id="1c032-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c032-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c032-132">-InputObject</span></span>
<span data-ttu-id="1c032-133">수정할 vpn gateway 개체</span><span class="sxs-lookup"><span data-stu-id="1c032-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1c032-134">-Name</span></span>
<span data-ttu-id="1c032-135">VPN 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c032-136">-ResourceGroupName</span></span>
<span data-ttu-id="1c032-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c032-138">-ResourceId</span></span>
<span data-ttu-id="1c032-139">수정할 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c032-140">-Tag</span></span>
<span data-ttu-id="1c032-141">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1c032-142">-VpnConnection</span></span>
<span data-ttu-id="1c032-143">이 VpnGateway에 필요한 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c032-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1c032-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="1c032-145">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="1c032-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c032-146">-WhatIf</span></span>
<span data-ttu-id="1c032-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c032-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c032-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c032-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c032-149">CommonParameters</span></span>
<span data-ttu-id="1c032-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c032-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c032-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c032-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c032-152">입력</span><span class="sxs-lookup"><span data-stu-id="1c032-152">INPUTS</span></span>

### <span data-ttu-id="1c032-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="1c032-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1c032-154">System.String</span></span>

## <span data-ttu-id="1c032-155">출력</span><span class="sxs-lookup"><span data-stu-id="1c032-155">OUTPUTS</span></span>

### <span data-ttu-id="1c032-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="1c032-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c032-157">NOTES</span></span>

## <span data-ttu-id="1c032-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c032-158">RELATED LINKS</span></span>
[<span data-ttu-id="1c032-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="1c032-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="1c032-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1c032-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)