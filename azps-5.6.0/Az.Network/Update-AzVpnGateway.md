---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: d04c665bce4c37425564e4eb65ff46da3b39fa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951456"
---
# <span data-ttu-id="c064f-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="c064f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c064f-102">SYNOPSIS</span></span>
<span data-ttu-id="c064f-103">확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="c064f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c064f-104">SYNTAX</span></span>

### <span data-ttu-id="c064f-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c064f-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c064f-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c064f-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c064f-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c064f-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c064f-108">설명</span><span class="sxs-lookup"><span data-stu-id="c064f-108">DESCRIPTION</span></span>
<span data-ttu-id="c064f-109">**Update-AzVpnGateway** cmdlet은 확장 가능한 VPN 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="c064f-110">Azure VPN 게이트웨이는 VirtualHub 내부 사이트 연결에 대한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="c064f-111">이 게이트웨이는 사용자가 지정한 크기 단위에 따라 크기 조정 및 크기 조정</span><span class="sxs-lookup"><span data-stu-id="c064f-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="c064f-112">VPN 사이트라고 하는 분기/사이트에서 확장 가능한 게이트웨이로 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="c064f-113">각 연결은 2개의 Active-Active 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="c064f-114">예제</span><span class="sxs-lookup"><span data-stu-id="c064f-114">EXAMPLES</span></span>

### <span data-ttu-id="c064f-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="c064f-115">Example 1</span></span>

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

<span data-ttu-id="c064f-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c064f-117">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c064f-118">게이트웨이를 만든 후 게이트웨이를 Update-AzVpnGateway 3개 확장 단위로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="c064f-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="c064f-119">Example 2</span></span>

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

<span data-ttu-id="c064f-120">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c064f-121">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c064f-122">게이트웨이를 만든 후 BgpPeeringAddress를 Set-AzVpnGateway 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="c064f-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c064f-123">PARAMETERS</span></span>

### <span data-ttu-id="c064f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c064f-124">-AsJob</span></span>
<span data-ttu-id="c064f-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c064f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c064f-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c064f-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="c064f-127">이 VpnGateway bgpsettings에 대한 BGP 피어링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

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

### <span data-ttu-id="c064f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c064f-128">-DefaultProfile</span></span>
<span data-ttu-id="c064f-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c064f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c064f-130">-InputObject</span></span>
<span data-ttu-id="c064f-131">수정할 VPN 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="c064f-131">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="c064f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c064f-132">-Name</span></span>
<span data-ttu-id="c064f-133">VPN 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-133">The vpn gateway name.</span></span>

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

### <span data-ttu-id="c064f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c064f-134">-ResourceGroupName</span></span>
<span data-ttu-id="c064f-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-135">The resource group name.</span></span>

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

### <span data-ttu-id="c064f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c064f-136">-ResourceId</span></span>
<span data-ttu-id="c064f-137">수정할 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="c064f-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="c064f-138">-Tag</span></span>
<span data-ttu-id="c064f-139">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c064f-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c064f-140">-VpnConnection</span></span>
<span data-ttu-id="c064f-141">이 VpnGateway에 필요한 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="c064f-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c064f-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="c064f-143">이 VpnGateway와 연결된 VpnGatewayNatRules 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="c064f-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c064f-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="c064f-145">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="c064f-146">-확인</span><span class="sxs-lookup"><span data-stu-id="c064f-146">-Confirm</span></span>
<span data-ttu-id="c064f-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c064f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c064f-148">-WhatIf</span></span>
<span data-ttu-id="c064f-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c064f-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c064f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c064f-151">CommonParameters</span></span>
<span data-ttu-id="c064f-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c064f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c064f-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c064f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c064f-154">입력</span><span class="sxs-lookup"><span data-stu-id="c064f-154">INPUTS</span></span>

### <span data-ttu-id="c064f-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c064f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="c064f-156">System.String</span></span>

## <span data-ttu-id="c064f-157">출력</span><span class="sxs-lookup"><span data-stu-id="c064f-157">OUTPUTS</span></span>

### <span data-ttu-id="c064f-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="c064f-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c064f-159">NOTES</span></span>

## <span data-ttu-id="c064f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c064f-160">RELATED LINKS</span></span>

[<span data-ttu-id="c064f-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c064f-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="c064f-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c064f-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)