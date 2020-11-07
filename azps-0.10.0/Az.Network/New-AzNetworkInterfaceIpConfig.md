---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7776bb57215ce3cb9b4291a0a71fdb01e028491e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875422"
---
# <span data-ttu-id="ed7e1-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ed7e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7e1-103">네트워크 인터페이스 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="ed7e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed7e1-104">SYNTAX</span></span>

### <span data-ttu-id="ed7e1-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed7e1-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7e1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ed7e1-107">DESCRIPTION</span></span>
<span data-ttu-id="ed7e1-108">**AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스에 대 한 Azure 네트워크 인터페이스 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="ed7e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ed7e1-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7e1-110">1: 네트워크 인터페이스용 공용 IP 주소를 사용 하 여 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="ed7e1-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="ed7e1-111">처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 이전에 만든 myvnet 이라는 서브넷을 각각 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="ed7e1-112">이러한 두 가지는 $vnet 및 $Subnet에 각각 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="ed7e1-113">세 번째 명령은 PIP1 이라는 이전에 만든 공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="ed7e1-114">위의 명령은 공용 IP 주소가 연결 된 기본 IP 구성으로 "IPConfig-1" 이라는 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="ed7e1-115">마지막 명령은이 IP 구성을 사용 하 여 mynic1 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="ed7e1-116">2: 개인 IP 주소를 사용 하 여 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="ed7e1-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="ed7e1-117">처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 이전에 만든 myvnet 이라는 서브넷을 각각 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="ed7e1-118">이러한 두 가지는 $vnet 및 $Subnet에 각각 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="ed7e1-119">세 번째 명령은 개인 IP 주소와 연결 된 10.0.0.5 "IPConfig-2" 라는 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="ed7e1-120">마지막 명령은이 IP 구성을 사용 하 여 mynic1 라는 네트워크 인터페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="ed7e1-121">변수</span><span class="sxs-lookup"><span data-stu-id="ed7e1-121">PARAMETERS</span></span>

### <span data-ttu-id="ed7e1-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed7e1-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="ed7e1-123">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="ed7e1-125">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed7e1-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="ed7e1-127">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="ed7e1-129">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7e1-130">-DefaultProfile</span></span>
<span data-ttu-id="ed7e1-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed7e1-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed7e1-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="ed7e1-133">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="ed7e1-135">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ed7e1-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="ed7e1-137">이 네트워크 인터페이스 IPConfiguration이 속한 부하 분산 장치 인바운드 Nat 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="ed7e1-139">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="ed7e1-140">-이름</span><span class="sxs-lookup"><span data-stu-id="ed7e1-140">-Name</span></span>
<span data-ttu-id="ed7e1-141">네트워크 인터페이스 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-141">Specifies the name of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-142">-기본</span><span class="sxs-lookup"><span data-stu-id="ed7e1-142">-Primary</span></span>
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

### <span data-ttu-id="ed7e1-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed7e1-143">-PrivateIpAddress</span></span>
<span data-ttu-id="ed7e1-144">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-144">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ed7e1-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ed7e1-146">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="ed7e1-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed7e1-148">(Ipv4</span><span class="sxs-lookup"><span data-stu-id="ed7e1-148">IPv4</span></span>
- <span data-ttu-id="ed7e1-149">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="ed7e1-149">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed7e1-150">-PublicIpAddress</span></span>
<span data-ttu-id="ed7e1-151">**PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="ed7e1-152">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-153">-PublicIpAddressId</span></span>
<span data-ttu-id="ed7e1-154">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-155">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ed7e1-155">-Subnet</span></span>
<span data-ttu-id="ed7e1-156">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="ed7e1-157">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ed7e1-158">-SubnetId</span></span>
<span data-ttu-id="ed7e1-159">이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed7e1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7e1-160">CommonParameters</span></span>
<span data-ttu-id="ed7e1-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7e1-162">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7e1-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7e1-163">입력</span><span class="sxs-lookup"><span data-stu-id="ed7e1-163">INPUTS</span></span>

## <span data-ttu-id="ed7e1-164">출력</span><span class="sxs-lookup"><span data-stu-id="ed7e1-164">OUTPUTS</span></span>

### <span data-ttu-id="ed7e1-165">PSNetworkInterfaceIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-165">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="ed7e1-166">상속자</span><span class="sxs-lookup"><span data-stu-id="ed7e1-166">NOTES</span></span>
* <span data-ttu-id="ed7e1-167">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="ed7e1-167">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ed7e1-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed7e1-168">RELATED LINKS</span></span>

[<span data-ttu-id="ed7e1-169">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-169">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed7e1-170">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-170">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed7e1-171">제거-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-171">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed7e1-172">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-172">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


