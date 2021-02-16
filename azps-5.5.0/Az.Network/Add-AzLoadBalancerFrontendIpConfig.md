---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193972"
---
# <span data-ttu-id="dad83-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dad83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad83-102">SYNOPSIS</span></span>
<span data-ttu-id="dad83-103">부하 균형 조정에 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="dad83-104">구문</span><span class="sxs-lookup"><span data-stu-id="dad83-104">SYNTAX</span></span>

### <span data-ttu-id="dad83-105">SetByResourceSubnet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dad83-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad83-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="dad83-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad83-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad83-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad83-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad83-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad83-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dad83-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad83-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dad83-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad83-111">설명</span><span class="sxs-lookup"><span data-stu-id="dad83-111">DESCRIPTION</span></span>
<span data-ttu-id="dad83-112">**Add-AzLoadBalancerFrontendIpConfig** cmdlet은 Azure Load Balancer에 프런트 엔드 IP 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="dad83-113">예제</span><span class="sxs-lookup"><span data-stu-id="dad83-113">EXAMPLES</span></span>

### <span data-ttu-id="dad83-114">예제 1 동적 IP 주소를 통해 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="dad83-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="dad83-115">첫 번째 명령은 MyVnet이라는 Azure 가상 네트워크를 사용하고 파이프라인을 사용하여 **결과를 Get-AzVirtualNetworkSubnetConfig** cmdlet에 전달하여 MySubnet이라는 서브넷을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="dad83-116">그런 다음, 명령은 결과를 이름 지정한 변수에 $Subnet.</span><span class="sxs-lookup"><span data-stu-id="dad83-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="dad83-117">두 번째 명령은 MyLB라는 부하 분산 장치에 대한 결과를 **Add-AzLoadBalancerFrontendIpConfig** cmdlet에 전달합니다. 이 cmdlet은 부하 분산 장치에 프런트 엔드 IP 구성을 추가하고, 이 cmdlet은 해당 변수에 저장된 서브넷의 동적 개인 IP 주소를 $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="dad83-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="dad83-118">예제 2 고정 IP 주소를 통해 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="dad83-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="dad83-119">첫 번째 명령은 MyVnet이라는 Azure 가상 네트워크를 사용하고 파이프라인을 사용하여 **결과를 Get-AzVirtualNetworkSubnetConfig** cmdlet에 전달하여 MySubnet이라는 서브넷을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="dad83-120">그런 다음, 명령은 결과를 이름 지정한 변수에 $Subnet.</span><span class="sxs-lookup"><span data-stu-id="dad83-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="dad83-121">두 번째 명령은 MyLB라는 부하 분산 장치에 대한 결과를 **Add-AzLoadBalancerFrontendIpConfig** cmdlet에 전달합니다. 이 cmdlet은 프런트 엔드 IP 구성을 부하 분산 장치에 추가하고, 이 cmdlet은 해당 변수에 저장된 서브넷의 정적 개인 IP 주소를 사용하여 $Subnet.</span><span class="sxs-lookup"><span data-stu-id="dad83-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="dad83-122">예제 3 공용 IP 주소를 통해 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="dad83-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="dad83-123">첫 번째 명령은 MyPub라는 Azure 공용 IP 주소를 사용하여 결과를 $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="dad83-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="dad83-124">두 번째 명령은 MyLB라는 부하 분산 장치에 대한 결과를 **Add-AzLoadBalancerFrontendIpConfig** cmdlet에 전달합니다. 이 cmdlet은 해당 변수에 저장된 공용 IP 주소를 사용하여 프런트 엔드 IP 구성을 부하 분산 장치에 $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="dad83-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="dad83-125">예제 4 공용 IP를 통해 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="dad83-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="dad83-126">첫 번째 명령은 MyPubPrefix라는 Azure 공용 IP prefix를 얻게 하여 결과를 $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="dad83-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="dad83-127">두 번째 명령은 MyLB라는 부하 분산 장치에 대한 결과를 **Add-AzLoadBalancerFrontendIpConfig** cmdlet에 전달합니다. 이 cmdlet은 해당 변수에 저장된 공용 IP 접두사로 프런트 엔드 IP 구성을 부하 분산 장치에 $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="dad83-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="dad83-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad83-128">PARAMETERS</span></span>

### <span data-ttu-id="dad83-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad83-129">-DefaultProfile</span></span>
<span data-ttu-id="dad83-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dad83-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dad83-131">-LoadBalancer</span></span>
<span data-ttu-id="dad83-132">**LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="dad83-133">이 cmdlet은 이 매개 변수가 지정하는 프런트 엔드 IP 구성을 부하 균형 조정에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-134">-Name</span><span class="sxs-lookup"><span data-stu-id="dad83-134">-Name</span></span>
<span data-ttu-id="dad83-135">추가할 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="dad83-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad83-136">-PrivateIpAddress</span></span>
<span data-ttu-id="dad83-137">프런트 엔드 IP 구성과 연결될 개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="dad83-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="dad83-139">IP 구성의 개인 IP 주소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-139">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad83-140">-PublicIpAddress</span></span>
<span data-ttu-id="dad83-141">프런트 엔드 IP 구성과 연결될 공용 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="dad83-142">-PublicIpAddressId</span></span>
<span data-ttu-id="dad83-143">프런트 엔드 IP 구성을 추가할 공용 IP 주소의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dad83-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="dad83-145">프런트 엔드 IP 구성과 연결될 공용 IP 주소 앞에 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="dad83-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="dad83-147">프런트 엔드 IP 구성과 연결될 공용 IP 주소 앞에 있는 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-148">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dad83-148">-Subnet</span></span>
<span data-ttu-id="dad83-149">프런트 엔드 IP 구성을 추가할 서브넷 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dad83-150">-SubnetId</span></span>
<span data-ttu-id="dad83-151">프런트 엔드 IP 구성을 추가할 서브넷의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="dad83-152">-Zone</span></span>
<span data-ttu-id="dad83-153">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="dad83-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dad83-154">-Confirm</span></span>
<span data-ttu-id="dad83-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad83-156">-WhatIf</span></span>
<span data-ttu-id="dad83-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dad83-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dad83-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad83-159">CommonParameters</span></span>
<span data-ttu-id="dad83-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dad83-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad83-161">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dad83-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad83-162">입력</span><span class="sxs-lookup"><span data-stu-id="dad83-162">INPUTS</span></span>

### <span data-ttu-id="dad83-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dad83-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="dad83-164">System.String</span><span class="sxs-lookup"><span data-stu-id="dad83-164">System.String</span></span>

### <span data-ttu-id="dad83-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dad83-165">System.String[]</span></span>

### <span data-ttu-id="dad83-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dad83-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="dad83-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dad83-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="dad83-168">출력</span><span class="sxs-lookup"><span data-stu-id="dad83-168">OUTPUTS</span></span>

### <span data-ttu-id="dad83-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dad83-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dad83-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dad83-170">NOTES</span></span>

## <span data-ttu-id="dad83-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dad83-171">RELATED LINKS</span></span>

[<span data-ttu-id="dad83-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dad83-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dad83-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="dad83-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dad83-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dad83-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dad83-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


