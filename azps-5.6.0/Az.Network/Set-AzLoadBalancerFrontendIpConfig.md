---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ef9121f0962cc5ba06aa9c040d4647a1365fdf80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963915"
---
# <span data-ttu-id="9bc93-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bc93-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9bc93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc93-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc93-103">부하 저울에 대한 프런트 엔드 IP 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="9bc93-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bc93-104">SYNTAX</span></span>

### <span data-ttu-id="9bc93-105">SetByResourceSubnet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9bc93-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc93-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9bc93-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc93-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bc93-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bc93-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bc93-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bc93-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9bc93-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bc93-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9bc93-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bc93-111">설명</span><span class="sxs-lookup"><span data-stu-id="9bc93-111">DESCRIPTION</span></span>
<span data-ttu-id="9bc93-112">**Set-AzLoadBalancerFrontendIpConfig** cmdlet은 부하 분산기에 대한 프런트 엔드 IP 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="9bc93-113">예제</span><span class="sxs-lookup"><span data-stu-id="9bc93-113">EXAMPLES</span></span>

### <span data-ttu-id="9bc93-114">예제 1: 부하 저울의 프런트 엔드 IP 구성 수정</span><span class="sxs-lookup"><span data-stu-id="9bc93-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="9bc93-115">첫 번째 명령은 서브넷이라는 가상 서브넷을 얻은 다음, 해당 서브넷을 $Subnet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="9bc93-116">두 번째 명령은 MyLoadBalancer라는 연결된 부하 분산 장치 $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9bc93-117">세 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerFrontendIpConfig에 전달합니다. 이 명령은 새 프론트 엔드에 대한 NewFrontend라는 프런트 엔드 IP 구성을 $slb.</span><span class="sxs-lookup"><span data-stu-id="9bc93-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="9bc93-118">네 번째 명령은 부하 분산 $slb **Set-AzLoadBalancerFrontendIpConfig로** 전달합니다. 이 명령은 프런트 엔드 IP 구성을 저장하고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="9bc93-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9bc93-119">PARAMETERS</span></span>

### <span data-ttu-id="9bc93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc93-120">-DefaultProfile</span></span>
<span data-ttu-id="9bc93-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bc93-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bc93-122">-LoadBalancer</span></span>
<span data-ttu-id="9bc93-123">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-123">Specifies a load balancer.</span></span>
<span data-ttu-id="9bc93-124">이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 대한 프런트 엔드 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bc93-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9bc93-125">-Name</span></span>
<span data-ttu-id="9bc93-126">설정할 프런트 엔드 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="9bc93-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bc93-127">-PrivateIpAddress</span></span>
<span data-ttu-id="9bc93-128">설정할 프런트 엔드 IP 구성과 연결된 부하 저울의 개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="9bc93-129">서브넷 매개 변수를 지정하는 경우만 *이 매개 변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="9bc93-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="9bc93-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9bc93-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9bc93-131">IP 구성의 개인 IP 주소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="9bc93-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bc93-132">-PublicIpAddress</span></span>
<span data-ttu-id="9bc93-133">설정할 프런트 엔드 IP 구성과 연결된 **PublicIpAddress** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="9bc93-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9bc93-134">-PublicIpAddressId</span></span>
<span data-ttu-id="9bc93-135">이 cmdlet이 설정하는 프런트 엔드 IP 구성과 연결된 **PublicIpAddress** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="9bc93-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9bc93-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="9bc93-137">프런트 엔드 IP 구성과 연결하기 위해 **PublicIpAddressPrefix** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9bc93-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="9bc93-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="9bc93-139">프런트 엔드 IP 구성과 연결하기 위해 **PublicIpAddressPrefix** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9bc93-140">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9bc93-140">-Subnet</span></span>
<span data-ttu-id="9bc93-141">이 cmdlet에서  설정하는 프런트 엔드 IP 구성을 포함하는 서브넷 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="9bc93-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9bc93-142">-SubnetId</span></span>
<span data-ttu-id="9bc93-143">이 cmdlet이 설정하는 프런트 엔드 IP 구성을 포함하는 서브넷의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="9bc93-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="9bc93-144">-Zone</span></span>
<span data-ttu-id="9bc93-145">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9bc93-146">-확인</span><span class="sxs-lookup"><span data-stu-id="9bc93-146">-Confirm</span></span>
<span data-ttu-id="9bc93-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc93-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc93-148">-WhatIf</span></span>
<span data-ttu-id="9bc93-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bc93-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc93-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc93-151">CommonParameters</span></span>
<span data-ttu-id="9bc93-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc93-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc93-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bc93-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc93-154">입력</span><span class="sxs-lookup"><span data-stu-id="9bc93-154">INPUTS</span></span>

### <span data-ttu-id="9bc93-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bc93-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9bc93-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9bc93-156">System.String</span></span>

### <span data-ttu-id="9bc93-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9bc93-157">System.String[]</span></span>

### <span data-ttu-id="9bc93-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9bc93-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="9bc93-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bc93-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9bc93-160">출력</span><span class="sxs-lookup"><span data-stu-id="9bc93-160">OUTPUTS</span></span>

### <span data-ttu-id="9bc93-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bc93-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9bc93-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bc93-162">NOTES</span></span>

## <span data-ttu-id="9bc93-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bc93-163">RELATED LINKS</span></span>

[<span data-ttu-id="9bc93-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bc93-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9bc93-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9bc93-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9bc93-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bc93-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9bc93-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bc93-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9bc93-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bc93-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9bc93-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bc93-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


