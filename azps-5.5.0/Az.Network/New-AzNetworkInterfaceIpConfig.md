---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202796"
---
# <span data-ttu-id="3a09a-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a09a-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3a09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a09a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a09a-103">네트워크 인터페이스 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="3a09a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a09a-104">SYNTAX</span></span>

### <span data-ttu-id="3a09a-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a09a-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a09a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a09a-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a09a-107">설명</span><span class="sxs-lookup"><span data-stu-id="3a09a-107">DESCRIPTION</span></span>
<span data-ttu-id="3a09a-108">**New-AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스에 대한 Azure 네트워크 인터페이스 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="3a09a-109">예제</span><span class="sxs-lookup"><span data-stu-id="3a09a-109">EXAMPLES</span></span>

### <span data-ttu-id="3a09a-110">1: 네트워크 인터페이스에 대한 공용 IP 주소를 사용하여 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="3a09a-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="3a09a-111">처음 두 명령은 이전에 만든 myvnet이라는 가상 네트워크와 mysubnet이라는 서브넷을 각각 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="3a09a-112">이러한 데이터는 각각 $vnet $Subnet 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="3a09a-113">세 번째 명령은 PIP1이라는 이전에 만든 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="3a09a-114">첫 번째 명령은 공용 IP 주소가 연결된 기본 IP 구성으로 "IPConfig-1"이라는 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="3a09a-115">그런 다음 마지막 명령은 이 IP 구성을 사용하여 mynic1이라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="3a09a-116">2: 개인 IP 주소를 사용하여 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="3a09a-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="3a09a-117">처음 두 명령은 이전에 만든 myvnet이라는 가상 네트워크와 mysubnet이라는 서브넷을 각각 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="3a09a-118">이러한 데이터는 각각 $vnet $Subnet 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="3a09a-119">세 번째 명령은 개인 IP 주소 10.0.0.5가 연결된 "IPConfig-2"라는 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="3a09a-120">그런 다음 마지막 명령은 이 IP 구성을 사용하여 mynic1이라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="3a09a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a09a-121">PARAMETERS</span></span>

### <span data-ttu-id="3a09a-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3a09a-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="3a09a-123">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3a09a-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="3a09a-125">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a09a-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="3a09a-127">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3a09a-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="3a09a-129">이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a09a-130">-DefaultProfile</span></span>
<span data-ttu-id="3a09a-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a09a-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3a09a-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="3a09a-133">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3a09a-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="3a09a-135">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백드 주소 풀 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="3a09a-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="3a09a-137">이 네트워크 인터페이스 IPConfiguration이 속한 부하 균형 조정기 인바운드 Nat 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="3a09a-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="3a09a-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="3a09a-139">이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 인바운드 NAT(네트워크 주소 변환) 규칙 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3a09a-140">-Name</span><span class="sxs-lookup"><span data-stu-id="3a09a-140">-Name</span></span>
<span data-ttu-id="3a09a-141">네트워크 인터페이스 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="3a09a-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="3a09a-142">-Primary</span></span>
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

### <span data-ttu-id="3a09a-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a09a-143">-PrivateIpAddress</span></span>
<span data-ttu-id="3a09a-144">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="3a09a-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3a09a-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="3a09a-146">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="3a09a-147">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3a09a-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a09a-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="3a09a-148">IPv4</span></span>
- <span data-ttu-id="3a09a-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="3a09a-149">IPv6</span></span>

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

### <span data-ttu-id="3a09a-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a09a-150">-PublicIpAddress</span></span>
<span data-ttu-id="3a09a-151">**PublicIPAddress 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3a09a-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="3a09a-152">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="3a09a-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3a09a-153">-PublicIpAddressId</span></span>
<span data-ttu-id="3a09a-154">이 cmdlet은 이 네트워크 인터페이스 IP 구성과 연결하기 위해 공용 IP 주소에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="3a09a-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3a09a-155">-Subnet</span></span>
<span data-ttu-id="3a09a-156">서브넷 개체를 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3a09a-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="3a09a-157">이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="3a09a-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3a09a-158">-SubnetId</span></span>
<span data-ttu-id="3a09a-159">이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="3a09a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a09a-160">CommonParameters</span></span>
<span data-ttu-id="3a09a-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a09a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a09a-162">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3a09a-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a09a-163">입력</span><span class="sxs-lookup"><span data-stu-id="3a09a-163">INPUTS</span></span>

### <span data-ttu-id="3a09a-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3a09a-164">System.String[]</span></span>

### <span data-ttu-id="3a09a-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="3a09a-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="3a09a-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="3a09a-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="3a09a-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="3a09a-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="3a09a-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="3a09a-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="3a09a-169">출력</span><span class="sxs-lookup"><span data-stu-id="3a09a-169">OUTPUTS</span></span>

### <span data-ttu-id="3a09a-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a09a-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="3a09a-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a09a-171">NOTES</span></span>
* <span data-ttu-id="3a09a-172">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="3a09a-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3a09a-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a09a-173">RELATED LINKS</span></span>

[<span data-ttu-id="3a09a-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a09a-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3a09a-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a09a-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3a09a-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a09a-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3a09a-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a09a-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
