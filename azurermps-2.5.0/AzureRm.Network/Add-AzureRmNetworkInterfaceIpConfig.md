---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: 8f0678f3b8c14e6d0c98c5cf29857fc3b2cad794
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881069"
---
# <span data-ttu-id="d1d86-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1d86-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d1d86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d86-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d86-103">네트워크 인터페이스에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1d86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1d86-104">SYNTAX</span></span>

### <span data-ttu-id="d1d86-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1d86-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1d86-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d86-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1d86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1d86-107">DESCRIPTION</span></span>
<span data-ttu-id="d1d86-108">**Add-AzureRmNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스 IP 구성을 Azure 네트워크 인터페이스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="d1d86-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d1d86-109">EXAMPLES</span></span>

### <span data-ttu-id="d1d86-110">예제 1: 응용 프로그램 보안 그룹을 사용 하 여 새 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="d1d86-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="d1d86-111">이 예제에서는 새 가상 네트워크 MyVNET의 서브넷에 속하는 새 네트워크 인터페이스 MyNetworkInterface를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="d1d86-112">또한 네트워크 인터페이스의 IP 구성에 연결 하는 빈 응용 프로그램 보안 그룹인 MyASG를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="d1d86-113">두 개체를 모두 만든 후에는 MyASG 개체에 기본 IP 구성을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="d1d86-114">마지막으로, 응용 프로그램 보안 그룹 개체에 연결 된 네트워크 인터페이스에 새 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="d1d86-115">변수</span><span class="sxs-lookup"><span data-stu-id="d1d86-115">PARAMETERS</span></span>

### <span data-ttu-id="d1d86-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1d86-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d1d86-117">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d1d86-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d1d86-119">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d1d86-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d1d86-121">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d1d86-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d1d86-123">이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d86-124">-DefaultProfile</span></span>
<span data-ttu-id="d1d86-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1d86-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1d86-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d1d86-127">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d1d86-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d1d86-129">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d1d86-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d1d86-131">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="d1d86-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d1d86-133">이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 NAT 규칙 참조의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d1d86-134">-이름</span><span class="sxs-lookup"><span data-stu-id="d1d86-134">-Name</span></span>
<span data-ttu-id="d1d86-135">네트워크 인터페이스 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d1d86-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1d86-136">-NetworkInterface</span></span>
<span data-ttu-id="d1d86-137">**NetworkInterface** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d1d86-138">이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 인터페이스 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d86-139">-기본</span><span class="sxs-lookup"><span data-stu-id="d1d86-139">-Primary</span></span>
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

### <span data-ttu-id="d1d86-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d1d86-140">-PrivateIpAddress</span></span>
<span data-ttu-id="d1d86-141">네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d1d86-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d1d86-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d1d86-143">네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="d1d86-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1d86-145">(Ipv4</span><span class="sxs-lookup"><span data-stu-id="d1d86-145">IPv4</span></span>
- <span data-ttu-id="d1d86-146">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="d1d86-146">IPv6</span></span>

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

### <span data-ttu-id="d1d86-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d1d86-147">-PublicIpAddress</span></span>
<span data-ttu-id="d1d86-148">**PublicIPAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="d1d86-149">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d1d86-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d1d86-150">-PublicIpAddressId</span></span>
<span data-ttu-id="d1d86-151">이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d1d86-152">-서브넷</span><span class="sxs-lookup"><span data-stu-id="d1d86-152">-Subnet</span></span>
<span data-ttu-id="d1d86-153">**서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d1d86-154">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d1d86-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d1d86-155">-SubnetId</span></span>
<span data-ttu-id="d1d86-156">이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d1d86-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d86-157">CommonParameters</span></span>
<span data-ttu-id="d1d86-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d86-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d86-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d86-160">입력</span><span class="sxs-lookup"><span data-stu-id="d1d86-160">INPUTS</span></span>

### <span data-ttu-id="d1d86-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1d86-161">PSNetworkInterface</span></span>
<span data-ttu-id="d1d86-162">' NetworkInterface ' 매개 변수는 파이프라인에서 ' PSNetworkInterface ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d86-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d1d86-163">출력</span><span class="sxs-lookup"><span data-stu-id="d1d86-163">OUTPUTS</span></span>

### <span data-ttu-id="d1d86-164">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d1d86-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d1d86-165">상속자</span><span class="sxs-lookup"><span data-stu-id="d1d86-165">NOTES</span></span>
* <span data-ttu-id="d1d86-166">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="d1d86-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d1d86-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1d86-167">RELATED LINKS</span></span>

[<span data-ttu-id="d1d86-168">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1d86-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d1d86-169">새로운 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1d86-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d1d86-170">제거-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1d86-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d1d86-171">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1d86-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

