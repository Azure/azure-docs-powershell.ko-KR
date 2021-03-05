---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984377"
---
# <span data-ttu-id="746fa-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="746fa-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="746fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="746fa-102">SYNOPSIS</span></span>
<span data-ttu-id="746fa-103">확장 가능한 VPN Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="746fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="746fa-104">SYNTAX</span></span>

### <span data-ttu-id="746fa-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="746fa-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="746fa-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="746fa-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="746fa-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="746fa-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="746fa-108">설명</span><span class="sxs-lookup"><span data-stu-id="746fa-108">DESCRIPTION</span></span>
<span data-ttu-id="746fa-109">New-AzVpnGateway VPN Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="746fa-110">VirtualHub 내부 사이트 연결에 대한 소프트웨어 정의 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="746fa-111">이 게이트웨이는 이 또는 cmdlet에 지정된 확장 단위를 Set-AzVpnGateway 크기 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="746fa-112">연결은 VPNSite라고 하는 분기/사이트에서 확장 가능한 게이트웨이로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="746fa-113">각 연결은 2개의 Active-Active 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="746fa-114">VpnGateway는 참조된 VirtualHub와 동일한 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="746fa-115">예제</span><span class="sxs-lookup"><span data-stu-id="746fa-115">EXAMPLES</span></span>

### <span data-ttu-id="746fa-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="746fa-116">Example 1</span></span>
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

<span data-ttu-id="746fa-117">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="746fa-118">2개 확장 단위가 있는 Virtual Hub에서 VPN 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="746fa-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="746fa-119">PARAMETERS</span></span>

### <span data-ttu-id="746fa-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="746fa-120">-AsJob</span></span>
<span data-ttu-id="746fa-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="746fa-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="746fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746fa-122">-DefaultProfile</span></span>
<span data-ttu-id="746fa-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746fa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="746fa-124">-Name</span></span>
<span data-ttu-id="746fa-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-125">The resource name.</span></span>

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

### <span data-ttu-id="746fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="746fa-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-127">The resource name.</span></span>

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

### <span data-ttu-id="746fa-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="746fa-128">-Tag</span></span>
<span data-ttu-id="746fa-129">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="746fa-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="746fa-130">-VirtualHub</span></span>
<span data-ttu-id="746fa-131">VirtualHub 이 VpnGateway를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="746fa-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="746fa-132">-VirtualHubId</span></span>
<span data-ttu-id="746fa-133">VirtualHub 이 VpnGateway의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="746fa-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="746fa-134">-VirtualHubName</span></span>
<span data-ttu-id="746fa-135">VirtualHub 이 VpnGateway의 ID를 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="746fa-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="746fa-136">-VpnConnection</span></span>
<span data-ttu-id="746fa-137">이 VpnGateway에 필요한 VpnConnections 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="746fa-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="746fa-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="746fa-139">이 VpnGateway와 연결된 VpnGatewayNatRules 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="746fa-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="746fa-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="746fa-141">이 VpnGateway의 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-141">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="746fa-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="746fa-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="746fa-143">이 VpnGateway에서 라우팅 기본 설정 인터넷을 사용하도록 설정하려면 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="746fa-144">-확인</span><span class="sxs-lookup"><span data-stu-id="746fa-144">-Confirm</span></span>
<span data-ttu-id="746fa-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746fa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746fa-146">-WhatIf</span></span>
<span data-ttu-id="746fa-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746fa-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746fa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746fa-149">CommonParameters</span></span>
<span data-ttu-id="746fa-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="746fa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746fa-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746fa-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746fa-152">입력</span><span class="sxs-lookup"><span data-stu-id="746fa-152">INPUTS</span></span>

### <span data-ttu-id="746fa-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="746fa-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="746fa-154">System.String</span><span class="sxs-lookup"><span data-stu-id="746fa-154">System.String</span></span>
## <span data-ttu-id="746fa-155">출력</span><span class="sxs-lookup"><span data-stu-id="746fa-155">OUTPUTS</span></span>

### <span data-ttu-id="746fa-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="746fa-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="746fa-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="746fa-157">NOTES</span></span>

## <span data-ttu-id="746fa-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="746fa-158">RELATED LINKS</span></span>

[<span data-ttu-id="746fa-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="746fa-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="746fa-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="746fa-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="746fa-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="746fa-161">Update-AzVpnGateway</span></span>]()

