---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340809"
---
# <span data-ttu-id="f36f2-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f36f2-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="f36f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f36f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f36f2-103">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-103">Creates a network interface.</span></span>

## <span data-ttu-id="f36f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f36f2-104">SYNTAX</span></span>

### <span data-ttu-id="f36f2-105">SetByIpConfigurationResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="f36f2-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f36f2-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f36f2-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f36f2-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f36f2-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f36f2-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f36f2-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f36f2-109">설명</span><span class="sxs-lookup"><span data-stu-id="f36f2-109">DESCRIPTION</span></span>
<span data-ttu-id="f36f2-110">**New-AzNetworkInterface** cmdlet은 Azure 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="f36f2-111">예제</span><span class="sxs-lookup"><span data-stu-id="f36f2-111">EXAMPLES</span></span>

### <span data-ttu-id="f36f2-112">예제 1: Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="f36f2-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="f36f2-113">이 명령은 VirtualNetwork1이라는 가상 네트워크의 Subnet1에서 동적으로 할당된 개인 IP 주소를 사용하여 NetworkInterface001이라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="f36f2-114">또한 이 명령은 네트워크 인터페이스에 두 개의 DNS 서버를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="f36f2-115">IPConfiguration 자식 리소스는 IPConfiguration1 이름을 사용하여 자동으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="f36f2-116">예제 2: IP 구성 개체를 사용하여 Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="f36f2-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="f36f2-117">이 예제에서는 IP 구성 개체를 사용하여 새 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="f36f2-118">IP 구성 개체는 정적 개인 IPv4 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="f36f2-119">첫 번째 명령은 두 번째 명령에서 서브넷을 할당하는 데 사용되는 기존 지정된 가상 네트워크를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="f36f2-120">두 번째 명령은 IPConfig1이라는 네트워크 인터페이스 IP 구성을 만들고 구성을 $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="f36f2-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="f36f2-121">세 번째 명령은 NetworkInterface1이라는 네트워크 인터페이스를 만듭니다. 이 인터페이스는 네트워크 인터페이스 IP 구성을 사용하여 $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="f36f2-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="f36f2-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="f36f2-122">Example 3</span></span>

<span data-ttu-id="f36f2-123">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-123">Creates a network interface.</span></span> <span data-ttu-id="f36f2-124">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="f36f2-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="f36f2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f36f2-125">PARAMETERS</span></span>

