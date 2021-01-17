---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322748"
---
# <span data-ttu-id="cf735-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf735-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="cf735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf735-102">SYNOPSIS</span></span>
<span data-ttu-id="cf735-103">네트워크 인터페이스에 대한 IP 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="cf735-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf735-104">SYNTAX</span></span>

### <span data-ttu-id="cf735-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="cf735-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf735-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf735-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf735-107">설명</span><span class="sxs-lookup"><span data-stu-id="cf735-107">DESCRIPTION</span></span>
<span data-ttu-id="cf735-108">**Set-AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스에 대한 IP 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="cf735-109">예제</span><span class="sxs-lookup"><span data-stu-id="cf735-109">EXAMPLES</span></span>

### <span data-ttu-id="cf735-110">1: IP 구성의 IP 주소 변경</span><span class="sxs-lookup"><span data-stu-id="cf735-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cf735-111">처음 두 명령은 myvnet이라는 가상 네트워크와 mysubnet이라는 서브넷을 사용하여 각각 $vnet 및 $subnet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="cf735-112">세 번째 명령은 업데이트해야 하는 IP 구성과 연결된 네트워크 인터페이스 nic1을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="cf735-113">세 번째 명령은 기본 IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="cf735-114">마지막으로 마지막 명령은 네트워크 인터페이스를 업데이트하여 변경이 성공적으로 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="cf735-115">2: 애플리케이션 보안 그룹과 IP 구성 연결</span><span class="sxs-lookup"><span data-stu-id="cf735-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cf735-116">이 예제에서 변수는 $asg 보안 그룹에 대한 참조를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="cf735-117">네 번째 명령은 업데이트해야 하는 IP 구성과 연결된 네트워크 인터페이스 nic1을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="cf735-118">이 Set-AzNetworkInterfaceIpConfig IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정하고 검색된 애플리케이션 보안 그룹과의 연관을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="cf735-119">마지막으로 마지막 명령은 네트워크 인터페이스를 업데이트하여 변경이 성공적으로 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="cf735-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf735-120">PARAMETERS</span></span>

### <span data-ttu-id="cf735-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cf735-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="cf735-122">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cf735-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="cf735-124">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cf735-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="cf735-126">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cf735-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="cf735-128">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf735-129">-DefaultProfile</span></span>
<span data-ttu-id="cf735-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf735-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cf735-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="cf735-132">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백end 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cf735-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="cf735-134">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백end 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="cf735-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="cf735-136">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 인바운드 NAT(네트워크 주소 변환) 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="cf735-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="cf735-138">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 인바운드 NAT 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="cf735-139">-Name</span><span class="sxs-lookup"><span data-stu-id="cf735-139">-Name</span></span>
<span data-ttu-id="cf735-140">이 cmdlet이 설정하는 네트워크 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="cf735-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cf735-141">-NetworkInterface</span></span>
<span data-ttu-id="cf735-142">**NetworkInterface 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf735-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="cf735-143">이 cmdlet은 이 매개 변수가 지정하는 개체에 네트워크 인터페이스 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf735-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="cf735-144">-Primary</span></span>
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

### <span data-ttu-id="cf735-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cf735-145">-PrivateIpAddress</span></span>
<span data-ttu-id="cf735-146">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="cf735-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cf735-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="cf735-148">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="cf735-149">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="cf735-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf735-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="cf735-150">IPv4</span></span>
- <span data-ttu-id="cf735-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="cf735-151">IPv6</span></span>

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

### <span data-ttu-id="cf735-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cf735-152">-PublicIpAddress</span></span>
<span data-ttu-id="cf735-153">**PublicIPAddress** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="cf735-154">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="cf735-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cf735-155">-PublicIpAddressId</span></span>
<span data-ttu-id="cf735-156">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="cf735-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="cf735-157">-Subnet</span></span>
<span data-ttu-id="cf735-158">서브넷 개체를 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf735-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="cf735-159">이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="cf735-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cf735-160">-SubnetId</span></span>
<span data-ttu-id="cf735-161">이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="cf735-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf735-162">CommonParameters</span></span>
<span data-ttu-id="cf735-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf735-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf735-164">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf735-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf735-165">입력</span><span class="sxs-lookup"><span data-stu-id="cf735-165">INPUTS</span></span>

### <span data-ttu-id="cf735-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cf735-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="cf735-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cf735-167">System.String[]</span></span>

### <span data-ttu-id="cf735-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="cf735-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="cf735-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="cf735-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="cf735-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="cf735-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="cf735-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="cf735-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="cf735-172">출력</span><span class="sxs-lookup"><span data-stu-id="cf735-172">OUTPUTS</span></span>

### <span data-ttu-id="cf735-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cf735-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cf735-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf735-174">NOTES</span></span>
* <span data-ttu-id="cf735-175">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="cf735-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cf735-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf735-176">RELATED LINKS</span></span>

[<span data-ttu-id="cf735-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf735-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cf735-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf735-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cf735-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf735-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cf735-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cf735-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
