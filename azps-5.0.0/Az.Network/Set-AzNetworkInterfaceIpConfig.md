---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217588"
---
# <span data-ttu-id="9e620-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e620-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="9e620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e620-102">SYNOPSIS</span></span>
<span data-ttu-id="9e620-103">네트워크 인터페이스에 대 한 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="9e620-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e620-104">SYNTAX</span></span>

### <span data-ttu-id="9e620-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e620-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e620-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e620-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e620-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e620-107">DESCRIPTION</span></span>
<span data-ttu-id="9e620-108">**AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스에 대 한 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="9e620-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9e620-109">EXAMPLES</span></span>

### <span data-ttu-id="9e620-110">1: IP 구성의 IP 주소 변경</span><span class="sxs-lookup"><span data-stu-id="9e620-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="9e620-111">처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 myvnet 이라는 서브넷을 가져오고이를 변수 $vnet 및 $subnet 각각에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="9e620-112">세 번째 명령은 업데이트 해야 하는 IP 구성과 연결 된 네트워크 인터페이스 nic1를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="9e620-113">세 번째 명령은 기본 IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="9e620-114">마지막으로 최종 명령은 변경 내용이 성공적으로 적용 되도록 네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="9e620-115">2: IP 구성을 응용 프로그램 보안 그룹과 연결</span><span class="sxs-lookup"><span data-stu-id="9e620-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="9e620-116">이 예제에서 변수 $asg에는 응용 프로그램 보안 그룹에 대 한 참조가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="9e620-117">네 번째 명령은 업데이트 해야 하는 IP 구성과 연결 된 네트워크 인터페이스 nic1를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="9e620-118">Set-AzNetworkInterfaceIpConfig는 기본 IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정 하 고 검색 된 응용 프로그램 보안 그룹과 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="9e620-119">마지막으로 최종 명령은 변경 내용이 성공적으로 적용 되도록 네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="9e620-120">변수</span><span class="sxs-lookup"><span data-stu-id="9e620-120">PARAMETERS</span></span>

### <span data-ttu-id="9e620-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e620-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="9e620-122">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9e620-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="9e620-124">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e620-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="9e620-126">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9e620-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="9e620-128">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e620-129">-DefaultProfile</span></span>
<span data-ttu-id="9e620-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e620-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e620-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="9e620-132">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9e620-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="9e620-134">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="9e620-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="9e620-136">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="9e620-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="9e620-138">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 NAT 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="9e620-139">-이름</span><span class="sxs-lookup"><span data-stu-id="9e620-139">-Name</span></span>
<span data-ttu-id="9e620-140">이 cmdlet이 설정 하는 네트워크 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="9e620-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e620-141">-NetworkInterface</span></span>
<span data-ttu-id="9e620-142">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="9e620-143">이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e620-144">-기본</span><span class="sxs-lookup"><span data-stu-id="9e620-144">-Primary</span></span>
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

### <span data-ttu-id="9e620-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e620-145">-PrivateIpAddress</span></span>
<span data-ttu-id="9e620-146">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="9e620-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9e620-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9e620-148">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="9e620-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e620-150">(Ipv4</span><span class="sxs-lookup"><span data-stu-id="9e620-150">IPv4</span></span>
- <span data-ttu-id="9e620-151">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="9e620-151">IPv6</span></span>

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

### <span data-ttu-id="9e620-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e620-152">-PublicIpAddress</span></span>
<span data-ttu-id="9e620-153">**PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="9e620-154">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="9e620-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9e620-155">-PublicIpAddressId</span></span>
<span data-ttu-id="9e620-156">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="9e620-157">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9e620-157">-Subnet</span></span>
<span data-ttu-id="9e620-158">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="9e620-159">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="9e620-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9e620-160">-SubnetId</span></span>
<span data-ttu-id="9e620-161">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="9e620-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e620-162">CommonParameters</span></span>
<span data-ttu-id="9e620-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e620-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e620-164">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e620-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e620-165">입력</span><span class="sxs-lookup"><span data-stu-id="9e620-165">INPUTS</span></span>

### <span data-ttu-id="9e620-166">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9e620-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="9e620-167">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="9e620-167">System.String[]</span></span>

### <span data-ttu-id="9e620-168">PSBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="9e620-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="9e620-169">PSInboundNatRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="9e620-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="9e620-170">PSApplicationGatewayBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="9e620-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="9e620-171">Microsoft Azure. \* PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="9e620-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="9e620-172">출력</span><span class="sxs-lookup"><span data-stu-id="9e620-172">OUTPUTS</span></span>

### <span data-ttu-id="9e620-173">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9e620-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9e620-174">상속자</span><span class="sxs-lookup"><span data-stu-id="9e620-174">NOTES</span></span>
* <span data-ttu-id="9e620-175">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="9e620-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9e620-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e620-176">RELATED LINKS</span></span>

[<span data-ttu-id="9e620-177">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e620-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9e620-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e620-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9e620-179">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e620-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9e620-180">제거-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9e620-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
