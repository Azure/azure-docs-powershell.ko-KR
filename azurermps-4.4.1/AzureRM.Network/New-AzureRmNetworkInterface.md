---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 75e16da63a5348b47a5b67042a2fb1e2078206c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703683"
---
# <span data-ttu-id="87412-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87412-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="87412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87412-102">SYNOPSIS</span></span>
<span data-ttu-id="87412-103">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87412-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87412-104">SYNTAX</span></span>

### <span data-ttu-id="87412-105">SetByIpConfigurationResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="87412-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87412-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="87412-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87412-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="87412-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87412-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="87412-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87412-109">설명은</span><span class="sxs-lookup"><span data-stu-id="87412-109">DESCRIPTION</span></span>
<span data-ttu-id="87412-110">**새 AzureRmNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="87412-111">예제의</span><span class="sxs-lookup"><span data-stu-id="87412-111">EXAMPLES</span></span>

### <span data-ttu-id="87412-112">예제 1: Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="87412-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="87412-113">이 명령은 VirtualNetwork1 이라는 가상 네트워크의 Subnet1에서 동적으로 할당 된 개인 IP 주소를 사용 하 여 NetworkInterface001 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="87412-114">또한이 명령은 두 개의 DNS 서버를 네트워크 인터페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="87412-115">IPConfiguration 자식 리소스는 이름 IPConfiguration1를 사용 하 여 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87412-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="87412-116">예제 2: IP 구성 개체를 사용 하 여 Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="87412-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="87412-117">이 예제에서는 IP 구성 개체를 사용 하 여 새 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="87412-118">IP 구성 개체는 고정 개인 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="87412-119">첫 번째 명령은 IPConfig1 이라는 네트워크 인터페이스 IP 구성을 만들고이 구성을 $IPconfig 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="87412-120">두 번째 명령은 $IPconfig 이라는 변수에 저장 된 네트워크 인터페이스 IP 구성을 사용 하는 NetworkInterface1 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="87412-121">변수</span><span class="sxs-lookup"><span data-stu-id="87412-121">PARAMETERS</span></span>

### <span data-ttu-id="87412-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="87412-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="87412-123">**ApplicationGatewayBackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="87412-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="87412-125">**ApplicationGatewayBackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="87412-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="87412-127">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="87412-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="87412-129">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87412-130">-DefaultProfile</span></span>
<span data-ttu-id="87412-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87412-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87412-132">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="87412-132">-DnsServer</span></span>
<span data-ttu-id="87412-133">네트워크 인터페이스에 대 한 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-133">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-134">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="87412-134">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="87412-135">가속화 네트워킹을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-135">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="87412-136">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="87412-136">-EnableIPForwarding</span></span>
<span data-ttu-id="87412-137">이 cmdlet이 네트워크 인터페이스에 대해 IP 전달을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87412-137">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="87412-138">IP 전달을 통해 가상 컴퓨터는 다른 목적지로 주소가 지정 된 트래픽을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87412-138">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="87412-139">-Force</span><span class="sxs-lookup"><span data-stu-id="87412-139">-Force</span></span>
<span data-ttu-id="87412-140">이름이 같은 네트워크 인터페이스가 이미 있는 경우에도 네트워크 인터페이스를 강제로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-140">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="87412-141">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="87412-141">-InternalDnsNameLabel</span></span>
<span data-ttu-id="87412-142">새 네트워크 인터페이스에 대 한 내부 DNS 이름 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-142">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="87412-143">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="87412-143">-IpConfiguration</span></span>
<span data-ttu-id="87412-144">이 cmdlet이 네트워크 인터페이스에 대해 사용 하는 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-144">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-145">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="87412-145">-IpConfigurationName</span></span>
<span data-ttu-id="87412-146">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-146">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="87412-147">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="87412-147">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="87412-148">**BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-148">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-149">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="87412-149">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="87412-150">**BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-150">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-151">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="87412-151">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="87412-152">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-152">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-153">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="87412-153">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="87412-154">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-154">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87412-155">-위치</span><span class="sxs-lookup"><span data-stu-id="87412-155">-Location</span></span>
<span data-ttu-id="87412-156">네트워크 인터페이스의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-156">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="87412-157">-이름</span><span class="sxs-lookup"><span data-stu-id="87412-157">-Name</span></span>
<span data-ttu-id="87412-158">만들려는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-158">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="87412-159">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="87412-159">-NetworkSecurityGroup</span></span>
<span data-ttu-id="87412-160">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-160">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="87412-161">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="87412-161">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="87412-162">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-162">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="87412-163">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="87412-163">-PrivateIpAddress</span></span>
<span data-ttu-id="87412-164">이 네트워크 인터페이스에 할당할 고정 IPv4 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-164">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="87412-165">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="87412-165">-PublicIpAddress</span></span>
<span data-ttu-id="87412-166">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-166">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="87412-167">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="87412-167">-PublicIpAddressId</span></span>
<span data-ttu-id="87412-168">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-168">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="87412-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87412-169">-ResourceGroupName</span></span>
<span data-ttu-id="87412-170">네트워크 인터페이스가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-170">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="87412-171">-서브넷</span><span class="sxs-lookup"><span data-stu-id="87412-171">-Subnet</span></span>
<span data-ttu-id="87412-172">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-172">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="87412-173">이 cmdlet은이 매개 변수에서 지정 하는 서브넷에 대 한 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87412-173">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="87412-174">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="87412-174">-SubnetId</span></span>
<span data-ttu-id="87412-175">네트워크 인터페이스를 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-175">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="87412-176">태그</span><span class="sxs-lookup"><span data-stu-id="87412-176">-Tag</span></span>
<span data-ttu-id="87412-177">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="87412-177">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87412-178">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="87412-178">For example:</span></span>

<span data-ttu-id="87412-179">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="87412-179">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="87412-180">-확인</span><span class="sxs-lookup"><span data-stu-id="87412-180">-Confirm</span></span>
<span data-ttu-id="87412-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87412-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87412-182">-WhatIf</span></span>
<span data-ttu-id="87412-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87412-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87412-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87412-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87412-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87412-185">CommonParameters</span></span>
<span data-ttu-id="87412-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87412-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87412-187">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87412-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87412-188">입력</span><span class="sxs-lookup"><span data-stu-id="87412-188">INPUTS</span></span>

## <span data-ttu-id="87412-189">출력</span><span class="sxs-lookup"><span data-stu-id="87412-189">OUTPUTS</span></span>

### <span data-ttu-id="87412-190">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="87412-190">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="87412-191">상속자</span><span class="sxs-lookup"><span data-stu-id="87412-191">NOTES</span></span>

## <span data-ttu-id="87412-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87412-192">RELATED LINKS</span></span>

[<span data-ttu-id="87412-193">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87412-193">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="87412-194">제거-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87412-194">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="87412-195">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87412-195">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
