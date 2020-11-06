---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 111723b2f0271583d43bd1c845eebe9800190a59
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93538260"
---
# <span data-ttu-id="cba95-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cba95-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="cba95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba95-102">SYNOPSIS</span></span>
<span data-ttu-id="cba95-103">네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cba95-104">SYNTAX</span></span>

### <span data-ttu-id="cba95-105">SetByIpConfigurationResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="cba95-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba95-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="cba95-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba95-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cba95-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba95-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cba95-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cba95-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cba95-109">DESCRIPTION</span></span>
<span data-ttu-id="cba95-110">**새 AzureRmNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="cba95-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cba95-111">EXAMPLES</span></span>

### <span data-ttu-id="cba95-112">예제 1: Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="cba95-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="cba95-113">이 명령은 VirtualNetwork1 이라는 가상 네트워크의 Subnet1에서 동적으로 할당 된 개인 IP 주소를 사용 하 여 NetworkInterface001 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="cba95-114">또한이 명령은 두 개의 DNS 서버를 네트워크 인터페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="cba95-115">IPConfiguration 자식 리소스는 이름 IPConfiguration1를 사용 하 여 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="cba95-116">예제 2: IP 구성 개체를 사용 하 여 Azure 네트워크 인터페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="cba95-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="cba95-117">이 예제에서는 IP 구성 개체를 사용 하 여 새 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="cba95-118">IP 구성 개체는 고정 개인 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="cba95-119">첫 번째 명령은 IPConfig1 이라는 네트워크 인터페이스 IP 구성을 만들고이 구성을 $IPconfig 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="cba95-120">두 번째 명령은 $IPconfig 이라는 변수에 저장 된 네트워크 인터페이스 IP 구성을 사용 하는 NetworkInterface1 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="cba95-121">변수</span><span class="sxs-lookup"><span data-stu-id="cba95-121">PARAMETERS</span></span>

### <span data-ttu-id="cba95-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cba95-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="cba95-123">**ApplicationGatewayBackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cba95-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cba95-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="cba95-125">**ApplicationGatewayBackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cba95-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cba95-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="cba95-127">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cba95-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cba95-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="cba95-129">네트워크 인터페이스 IP 구성이 속해야 하는 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="cba95-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cba95-130">-AsJob</span></span>
<span data-ttu-id="cba95-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cba95-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cba95-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba95-132">-DefaultProfile</span></span>
<span data-ttu-id="cba95-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cba95-134">-DnsServer</span></span>
<span data-ttu-id="cba95-135">네트워크 인터페이스에 대 한 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="cba95-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="cba95-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="cba95-137">가속화 네트워킹을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="cba95-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="cba95-138">-EnableIPForwarding</span></span>
<span data-ttu-id="cba95-139">이 cmdlet이 네트워크 인터페이스에 대해 IP 전달을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="cba95-140">IP 전달을 통해 가상 컴퓨터는 다른 목적지로 주소가 지정 된 트래픽을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="cba95-141">-Force</span><span class="sxs-lookup"><span data-stu-id="cba95-141">-Force</span></span>
<span data-ttu-id="cba95-142">이름이 같은 네트워크 인터페이스가 이미 있는 경우에도 네트워크 인터페이스를 강제로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="cba95-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="cba95-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="cba95-144">새 네트워크 인터페이스에 대 한 내부 DNS 이름 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cba95-145">-IpConfiguration</span></span>
<span data-ttu-id="cba95-146">이 cmdlet이 네트워크 인터페이스에 대해 사용 하는 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="cba95-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cba95-147">-IpConfigurationName</span></span>
<span data-ttu-id="cba95-148">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cba95-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="cba95-150">**BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cba95-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cba95-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="cba95-152">**BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="cba95-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="cba95-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="cba95-154">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cba95-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="cba95-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="cba95-156">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="cba95-157">-위치</span><span class="sxs-lookup"><span data-stu-id="cba95-157">-Location</span></span>
<span data-ttu-id="cba95-158">네트워크 인터페이스의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-159">-이름</span><span class="sxs-lookup"><span data-stu-id="cba95-159">-Name</span></span>
<span data-ttu-id="cba95-160">만들려는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cba95-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cba95-162">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cba95-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="cba95-164">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="cba95-165">-PrivateIpAddress</span></span>
<span data-ttu-id="cba95-166">이 네트워크 인터페이스에 할당할 고정 IPv4 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cba95-167">-PublicIpAddress</span></span>
<span data-ttu-id="cba95-168">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="cba95-169">-PublicIpAddressId</span></span>
<span data-ttu-id="cba95-170">네트워크 인터페이스에 할당할 **PublicIPAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba95-171">-ResourceGroupName</span></span>
<span data-ttu-id="cba95-172">네트워크 인터페이스가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-173">-서브넷</span><span class="sxs-lookup"><span data-stu-id="cba95-173">-Subnet</span></span>
<span data-ttu-id="cba95-174">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="cba95-175">이 cmdlet은이 매개 변수에서 지정 하는 서브넷에 대 한 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cba95-176">-SubnetId</span></span>
<span data-ttu-id="cba95-177">네트워크 인터페이스를 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-178">태그</span><span class="sxs-lookup"><span data-stu-id="cba95-178">-Tag</span></span>
<span data-ttu-id="cba95-179">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cba95-180">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="cba95-180">For example:</span></span>

<span data-ttu-id="cba95-181">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cba95-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba95-182">-확인</span><span class="sxs-lookup"><span data-stu-id="cba95-182">-Confirm</span></span>
<span data-ttu-id="cba95-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba95-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba95-184">-WhatIf</span></span>
<span data-ttu-id="cba95-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cba95-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba95-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba95-187">CommonParameters</span></span>
<span data-ttu-id="cba95-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba95-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba95-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba95-190">입력</span><span class="sxs-lookup"><span data-stu-id="cba95-190">INPUTS</span></span>

### <span data-ttu-id="cba95-191">않아야</span><span class="sxs-lookup"><span data-stu-id="cba95-191">None</span></span>
<span data-ttu-id="cba95-192">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cba95-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cba95-193">출력</span><span class="sxs-lookup"><span data-stu-id="cba95-193">OUTPUTS</span></span>

### <span data-ttu-id="cba95-194">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cba95-194">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cba95-195">상속자</span><span class="sxs-lookup"><span data-stu-id="cba95-195">NOTES</span></span>

## <span data-ttu-id="cba95-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cba95-196">RELATED LINKS</span></span>

[<span data-ttu-id="cba95-197">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cba95-197">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="cba95-198">제거-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cba95-198">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="cba95-199">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cba95-199">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
