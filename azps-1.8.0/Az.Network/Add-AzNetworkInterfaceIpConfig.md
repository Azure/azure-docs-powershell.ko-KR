---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 587ae151830f4d4860aa90c25b80a799e1ba2946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700699"
---
# <span data-ttu-id="a1611-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a1611-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="a1611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1611-102">SYNOPSIS</span></span>
<span data-ttu-id="a1611-103">네트워크 인터페이스에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="a1611-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1611-104">SYNTAX</span></span>

### <span data-ttu-id="a1611-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1611-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1611-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1611-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1611-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a1611-107">DESCRIPTION</span></span>
<span data-ttu-id="a1611-108">**Add-AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스 IP 구성을 Azure 네트워크 인터페이스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="a1611-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a1611-109">EXAMPLES</span></span>

### <span data-ttu-id="a1611-110">예제 1: 응용 프로그램 보안 그룹을 사용 하 여 새 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="a1611-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="a1611-111">이 예제에서는 새 가상 네트워크 MyVNET의 서브넷에 속하는 새 네트워크 인터페이스 MyNetworkInterface를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="a1611-112">또한 네트워크 인터페이스의 IP 구성에 연결 하는 빈 응용 프로그램 보안 그룹인 MyASG를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="a1611-113">두 개체를 모두 만든 후에는 MyASG 개체에 기본 IP 구성을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="a1611-114">마지막으로, 응용 프로그램 보안 그룹 개체에 연결 된 네트워크 인터페이스에 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="a1611-115">변수</span><span class="sxs-lookup"><span data-stu-id="a1611-115">PARAMETERS</span></span>

### <span data-ttu-id="a1611-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a1611-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a1611-117">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a1611-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a1611-119">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1611-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a1611-121">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1611-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a1611-123">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1611-124">-DefaultProfile</span></span>
<span data-ttu-id="a1611-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1611-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a1611-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a1611-127">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a1611-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a1611-129">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a1611-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a1611-131">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a1611-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a1611-133">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 NAT 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="a1611-134">-이름</span><span class="sxs-lookup"><span data-stu-id="a1611-134">-Name</span></span>
<span data-ttu-id="a1611-135">네트워크 인터페이스 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="a1611-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a1611-136">-NetworkInterface</span></span>
<span data-ttu-id="a1611-137">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="a1611-138">이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1611-139">-기본</span><span class="sxs-lookup"><span data-stu-id="a1611-139">-Primary</span></span>
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

### <span data-ttu-id="a1611-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1611-140">-PrivateIpAddress</span></span>
<span data-ttu-id="a1611-141">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="a1611-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a1611-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="a1611-143">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="a1611-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1611-145">(Ipv4</span><span class="sxs-lookup"><span data-stu-id="a1611-145">IPv4</span></span>
- <span data-ttu-id="a1611-146">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="a1611-146">IPv6</span></span>

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

### <span data-ttu-id="a1611-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1611-147">-PublicIpAddress</span></span>
<span data-ttu-id="a1611-148">**PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="a1611-149">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="a1611-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a1611-150">-PublicIpAddressId</span></span>
<span data-ttu-id="a1611-151">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="a1611-152">-서브넷</span><span class="sxs-lookup"><span data-stu-id="a1611-152">-Subnet</span></span>
<span data-ttu-id="a1611-153">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a1611-154">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="a1611-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a1611-155">-SubnetId</span></span>
<span data-ttu-id="a1611-156">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="a1611-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1611-157">CommonParameters</span></span>
<span data-ttu-id="a1611-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1611-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1611-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1611-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1611-160">입력</span><span class="sxs-lookup"><span data-stu-id="a1611-160">INPUTS</span></span>

### <span data-ttu-id="a1611-161">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a1611-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="a1611-162">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="a1611-162">System.String[]</span></span>

### <span data-ttu-id="a1611-163">PSBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a1611-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="a1611-164">PSInboundNatRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a1611-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="a1611-165">PSApplicationGatewayBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a1611-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="a1611-166">Microsoft Azure. \* PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="a1611-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="a1611-167">출력</span><span class="sxs-lookup"><span data-stu-id="a1611-167">OUTPUTS</span></span>

### <span data-ttu-id="a1611-168">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a1611-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a1611-169">상속자</span><span class="sxs-lookup"><span data-stu-id="a1611-169">NOTES</span></span>
* <span data-ttu-id="a1611-170">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="a1611-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a1611-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1611-171">RELATED LINKS</span></span>

[<span data-ttu-id="a1611-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a1611-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a1611-173">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a1611-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a1611-174">제거-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a1611-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a1611-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a1611-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
