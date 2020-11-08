---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042494"
---
# <span data-ttu-id="2d674-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="2d674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d674-102">SYNOPSIS</span></span>
<span data-ttu-id="2d674-103">네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-103">Updates a network interface.</span></span>

## <span data-ttu-id="2d674-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d674-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d674-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d674-105">DESCRIPTION</span></span>
<span data-ttu-id="2d674-106">**AzNetworkInterface** 는 네트워크 인터페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="2d674-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d674-107">EXAMPLES</span></span>

### <span data-ttu-id="2d674-108">예제 1: 네트워크 인터페이스 구성</span><span class="sxs-lookup"><span data-stu-id="2d674-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="2d674-109">이 예제에서는 네트워크 인터페이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-109">This example configures a network interface.</span></span>
<span data-ttu-id="2d674-110">첫 번째 명령은 리소스 그룹 ResourceGroup1에서 NetworkInterface1 라는 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2d674-111">두 번째 명령은 IP 구성의 개인 IP 주소를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="2d674-112">세 번째 명령은 개인 IP 할당 방법을 Static으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="2d674-113">네 번째 명령은 네트워크 인터페이스에 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="2d674-114">다섯 번째 명령은 $Nic 변수에 저장 된 정보를 사용 하 여 네트워크 인터페이스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="2d674-115">예제 2: 네트워크 인터페이스에서 DNS 설정 변경</span><span class="sxs-lookup"><span data-stu-id="2d674-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2d674-116">첫 번째 명령은 리소스 그룹 ResourceGroup1 내에 있는 NetworkInterface1 라는 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="2d674-117">두 번째 명령은이 인터페이스에 DNS 서버 192.168.1.100를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="2d674-118">세 번째 명령은 이러한 변경 내용을 네트워크 인터페이스에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="2d674-119">DNS 서버를 제거 하려면 위에 나열 된 명령을 실행 하 되, 대체 "를 입력 합니다. "With"를 추가 합니다. "제거"를 두 번 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="2d674-120">예제 3: 네트워크 인터페이스에서 IP 전달 사용</span><span class="sxs-lookup"><span data-stu-id="2d674-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2d674-121">첫 번째 명령은 NetworkInterface1 이라는 기존 네트워크 인터페이스를 가져와 $nic 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2d674-122">두 번째 명령은 IP 전달 값을 true로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="2d674-123">마지막으로 세 번째 명령은 네트워크 인터페이스에 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="2d674-124">네트워크 인터페이스에서 IP 전달을 사용 하지 않도록 설정 하려면 예제 예제를 따르고, 두 번째 명령을 "$nic로 변경 하세요. EnableIPForwarding = 0 "입니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="2d674-125">예제 4: 네트워크 인터페이스의 서브넷 변경</span><span class="sxs-lookup"><span data-stu-id="2d674-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2d674-126">첫 번째 명령은 네트워크 인터페이스 NetworkInterface1를 가져와이를 $nic 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2d674-127">두 번째 명령은 네트워크 인터페이스가 연결 될 서브넷과 연결 된 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="2d674-128">두 번째 명령은 서브넷을 가져와 $subnet 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="2d674-129">세 번째 명령은 새 서브넷이 있는 네트워크 인터페이스의 기본 개인 IP 주소와 연결 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="2d674-130">마지막으로 네트워크 인터페이스에 이러한 변경 내용을 적용 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="2d674-131">서브넷을 변경할 수 있으려면 먼저 IP 구성이 동적 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="2d674-132">고정 IP 구성이 있는 경우 계속 하기 전에 동적으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="2d674-133">네트워크 인터페이스에 여러 개의 IP 구성이 있는 경우 이러한 모든 IP 구성에 대해 위 명령에 대해 마지막 Set-AzNetworkInterface 명령을 실행 하기 전에 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="2d674-134">위의 명령 에서처럼 "0"을 적절 한 번호로 바꾸어이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="2d674-135">네트워크 인터페이스에 N 개의 IP 구성이 있는 경우 이러한 명령의 N-1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="2d674-136">예제 5: 네트워크 인터페이스에 네트워크 보안 그룹 연결/분리</span><span class="sxs-lookup"><span data-stu-id="2d674-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2d674-137">첫 번째 명령은 NetworkInterface1 이라는 기존 네트워크 인터페이스를 가져와 $nic 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2d674-138">두 번째 명령은 MyNSG 이라는 기존 네트워크 보안 그룹을 가져와 $nsg 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="2d674-139">세 번째 명령은 $nsg를 $nic에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="2d674-140">마지막으로, 위의 명령은 네트워크 인터페이스에 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="2d674-141">네트워크 인터페이스에서 네트워크 보안 그룹을 분리 하려면, 세 번째 명령에서 $null으로 $nsg을 간단히 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="2d674-142">변수</span><span class="sxs-lookup"><span data-stu-id="2d674-142">PARAMETERS</span></span>

### <span data-ttu-id="2d674-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d674-143">-AsJob</span></span>
<span data-ttu-id="2d674-144">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2d674-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d674-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d674-145">-DefaultProfile</span></span>
<span data-ttu-id="2d674-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d674-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-147">-NetworkInterface</span></span>
<span data-ttu-id="2d674-148">네트워크 인터페이스를 설정 해야 하는 상태를 나타내는 네트워크 인터페이스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="2d674-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d674-149">CommonParameters</span></span>
<span data-ttu-id="2d674-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d674-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d674-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d674-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d674-152">입력</span><span class="sxs-lookup"><span data-stu-id="2d674-152">INPUTS</span></span>

### <span data-ttu-id="2d674-153">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2d674-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2d674-154">출력</span><span class="sxs-lookup"><span data-stu-id="2d674-154">OUTPUTS</span></span>

### <span data-ttu-id="2d674-155">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2d674-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2d674-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2d674-156">NOTES</span></span>

## <span data-ttu-id="2d674-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d674-157">RELATED LINKS</span></span>

[<span data-ttu-id="2d674-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2d674-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2d674-160">새로운 AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="2d674-161">제거-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d674-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
