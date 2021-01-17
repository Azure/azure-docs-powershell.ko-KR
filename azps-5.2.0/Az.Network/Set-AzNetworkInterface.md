---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345837"
---
# <span data-ttu-id="2e275-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="2e275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e275-102">SYNOPSIS</span></span>
<span data-ttu-id="2e275-103">네트워크 인터페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-103">Updates a network interface.</span></span>

## <span data-ttu-id="2e275-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e275-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e275-105">설명</span><span class="sxs-lookup"><span data-stu-id="2e275-105">DESCRIPTION</span></span>
<span data-ttu-id="2e275-106">**Set-AzNetworkInterface는** 네트워크 인터페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="2e275-107">예제</span><span class="sxs-lookup"><span data-stu-id="2e275-107">EXAMPLES</span></span>

### <span data-ttu-id="2e275-108">예제 1: 네트워크 인터페이스 구성</span><span class="sxs-lookup"><span data-stu-id="2e275-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="2e275-109">이 예제에서는 네트워크 인터페이스를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-109">This example configures a network interface.</span></span>
<span data-ttu-id="2e275-110">첫 번째 명령은 리소스 그룹 ResourceGroup1에서 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2e275-111">두 번째 명령은 IP 구성의 개인 IP 주소를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="2e275-112">세 번째 명령은 개인 IP 할당 방법을 고정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="2e275-113">네 번째 명령은 네트워크 인터페이스에 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="2e275-114">다섯 번째 명령은 네트워크 인터페이스를 설정하기 위해 $Nic 변수에 저장된 정보를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="2e275-115">예제 2: 네트워크 인터페이스에서 DNS 설정 변경</span><span class="sxs-lookup"><span data-stu-id="2e275-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2e275-116">첫 번째 명령은 리소스 그룹 ResourceGroup1 내에 있는 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="2e275-117">두 번째 명령은 이 인터페이스에 DNS 서버 192.168.1.100을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="2e275-118">세 번째 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="2e275-119">DNS 서버를 제거하려면 위에 나열된 명령을 따르지만 "을(를) 대체합니다. "을(를) 통해 "를 추가합니다. 두 번째 명령에서 "제거"를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="2e275-120">예제 3: 네트워크 인터페이스에서 IP 전달 사용</span><span class="sxs-lookup"><span data-stu-id="2e275-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2e275-121">첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 $nic 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2e275-122">두 번째 명령은 IP 전달 값을 true로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="2e275-123">마지막으로 세 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="2e275-124">네트워크 인터페이스에서 IP 전달을 사용하지 않도록 설정하는 경우 샘플 예제를 따르지만 두 번째 명령을 "연결"으로 $nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="2e275-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="2e275-125">예제 4: 네트워크 인터페이스의 서브넷 변경</span><span class="sxs-lookup"><span data-stu-id="2e275-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2e275-126">첫 번째 명령은 NetworkInterface1 네트워크 인터페이스를 사용하여 네트워크 인터페이스를 $nic 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2e275-127">두 번째 명령은 네트워크 인터페이스가 연결될 서브넷과 연결된 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="2e275-128">두 번째 명령은 서브넷을 사용하여 $subnet 2 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="2e275-129">세 번째 명령은 네트워크 인터페이스의 기본 개인 IP 주소를 새 서브넷과 연결했습니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="2e275-130">마지막으로 마지막 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용했습니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="2e275-131">서브넷을 변경하려면 먼저 IP 구성이 동적이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="2e275-132">고정 IP 구성이 있는 경우 계속하기 전에 동적 IP 구성으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="2e275-133">네트워크 인터페이스에 여러 IP 구성이 있는 경우 마지막 명령이 실행되기 전에 이러한 모든 IP 구성에 대해 Set-AzNetworkInterface 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="2e275-134">이는 첫 번째 명령에서처럼 수행되지만 "0"을 적절한 숫자로 바꾸면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="2e275-135">네트워크 인터페이스에 N IP 구성이 있는 경우 이러한 명령 중 N-1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="2e275-136">예제 5: 네트워크 인터페이스에 네트워크 보안 그룹 연결/연결 해리</span><span class="sxs-lookup"><span data-stu-id="2e275-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2e275-137">첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 $nic 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="2e275-138">두 번째 명령은 MyNSG라는 기존 네트워크 보안 그룹을 $nsg 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="2e275-139">세 번째 명령은 $nsg 할당하는 $nic.</span><span class="sxs-lookup"><span data-stu-id="2e275-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="2e275-140">마지막으로, 첫 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="2e275-141">네트워크 인터페이스에서 네트워크 보안 그룹을 해리하기 위해 세 번째 $nsg 네트워크 인터페이스로 $null.</span><span class="sxs-lookup"><span data-stu-id="2e275-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="2e275-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e275-142">PARAMETERS</span></span>

### <span data-ttu-id="2e275-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e275-143">-AsJob</span></span>
<span data-ttu-id="2e275-144">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2e275-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e275-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e275-145">-DefaultProfile</span></span>
<span data-ttu-id="2e275-146">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e275-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-147">-NetworkInterface</span></span>
<span data-ttu-id="2e275-148">네트워크 인터페이스를 설정해야 하는 상태를 나타내는 네트워크 인터페이스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="2e275-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e275-149">CommonParameters</span></span>
<span data-ttu-id="2e275-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e275-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e275-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e275-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e275-152">입력</span><span class="sxs-lookup"><span data-stu-id="2e275-152">INPUTS</span></span>

### <span data-ttu-id="2e275-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2e275-154">출력</span><span class="sxs-lookup"><span data-stu-id="2e275-154">OUTPUTS</span></span>

### <span data-ttu-id="2e275-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2e275-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e275-156">NOTES</span></span>

## <span data-ttu-id="2e275-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e275-157">RELATED LINKS</span></span>

[<span data-ttu-id="2e275-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2e275-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2e275-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="2e275-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2e275-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
