---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 75942fa57681b046028e196b0438d8633e1cd3df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179561"
---
# <span data-ttu-id="db9fc-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="db9fc-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="db9fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="db9fc-103">확장 가능한 VPN Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="db9fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="db9fc-104">SYNTAX</span></span>

### <span data-ttu-id="db9fc-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="db9fc-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db9fc-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="db9fc-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db9fc-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="db9fc-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db9fc-108">설명</span><span class="sxs-lookup"><span data-stu-id="db9fc-108">DESCRIPTION</span></span>
<span data-ttu-id="db9fc-109">New-AzVpnGateway VPN Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="db9fc-110">VirtualHub 내에서 사이트와 사이트 연결을 위한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="db9fc-111">이 게이트웨이는 이 또는 이 cmdlet에 지정된 배율 단위에 따라 Set-AzVpnGateway 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="db9fc-112">VPNSite라고 하는 분기/사이트에서 확장 가능한 게이트웨이로 연결이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="db9fc-113">각 연결은 2개의 터널로 Active-Active 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="db9fc-114">VpnGateway는 참조된 VirtualHub와 동일한 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="db9fc-115">예제</span><span class="sxs-lookup"><span data-stu-id="db9fc-115">EXAMPLES</span></span>

### <span data-ttu-id="db9fc-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="db9fc-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="db9fc-117">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="db9fc-118">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="db9fc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db9fc-119">PARAMETERS</span></span>

### <span data-ttu-id="db9fc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db9fc-120">-AsJob</span></span>
<span data-ttu-id="db9fc-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="db9fc-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9fc-122">-DefaultProfile</span></span>
<span data-ttu-id="db9fc-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db9fc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="db9fc-124">-Name</span></span>
<span data-ttu-id="db9fc-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db9fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="db9fc-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="db9fc-128">-Tag</span></span>
<span data-ttu-id="db9fc-129">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="db9fc-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="db9fc-130">-VirtualHub</span></span>
<span data-ttu-id="db9fc-131">이 VpnGateway를 VirtualHub에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="db9fc-132">-VirtualHubId</span></span>
<span data-ttu-id="db9fc-133">이 VpnGateway를 연결해야 하는 VirtualHub의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="db9fc-134">-VirtualHubName</span></span>
<span data-ttu-id="db9fc-135">이 VpnGateway를 연결해야 하는 VirtualHub의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="db9fc-136">-VpnConnection</span></span>
<span data-ttu-id="db9fc-137">이 VpnGateway에 필요한 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="db9fc-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="db9fc-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="db9fc-139">이 VpnGateway와 연결된 VpnGatewayNatRules 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="db9fc-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="db9fc-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="db9fc-141">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="db9fc-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="db9fc-143">이 VpnGateway에서 라우팅 기본 설정 인터넷을 사용하도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="db9fc-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db9fc-144">-Confirm</span></span>
<span data-ttu-id="db9fc-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9fc-146">-WhatIf</span></span>
<span data-ttu-id="db9fc-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="db9fc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db9fc-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9fc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9fc-149">CommonParameters</span></span>
<span data-ttu-id="db9fc-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db9fc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9fc-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db9fc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9fc-152">입력</span><span class="sxs-lookup"><span data-stu-id="db9fc-152">INPUTS</span></span>

### <span data-ttu-id="db9fc-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="db9fc-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="db9fc-154">System.String</span><span class="sxs-lookup"><span data-stu-id="db9fc-154">System.String</span></span>
## <span data-ttu-id="db9fc-155">출력</span><span class="sxs-lookup"><span data-stu-id="db9fc-155">OUTPUTS</span></span>

### <span data-ttu-id="db9fc-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="db9fc-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="db9fc-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db9fc-157">NOTES</span></span>

## <span data-ttu-id="db9fc-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db9fc-158">RELATED LINKS</span></span>

[<span data-ttu-id="db9fc-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="db9fc-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="db9fc-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="db9fc-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="db9fc-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="db9fc-161">Update-AzVpnGateway</span></span>]()

