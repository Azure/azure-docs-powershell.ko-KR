---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216888"
---
# <span data-ttu-id="2a927-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a927-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="2a927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a927-102">SYNOPSIS</span></span>
<span data-ttu-id="2a927-103">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-103">Creates a network interface.</span></span>

## <span data-ttu-id="2a927-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a927-104">SYNTAX</span></span>

### <span data-ttu-id="2a927-105">SetByIpConfigurationResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a927-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a927-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="2a927-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a927-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a927-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a927-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a927-108">SetByResource</span></span>
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

## <span data-ttu-id="2a927-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2a927-109">DESCRIPTION</span></span>
<span data-ttu-id="2a927-110">**새 AzNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="2a927-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2a927-111">EXAMPLES</span></span>

### <span data-ttu-id="2a927-112">예제 1: Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="2a927-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="2a927-113">이 명령은 VirtualNetwork1 이라는 가상 네트워크의 Subnet1에서 동적으로 할당 된 개인 IP 주소를 사용 하 여 NetworkInterface001 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="2a927-114">또한이 명령은 두 개의 DNS 서버를 네트워크 인터페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="2a927-115">IPConfiguration 자식 리소스는 이름 IPConfiguration1를 사용 하 여 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="2a927-116">예제 2: IP 구성 개체를 사용 하 여 Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="2a927-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="2a927-117">이 예제에서는 IP 구성 개체를 사용 하 여 새 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="2a927-118">IP 구성 개체는 고정 개인 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="2a927-119">첫 번째 명령은 두 번째 명령에서 서브넷을 할당 하는 데 사용 되는 기존 지정 된 가상 네트워크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="2a927-120">두 번째 명령은 IPConfig1 이라는 네트워크 인터페이스 IP 구성을 만들고이 구성을 $IPconfig 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="2a927-121">세 번째 명령은 $IPconfig 이라는 변수에 저장 된 네트워크 인터페이스 IP 구성을 사용 하는 NetworkInterface1 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="2a927-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="2a927-122">Example 3</span></span>

<span data-ttu-id="2a927-123">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-123">Creates a network interface.</span></span> <span data-ttu-id="2a927-124">생성</span><span class="sxs-lookup"><span data-stu-id="2a927-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="2a927-125">변수</span><span class="sxs-lookup"><span data-stu-id="2a927-125">PARAMETERS</span></span>

### <span data-ttu-id="2a927-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a927-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="2a927-127">**ApplicationGatewayBackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a927-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a927-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="2a927-129">**ApplicationGatewayBackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a927-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a927-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="2a927-131">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2a927-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2a927-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="2a927-133">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2a927-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a927-134">-AsJob</span></span>
<span data-ttu-id="2a927-135">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2a927-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a927-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a927-136">-DefaultProfile</span></span>
<span data-ttu-id="2a927-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a927-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="2a927-138">-DnsServer</span></span>
<span data-ttu-id="2a927-139">네트워크 인터페이스에 대 한 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="2a927-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="2a927-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="2a927-141">가속화 네트워킹을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="2a927-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="2a927-142">-EnableIPForwarding</span></span>
<span data-ttu-id="2a927-143">이 cmdlet이 네트워크 인터페이스에 대해 IP 전달을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="2a927-144">IP 전달을 통해 가상 컴퓨터는 다른 목적지로 주소가 지정 된 트래픽을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="2a927-145">-Force</span><span class="sxs-lookup"><span data-stu-id="2a927-145">-Force</span></span>
<span data-ttu-id="2a927-146">이름이 같은 네트워크 인터페이스가 이미 있는 경우에도 네트워크 인터페이스를 강제로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="2a927-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="2a927-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="2a927-148">새 네트워크 인터페이스에 대 한 내부 DNS 이름 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="2a927-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a927-149">-IpConfiguration</span></span>
<span data-ttu-id="2a927-150">이 cmdlet이 네트워크 인터페이스에 대해 사용 하는 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="2a927-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2a927-151">-IpConfigurationName</span></span>
<span data-ttu-id="2a927-152">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="2a927-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a927-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="2a927-154">**BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a927-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a927-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="2a927-156">**BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a927-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2a927-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="2a927-158">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2a927-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="2a927-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="2a927-160">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2a927-161">-위치</span><span class="sxs-lookup"><span data-stu-id="2a927-161">-Location</span></span>
<span data-ttu-id="2a927-162">네트워크 인터페이스의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="2a927-163">-이름</span><span class="sxs-lookup"><span data-stu-id="2a927-163">-Name</span></span>
<span data-ttu-id="2a927-164">만들려는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="2a927-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a927-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2a927-166">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="2a927-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2a927-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2a927-168">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2a927-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a927-169">-PrivateIpAddress</span></span>
<span data-ttu-id="2a927-170">이 네트워크 인터페이스에 할당할 고정 IPv4 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="2a927-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a927-171">-PublicIpAddress</span></span>
<span data-ttu-id="2a927-172">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="2a927-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2a927-173">-PublicIpAddressId</span></span>
<span data-ttu-id="2a927-174">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="2a927-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a927-175">-ResourceGroupName</span></span>
<span data-ttu-id="2a927-176">네트워크 인터페이스가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="2a927-177">-서브넷</span><span class="sxs-lookup"><span data-stu-id="2a927-177">-Subnet</span></span>
<span data-ttu-id="2a927-178">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="2a927-179">이 cmdlet은이 매개 변수에서 지정 하는 서브넷에 대 한 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a927-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2a927-180">-SubnetId</span></span>
<span data-ttu-id="2a927-181">네트워크 인터페이스를 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="2a927-182">태그</span><span class="sxs-lookup"><span data-stu-id="2a927-182">-Tag</span></span>
<span data-ttu-id="2a927-183">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a927-184">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2a927-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a927-185">-확인</span><span class="sxs-lookup"><span data-stu-id="2a927-185">-Confirm</span></span>
<span data-ttu-id="2a927-186">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a927-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a927-187">-WhatIf</span></span>
<span data-ttu-id="2a927-188">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a927-189">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a927-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a927-190">CommonParameters</span></span>
<span data-ttu-id="2a927-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a927-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a927-192">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a927-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a927-193">입력</span><span class="sxs-lookup"><span data-stu-id="2a927-193">INPUTS</span></span>

### <span data-ttu-id="2a927-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a927-194">System.String</span></span>

### <span data-ttu-id="2a927-195">PSNetworkInterfaceIPConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="2a927-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="2a927-196">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2a927-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="2a927-197">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2a927-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="2a927-198">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a927-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2a927-199">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2a927-199">System.String[]</span></span>

### <span data-ttu-id="2a927-200">PSBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="2a927-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="2a927-201">PSInboundNatRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="2a927-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="2a927-202">PSApplicationGatewayBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="2a927-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="2a927-203">Microsoft Azure. \* PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="2a927-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="2a927-204">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2a927-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a927-205">출력</span><span class="sxs-lookup"><span data-stu-id="2a927-205">OUTPUTS</span></span>

### <span data-ttu-id="2a927-206">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2a927-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2a927-207">상속자</span><span class="sxs-lookup"><span data-stu-id="2a927-207">NOTES</span></span>

## <span data-ttu-id="2a927-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a927-208">RELATED LINKS</span></span>

[<span data-ttu-id="2a927-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a927-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2a927-210">제거-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a927-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="2a927-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a927-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
