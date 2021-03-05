---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 2bc63fb21de63dc35855acad53c7e42a13caf215
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011840"
---
# <span data-ttu-id="9b185-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b185-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="9b185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b185-102">SYNOPSIS</span></span>
<span data-ttu-id="9b185-103">부하 균형 조정기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-103">Creates a load balancer.</span></span>

## <span data-ttu-id="9b185-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b185-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b185-105">설명</span><span class="sxs-lookup"><span data-stu-id="9b185-105">DESCRIPTION</span></span>
<span data-ttu-id="9b185-106">**New-AzLoadBalancer** cmdlet은 Azure 부하 분산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="9b185-107">예제</span><span class="sxs-lookup"><span data-stu-id="9b185-107">EXAMPLES</span></span>

### <span data-ttu-id="9b185-108">예제 1: 부하 균형 조정기 만들기</span><span class="sxs-lookup"><span data-stu-id="9b185-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9b185-109">부하 균형 조정기 배포를 위해서는 먼저 여러 개체를 만들어야 합니다. 처음 7개의 명령은 이러한 개체를 만드는 방법을 보여 주야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="9b185-110">8차 명령은 MyResourceGroup이라는 리소스 그룹에 MyLoadBalancer라는 부하 분산기 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="9b185-111">9번째 명령과 마지막 명령은 성공적으로 만들어지기 위해 새 부하 저울을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="9b185-112">이 예제에서는 부하 저울을 만드는 방법만 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="9b185-113">또한 다른 가상 머신에 Add-AzNetworkInterfaceIpConfig cmdlet을 사용하여 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="9b185-114">예제 2: 전역 부하 균형 조정기 만들기</span><span class="sxs-lookup"><span data-stu-id="9b185-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9b185-115">전역 부하 균형을 배포하려면 먼저 여러 개체를 만들어야 합니다. 처음 5개의 명령은 해당 개체를 만드는 방법을 보여 주야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="9b185-116">여섯 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyLoadBalancer라는 부하 분산기 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="9b185-117">일곱 번째 명령과 마지막 명령은 성공적으로 만들어지기 위해 새 부하 균형 조정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="9b185-118">이 예제에서는 전역 부하 균형을 만드는 방법만 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="9b185-119">또한 백 엔드 주소 풀에 지역 부하 New-AzLoadBalancerBackendAddressConfig 프런트 엔드 ipconfig ID를 할당하기 위해 New-AzLoadBalancerBackendAddressConfig cmdlet을 사용하여 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="9b185-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b185-120">PARAMETERS</span></span>

### <span data-ttu-id="9b185-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b185-121">-AsJob</span></span>
<span data-ttu-id="9b185-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9b185-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b185-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9b185-123">-BackendAddressPool</span></span>
<span data-ttu-id="9b185-124">부하 균형 조정기와 연결하기 위해 백던드 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b185-125">-DefaultProfile</span></span>
<span data-ttu-id="9b185-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b185-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9b185-127">-Force</span></span>
<span data-ttu-id="9b185-128">이 cmdlet이 동일한 이름의 부하 균형 조정기가 이미 있는 경우에도 부하 균형 조정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="9b185-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b185-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9b185-130">부하 균형 조정기와 연결하기 위해 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="9b185-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="9b185-132">-InboundNatRule</span></span>
<span data-ttu-id="9b185-133">부하 저울과 연결하기 위해 NAT(인바운드 네트워크 주소 변환) 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="9b185-134">-LoadBalancingRule</span></span>
<span data-ttu-id="9b185-135">부하 분산기와 연결하기 위해 부하 분산 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-136">-Location</span><span class="sxs-lookup"><span data-stu-id="9b185-136">-Location</span></span>
<span data-ttu-id="9b185-137">부하 균형기를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="9b185-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9b185-138">-Name</span></span>
<span data-ttu-id="9b185-139">이렇게 만드는 부하 균형 조정기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="9b185-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="9b185-140">-OutboundRule</span></span>
<span data-ttu-id="9b185-141">아웃바운드 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-142">-Probe</span><span class="sxs-lookup"><span data-stu-id="9b185-142">-Probe</span></span>
<span data-ttu-id="9b185-143">부하 균형 조정기와 연결하기 위해 프로브 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b185-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b185-144">-ResourceGroupName</span></span>
<span data-ttu-id="9b185-145">부하 균형 조정기를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="9b185-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="9b185-146">-Sku</span></span>
<span data-ttu-id="9b185-147">부하 균형 조정기 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="9b185-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b185-148">-Tag</span></span>
<span data-ttu-id="9b185-149">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b185-150">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9b185-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b185-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="9b185-151">-Tier</span></span>
<span data-ttu-id="9b185-152">부하 균형 조정기 Sku 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="9b185-153">-확인</span><span class="sxs-lookup"><span data-stu-id="9b185-153">-Confirm</span></span>
<span data-ttu-id="9b185-154">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b185-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b185-155">-WhatIf</span></span>
<span data-ttu-id="9b185-156">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b185-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b185-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b185-158">CommonParameters</span></span>
<span data-ttu-id="9b185-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b185-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b185-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b185-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b185-161">입력</span><span class="sxs-lookup"><span data-stu-id="9b185-161">INPUTS</span></span>

### <span data-ttu-id="9b185-162">System.String</span><span class="sxs-lookup"><span data-stu-id="9b185-162">System.String</span></span>

### <span data-ttu-id="9b185-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b185-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9b185-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9b185-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="9b185-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="9b185-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="9b185-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="9b185-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="9b185-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="9b185-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="9b185-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="9b185-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="9b185-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="9b185-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="9b185-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="9b185-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="9b185-171">출력</span><span class="sxs-lookup"><span data-stu-id="9b185-171">OUTPUTS</span></span>

### <span data-ttu-id="9b185-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b185-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9b185-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b185-173">NOTES</span></span>

## <span data-ttu-id="9b185-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b185-174">RELATED LINKS</span></span>

[<span data-ttu-id="9b185-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9b185-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9b185-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b185-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9b185-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b185-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="9b185-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b185-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
