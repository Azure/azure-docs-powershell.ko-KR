---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215940"
---
# <span data-ttu-id="372fb-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="372fb-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="372fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372fb-102">SYNOPSIS</span></span>
<span data-ttu-id="372fb-103">확장 가능한 VPN 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="372fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="372fb-104">SYNTAX</span></span>

### <span data-ttu-id="372fb-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="372fb-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372fb-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="372fb-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372fb-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="372fb-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372fb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="372fb-108">DESCRIPTION</span></span>
<span data-ttu-id="372fb-109">**업데이트 AzVpnGateway** cmdlet은 확장 가능한 VPN 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="372fb-110">Azure VPN 게이트웨이는 VirtualHub 내 사이트 간 연결에 대해 소프트웨어에 정의 된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="372fb-111">이 게이트웨이에는 사용자가 지정한 배율 단위에 따라 크기가 조정 되 고 크기가 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="372fb-112">VPN 사이트 라고 하는 지사/사이트에서 확장 가능한 게이트웨이로의 연결을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="372fb-113">각 연결은 2 개의 Active-Active 터널로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="372fb-114">예제의</span><span class="sxs-lookup"><span data-stu-id="372fb-114">EXAMPLES</span></span>

### <span data-ttu-id="372fb-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="372fb-115">Example 1</span></span>

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

<span data-ttu-id="372fb-116">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="372fb-117">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="372fb-118">게이트웨이를 만든 후에는 Update-AzVpnGateway를 사용 하 여 게이트웨이를 3 단위 단위로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="372fb-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="372fb-119">Example 2</span></span>

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

<span data-ttu-id="372fb-120">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="372fb-121">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="372fb-122">게이트웨이를 만든 후에는 Set-AzVpnGateway를 사용 하 여 BgpPeeringAddress를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="372fb-123">변수</span><span class="sxs-lookup"><span data-stu-id="372fb-123">PARAMETERS</span></span>

### <span data-ttu-id="372fb-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="372fb-124">-AsJob</span></span>
<span data-ttu-id="372fb-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="372fb-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="372fb-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="372fb-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="372fb-127">이 VpnGateway bgpsettings의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

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

### <span data-ttu-id="372fb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="372fb-128">-Confirm</span></span>
<span data-ttu-id="372fb-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372fb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372fb-130">-DefaultProfile</span></span>
<span data-ttu-id="372fb-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372fb-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="372fb-132">-InputObject</span></span>
<span data-ttu-id="372fb-133">수정할 vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="372fb-133">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="372fb-134">-이름</span><span class="sxs-lookup"><span data-stu-id="372fb-134">-Name</span></span>
<span data-ttu-id="372fb-135">Vpn 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-135">The vpn gateway name.</span></span>

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

### <span data-ttu-id="372fb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372fb-136">-ResourceGroupName</span></span>
<span data-ttu-id="372fb-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-137">The resource group name.</span></span>

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

### <span data-ttu-id="372fb-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372fb-138">-ResourceId</span></span>
<span data-ttu-id="372fb-139">수정할 VpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="372fb-140">태그</span><span class="sxs-lookup"><span data-stu-id="372fb-140">-Tag</span></span>
<span data-ttu-id="372fb-141">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="372fb-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="372fb-142">-VpnConnection</span></span>
<span data-ttu-id="372fb-143">이 VpnGateway에 있어야 하는 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="372fb-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="372fb-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="372fb-145">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="372fb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372fb-146">-WhatIf</span></span>
<span data-ttu-id="372fb-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372fb-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372fb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372fb-149">CommonParameters</span></span>
<span data-ttu-id="372fb-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="372fb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372fb-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="372fb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372fb-152">입력</span><span class="sxs-lookup"><span data-stu-id="372fb-152">INPUTS</span></span>

### <span data-ttu-id="372fb-153">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="372fb-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="372fb-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="372fb-154">System.String</span></span>

## <span data-ttu-id="372fb-155">출력</span><span class="sxs-lookup"><span data-stu-id="372fb-155">OUTPUTS</span></span>

### <span data-ttu-id="372fb-156">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="372fb-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="372fb-157">상속자</span><span class="sxs-lookup"><span data-stu-id="372fb-157">NOTES</span></span>

## <span data-ttu-id="372fb-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="372fb-158">RELATED LINKS</span></span>
[<span data-ttu-id="372fb-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="372fb-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="372fb-160">새로운 AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="372fb-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="372fb-161">제거-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="372fb-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)