### <span data-ttu-id="f36f2-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f36f2-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f36f2-127">**ApplicationGatewayBackendAddressPool 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f36f2-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f36f2-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f36f2-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f36f2-129">**ApplicationGatewayBackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f36f2-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f36f2-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f36f2-131">네트워크 인터페이스 IP 구성이 속해야 하는 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f36f2-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f36f2-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f36f2-133">네트워크 인터페이스 IP 구성이 속해야 하는 애플리케이션 보안 그룹 참조의 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f36f2-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f36f2-134">-AsJob</span></span>
<span data-ttu-id="f36f2-135">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f36f2-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f36f2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36f2-136">-DefaultProfile</span></span>
<span data-ttu-id="f36f2-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f36f2-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f36f2-138">-DnsServer</span></span>
<span data-ttu-id="f36f2-139">네트워크 인터페이스에 대한 DNS 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-139">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="f36f2-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="f36f2-141">가속 네트워킹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="f36f2-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f36f2-142">-EnableIPForwarding</span></span>
<span data-ttu-id="f36f2-143">이 cmdlet을 통해 네트워크 인터페이스에 IP 전달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="f36f2-144">IP 전달을 사용하면 가상 머신이 다른 대상에 주소가 주소가 있는 트래픽을 수신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="f36f2-145">-Force</span><span class="sxs-lookup"><span data-stu-id="f36f2-145">-Force</span></span>
<span data-ttu-id="f36f2-146">동일한 이름의 네트워크 인터페이스가 이미 있는 경우에도 네트워크 인터페이스를 강제로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="f36f2-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="f36f2-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="f36f2-148">새 네트워크 인터페이스에 대한 내부 DNS 이름 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-148">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36f2-149">-IpConfiguration</span></span>
<span data-ttu-id="f36f2-150">이 cmdlet이 네트워크 인터페이스에 사용하는 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f36f2-151">-IpConfigurationName</span></span>
<span data-ttu-id="f36f2-152">IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-152">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f36f2-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f36f2-154">**BackendAddressPool** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f36f2-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f36f2-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f36f2-156">**BackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f36f2-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f36f2-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f36f2-158">부하 균형 조정에 대한 인바운드 NAT 규칙 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f36f2-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="f36f2-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f36f2-160">부하 균형 조정에 대한 인바운드 NAT 규칙 구성의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f36f2-161">-Location</span><span class="sxs-lookup"><span data-stu-id="f36f2-161">-Location</span></span>
<span data-ttu-id="f36f2-162">네트워크 인터페이스에 대한 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-162">Specifies the region for a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-163">-Name</span><span class="sxs-lookup"><span data-stu-id="f36f2-163">-Name</span></span>
<span data-ttu-id="f36f2-164">만들 네트워크 인터페이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-164">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f36f2-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f36f2-166">**NetworkSecurityGroup 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f36f2-166">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f36f2-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f36f2-168">네트워크 보안 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-168">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f36f2-169">-PrivateIpAddress</span></span>
<span data-ttu-id="f36f2-170">이 네트워크 인터페이스에 할당할 고정 IPv4 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f36f2-171">-PublicIpAddress</span></span>
<span data-ttu-id="f36f2-172">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f36f2-173">-PublicIpAddressId</span></span>
<span data-ttu-id="f36f2-174">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36f2-175">-ResourceGroupName</span></span>
<span data-ttu-id="f36f2-176">네트워크 인터페이스가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-177">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f36f2-177">-Subnet</span></span>
<span data-ttu-id="f36f2-178">서브넷 개체를 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f36f2-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f36f2-179">이 cmdlet은 이 매개 변수가 지정하는 서브넷에 대한 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f36f2-180">-SubnetId</span></span>
<span data-ttu-id="f36f2-181">네트워크 인터페이스를 만들 서브넷의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="f36f2-182">-Tag</span></span>
<span data-ttu-id="f36f2-183">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f36f2-184">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f36f2-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f36f2-185">-Confirm</span></span>
<span data-ttu-id="f36f2-186">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-186">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36f2-187">-WhatIf</span></span>
<span data-ttu-id="f36f2-188">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f36f2-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36f2-189">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-189">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36f2-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36f2-190">CommonParameters</span></span>
<span data-ttu-id="f36f2-191">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f36f2-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36f2-192">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f36f2-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36f2-193">입력</span><span class="sxs-lookup"><span data-stu-id="f36f2-193">INPUTS</span></span>

### <span data-ttu-id="f36f2-194">System.String</span><span class="sxs-lookup"><span data-stu-id="f36f2-194">System.String</span></span>

### <span data-ttu-id="f36f2-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="f36f2-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f36f2-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f36f2-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f36f2-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="f36f2-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f36f2-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="f36f2-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-199">System.String[]</span></span>

### <span data-ttu-id="f36f2-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="f36f2-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="f36f2-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="f36f2-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="f36f2-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="f36f2-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f36f2-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f36f2-205">출력</span><span class="sxs-lookup"><span data-stu-id="f36f2-205">OUTPUTS</span></span>

### <span data-ttu-id="f36f2-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f36f2-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f36f2-207">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f36f2-207">NOTES</span></span>

## <span data-ttu-id="f36f2-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f36f2-208">RELATED LINKS</span></span>

[<span data-ttu-id="f36f2-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f36f2-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f36f2-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f36f2-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="f36f2-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f36f2-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
