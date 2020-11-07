---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 6bf01750543fa5564e9490ad85d84cc258f10f4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702431"
---
# <span data-ttu-id="81191-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81191-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="81191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81191-102">SYNOPSIS</span></span>
<span data-ttu-id="81191-103">Azure 네트워크 인터페이스 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81191-104">SYNTAX</span></span>

### <span data-ttu-id="81191-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="81191-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81191-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81191-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81191-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81191-107">DESCRIPTION</span></span>
<span data-ttu-id="81191-108">**AzureRmNetworkInterfaceIpConfig** Cmdlet은 Azure 네트워크 인터페이스 IP 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="81191-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81191-109">EXAMPLES</span></span>

### <span data-ttu-id="81191-110">1: IP 구성의 IP 주소 변경</span><span class="sxs-lookup"><span data-stu-id="81191-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="81191-111">처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 myvnet 이라는 서브넷을 가져오고이를 변수 $vnet 및 $subnet 각각에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="81191-112">세 번째 명령은 업데이트 해야 하는 IP 구성과 연결 된 네트워크 인터페이스 nic1를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81191-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="81191-113">세 번째 명령은 기본 IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="81191-114">마지막으로 최종 명령은 변경 내용이 성공적으로 적용 되도록 네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="81191-115">2: IP 구성에 응용 프로그램 보안 groupp 연결</span><span class="sxs-lookup"><span data-stu-id="81191-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="81191-116">이 예제에서 변수 $asg에는 응용 프로그램 보안 그룹에 대 한 참조가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81191-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="81191-117">네 번째 명령은 업데이트 해야 하는 IP 구성과 연결 된 네트워크 인터페이스 nic1를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81191-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="81191-118">Set-AzureRmNetworkInterfaceIpConfig는 기본 IP 구성 ipconfig1의 개인 IP 주소를 10.0.0.11로 설정 하 고 검색 된 응용 프로그램 보안 그룹과 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81191-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="81191-119">마지막으로 최종 명령은 변경 내용이 성공적으로 적용 되도록 네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="81191-120">변수</span><span class="sxs-lookup"><span data-stu-id="81191-120">PARAMETERS</span></span>

### <span data-ttu-id="81191-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81191-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="81191-122">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="81191-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="81191-124">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="81191-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="81191-126">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="81191-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="81191-128">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81191-129">-DefaultProfile</span></span>
<span data-ttu-id="81191-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81191-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81191-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81191-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="81191-132">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="81191-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="81191-134">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="81191-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="81191-136">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="81191-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="81191-138">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 NAT 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="81191-139">-이름</span><span class="sxs-lookup"><span data-stu-id="81191-139">-Name</span></span>
<span data-ttu-id="81191-140">이 cmdlet이 설정 하는 네트워크 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="81191-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="81191-141">-NetworkInterface</span></span>
<span data-ttu-id="81191-142">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="81191-143">이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="81191-144">-기본</span><span class="sxs-lookup"><span data-stu-id="81191-144">-Primary</span></span>
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

### <span data-ttu-id="81191-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="81191-145">-PrivateIpAddress</span></span>
<span data-ttu-id="81191-146">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="81191-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="81191-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="81191-148">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="81191-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81191-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81191-150">(Ipv4</span><span class="sxs-lookup"><span data-stu-id="81191-150">IPv4</span></span>
- <span data-ttu-id="81191-151">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="81191-151">IPv6</span></span>

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

### <span data-ttu-id="81191-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="81191-152">-PublicIpAddress</span></span>
<span data-ttu-id="81191-153">**PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="81191-154">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81191-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="81191-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="81191-155">-PublicIpAddressId</span></span>
<span data-ttu-id="81191-156">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81191-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="81191-157">-서브넷</span><span class="sxs-lookup"><span data-stu-id="81191-157">-Subnet</span></span>
<span data-ttu-id="81191-158">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="81191-159">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81191-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="81191-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="81191-160">-SubnetId</span></span>
<span data-ttu-id="81191-161">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81191-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="81191-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81191-162">CommonParameters</span></span>
<span data-ttu-id="81191-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81191-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81191-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81191-165">입력</span><span class="sxs-lookup"><span data-stu-id="81191-165">INPUTS</span></span>

### <span data-ttu-id="81191-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="81191-166">PSNetworkInterface</span></span>
<span data-ttu-id="81191-167">' NetworkInterface ' 매개 변수는 파이프라인에서 ' PSNetworkInterface ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81191-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="81191-168">출력</span><span class="sxs-lookup"><span data-stu-id="81191-168">OUTPUTS</span></span>

### <span data-ttu-id="81191-169">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="81191-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="81191-170">상속자</span><span class="sxs-lookup"><span data-stu-id="81191-170">NOTES</span></span>
* <span data-ttu-id="81191-171">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="81191-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="81191-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81191-172">RELATED LINKS</span></span>

[<span data-ttu-id="81191-173">추가-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81191-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="81191-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81191-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="81191-175">새로운 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81191-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="81191-176">제거-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81191-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


