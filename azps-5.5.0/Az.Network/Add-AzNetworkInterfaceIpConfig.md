---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207040"
---
# <span data-ttu-id="99fe0-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="99fe0-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="99fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="99fe0-103">네트워크 인터페이스 IP 구성을 네트워크 인터페이스에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="99fe0-104">구문</span><span class="sxs-lookup"><span data-stu-id="99fe0-104">SYNTAX</span></span>

### <span data-ttu-id="99fe0-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="99fe0-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99fe0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="99fe0-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99fe0-107">설명</span><span class="sxs-lookup"><span data-stu-id="99fe0-107">DESCRIPTION</span></span>
<span data-ttu-id="99fe0-108">**Add-AzNetworkInterfaceIpConfig** cmdlet은 Azure 네트워크 인터페이스에 네트워크 인터페이스 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="99fe0-109">예제</span><span class="sxs-lookup"><span data-stu-id="99fe0-109">EXAMPLES</span></span>

### <span data-ttu-id="99fe0-110">예제 1: 애플리케이션 보안 그룹을 통해 새 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="99fe0-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="99fe0-111">이 예제에서는 새 가상 네트워크 MyVNET의 서브넷에 속하는 새 네트워크 인터페이스 MyNetworkInterface를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="99fe0-112">또한 네트워크 인터페이스의 IP 구성과 연결하기 위해 빈 애플리케이션 보안 그룹 MyASG를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="99fe0-113">두 개체가 모두 만들어지면 기본 IP 구성을 MyASG 개체에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="99fe0-114">마지막으로 애플리케이션 보안 그룹 개체에 연결된 네트워크 인터페이스에서 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="99fe0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99fe0-115">PARAMETERS</span></span>

### <span data-ttu-id="99fe0-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="99fe0-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="99fe0-117">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="99fe0-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="99fe0-119">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="99fe0-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="99fe0-121">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="99fe0-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="99fe0-123">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fe0-124">-DefaultProfile</span></span>
<span data-ttu-id="99fe0-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99fe0-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="99fe0-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="99fe0-127">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="99fe0-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="99fe0-129">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백end 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="99fe0-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="99fe0-131">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 인바운드 NAT(네트워크 주소 변환) 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="99fe0-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="99fe0-133">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 인바운드 NAT 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="99fe0-134">-Name</span></span>
<span data-ttu-id="99fe0-135">네트워크 인터페이스 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="99fe0-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="99fe0-136">-NetworkInterface</span></span>
<span data-ttu-id="99fe0-137">**NetworkInterface 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="99fe0-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="99fe0-138">이 cmdlet은 이 매개 변수가 지정하는 개체에 네트워크 인터페이스 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="99fe0-139">-Primary</span></span>
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

### <span data-ttu-id="99fe0-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="99fe0-140">-PrivateIpAddress</span></span>
<span data-ttu-id="99fe0-141">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-141">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="99fe0-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="99fe0-143">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="99fe0-144">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="99fe0-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99fe0-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="99fe0-145">IPv4</span></span>
- <span data-ttu-id="99fe0-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="99fe0-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="99fe0-147">-PublicIpAddress</span></span>
<span data-ttu-id="99fe0-148">**PublicIPAddress 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="99fe0-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="99fe0-149">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="99fe0-150">-PublicIpAddressId</span></span>
<span data-ttu-id="99fe0-151">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="99fe0-152">-Subnet</span></span>
<span data-ttu-id="99fe0-153">서브넷 개체를 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="99fe0-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="99fe0-154">이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99fe0-155">-SubnetId</span></span>
<span data-ttu-id="99fe0-156">이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fe0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fe0-157">CommonParameters</span></span>
<span data-ttu-id="99fe0-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99fe0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fe0-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99fe0-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fe0-160">입력</span><span class="sxs-lookup"><span data-stu-id="99fe0-160">INPUTS</span></span>

### <span data-ttu-id="99fe0-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="99fe0-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="99fe0-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="99fe0-162">System.String[]</span></span>

### <span data-ttu-id="99fe0-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="99fe0-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="99fe0-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="99fe0-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="99fe0-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="99fe0-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="99fe0-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="99fe0-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="99fe0-167">출력</span><span class="sxs-lookup"><span data-stu-id="99fe0-167">OUTPUTS</span></span>

### <span data-ttu-id="99fe0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="99fe0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="99fe0-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99fe0-169">NOTES</span></span>
* <span data-ttu-id="99fe0-170">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="99fe0-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="99fe0-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99fe0-171">RELATED LINKS</span></span>

[<span data-ttu-id="99fe0-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="99fe0-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="99fe0-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="99fe0-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="99fe0-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="99fe0-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="99fe0-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="99fe0-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
