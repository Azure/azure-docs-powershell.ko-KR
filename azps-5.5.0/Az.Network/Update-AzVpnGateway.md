---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: b38108a9655378349efff44bae3e51efc3ce1f7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186801"
---
# <span data-ttu-id="e2920-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="e2920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2920-102">SYNOPSIS</span></span>
<span data-ttu-id="e2920-103">확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="e2920-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2920-104">SYNTAX</span></span>

### <span data-ttu-id="e2920-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2920-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2920-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e2920-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2920-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e2920-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2920-108">설명</span><span class="sxs-lookup"><span data-stu-id="e2920-108">DESCRIPTION</span></span>
<span data-ttu-id="e2920-109">**Update-AzVpnGateway** cmdlet은 확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="e2920-110">Azure VPN Gateway는 VirtualHub 내에서 사이트와 사이트 연결을 위한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="e2920-111">이 게이트웨이는 사용자가 지정한 배율 단위에 따라 크기 조정 및 크기 조정</span><span class="sxs-lookup"><span data-stu-id="e2920-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="e2920-112">VPN 사이트라고 하는 분기/사이트에서 확장 가능한 게이트웨이로 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="e2920-113">각 연결은 2개의 Active-Active 터널로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="e2920-114">예제</span><span class="sxs-lookup"><span data-stu-id="e2920-114">EXAMPLES</span></span>

### <span data-ttu-id="e2920-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2920-115">Example 1</span></span>

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

<span data-ttu-id="e2920-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e2920-117">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e2920-118">게이트웨이를 만든 후 게이트웨이를 Update-AzVpnGateway 3개 배율 단위로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="e2920-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="e2920-119">Example 2</span></span>

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

<span data-ttu-id="e2920-120">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e2920-121">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e2920-122">게이트웨이를 만든 후 게이트웨이를 사용하여 Set-AzVpnGateway BgpPeeringAddress를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="e2920-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2920-123">PARAMETERS</span></span>

### <span data-ttu-id="e2920-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2920-124">-AsJob</span></span>
<span data-ttu-id="e2920-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e2920-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2920-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e2920-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="e2920-127">이 VpnGateway bgpsettings에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2920-128">-DefaultProfile</span></span>
<span data-ttu-id="e2920-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2920-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2920-130">-InputObject</span></span>
<span data-ttu-id="e2920-131">수정할 vpn gateway 개체</span><span class="sxs-lookup"><span data-stu-id="e2920-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e2920-132">-Name</span></span>
<span data-ttu-id="e2920-133">VPN 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2920-134">-ResourceGroupName</span></span>
<span data-ttu-id="e2920-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-135">The resource group name.</span></span>

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

### <span data-ttu-id="e2920-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2920-136">-ResourceId</span></span>
<span data-ttu-id="e2920-137">수정할 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2920-138">-Tag</span></span>
<span data-ttu-id="e2920-139">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e2920-140">-VpnConnection</span></span>
<span data-ttu-id="e2920-141">이 VpnGateway에 필요한 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="e2920-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="e2920-143">이 VpnGateway와 연결된 VpnGatewayNatRules 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e2920-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="e2920-145">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="e2920-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2920-146">-Confirm</span></span>
<span data-ttu-id="e2920-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2920-148">-WhatIf</span></span>
<span data-ttu-id="e2920-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2920-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2920-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2920-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2920-151">CommonParameters</span></span>
<span data-ttu-id="e2920-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2920-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2920-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2920-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2920-154">입력</span><span class="sxs-lookup"><span data-stu-id="e2920-154">INPUTS</span></span>

### <span data-ttu-id="e2920-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e2920-156">System.String</span><span class="sxs-lookup"><span data-stu-id="e2920-156">System.String</span></span>

## <span data-ttu-id="e2920-157">출력</span><span class="sxs-lookup"><span data-stu-id="e2920-157">OUTPUTS</span></span>

### <span data-ttu-id="e2920-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="e2920-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2920-159">NOTES</span></span>

## <span data-ttu-id="e2920-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2920-160">RELATED LINKS</span></span>

[<span data-ttu-id="e2920-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="e2920-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="e2920-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e2920-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)