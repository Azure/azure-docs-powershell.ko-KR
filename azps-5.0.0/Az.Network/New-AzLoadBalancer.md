---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 0b51e2b01fd194b0cb400e2d8547f7d7df78f0a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218257"
---
# <span data-ttu-id="0f5a4-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f5a4-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="0f5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5a4-103">부하 분산 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-103">Creates a load balancer.</span></span>

## <span data-ttu-id="0f5a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f5a4-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f5a4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5a4-106">**AzLoadBalancer** Cmdlet은 Azure 부하 분산 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="0f5a4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f5a4-107">EXAMPLES</span></span>

### <span data-ttu-id="0f5a4-108">예제 1: 부하 분산 만들기</span><span class="sxs-lookup"><span data-stu-id="0f5a4-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0f5a4-109">부하 분산 장치를 배포 하려면 먼저 여러 개체를 만들어야 하 고 처음 일곱 개의 명령은 해당 개체를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="0f5a4-110">여덟 번째 명령은 Myloadbalancer 이라는 리소스 그룹에서 MyLoadBalancer 라는 부하 분산 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="0f5a4-111">아홉 번째 및 마지막 명령은 새 부하 분산을 가져와 성공적으로 생성 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="0f5a4-112">이 예제에서는 부하 분산 장치를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="0f5a4-113">또한 Nic를 다른 가상 컴퓨터에 할당 하려면 Add-AzNetworkInterfaceIpConfig cmdlet을 사용 하 여 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="0f5a4-114">변수</span><span class="sxs-lookup"><span data-stu-id="0f5a4-114">PARAMETERS</span></span>

### <span data-ttu-id="0f5a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f5a4-115">-AsJob</span></span>
<span data-ttu-id="0f5a4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0f5a4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f5a4-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f5a4-117">-BackendAddressPool</span></span>
<span data-ttu-id="0f5a4-118">부하 분산 장치와 연결할 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5a4-119">-DefaultProfile</span></span>
<span data-ttu-id="0f5a4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f5a4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0f5a4-121">-Force</span></span>
<span data-ttu-id="0f5a4-122">동일한 이름을 가진 부하 분산이 이미 있는 경우에도이 cmdlet이 부하 분산 장치를 만드는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="0f5a4-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f5a4-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0f5a4-124">부하 분산 장치와 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="0f5a4-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="0f5a4-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="0f5a4-126">-InboundNatRule</span></span>
<span data-ttu-id="0f5a4-127">부하 분산 장치에 연결 하는 데 사용 되는 인바운드 NAT (network address translation) 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="0f5a4-128">-LoadBalancingRule</span></span>
<span data-ttu-id="0f5a4-129">부하 분산 장치에 연결 하는 부하 분산 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-130">-위치</span><span class="sxs-lookup"><span data-stu-id="0f5a4-130">-Location</span></span>
<span data-ttu-id="0f5a4-131">부하 분산을 만들 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-132">-이름</span><span class="sxs-lookup"><span data-stu-id="0f5a4-132">-Name</span></span>
<span data-ttu-id="0f5a4-133">이를 통해 생성 되는 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="0f5a4-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="0f5a4-134">-OutboundRule</span></span>
<span data-ttu-id="0f5a4-135">아웃 바운드 규칙</span><span class="sxs-lookup"><span data-stu-id="0f5a4-135">The outbound rules.</span></span>

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

### <span data-ttu-id="0f5a4-136">-프로브</span><span class="sxs-lookup"><span data-stu-id="0f5a4-136">-Probe</span></span>
<span data-ttu-id="0f5a4-137">부하 분산 장치와 연결할 프로브 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-137">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f5a4-138">-ResourceGroupName</span></span>
<span data-ttu-id="0f5a4-139">부하 분산을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="0f5a4-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="0f5a4-140">-Sku</span></span>
<span data-ttu-id="0f5a4-141">부하 분산 장치 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="0f5a4-142">태그</span><span class="sxs-lookup"><span data-stu-id="0f5a4-142">-Tag</span></span>
<span data-ttu-id="0f5a4-143">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f5a4-144">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0f5a4-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0f5a4-145">-확인</span><span class="sxs-lookup"><span data-stu-id="0f5a4-145">-Confirm</span></span>
<span data-ttu-id="0f5a4-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f5a4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f5a4-147">-WhatIf</span></span>
<span data-ttu-id="0f5a4-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f5a4-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f5a4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5a4-150">CommonParameters</span></span>
<span data-ttu-id="0f5a4-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5a4-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5a4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5a4-153">입력</span><span class="sxs-lookup"><span data-stu-id="0f5a4-153">INPUTS</span></span>

### <span data-ttu-id="0f5a4-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0f5a4-154">System.String</span></span>

### <span data-ttu-id="0f5a4-155">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0f5a4-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f5a4-156">PSFrontendIPConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-156">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="0f5a4-157">PSBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-157">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="0f5a4-158">PSLoadBalancingRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="0f5a4-159">Microsoft. 네트워크. m a m a. 모델. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="0f5a4-159">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="0f5a4-160">PSInboundNatRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-160">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="0f5a4-161">PSInboundNatPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-161">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="0f5a4-162">PSOutboundRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="0f5a4-162">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="0f5a4-163">출력</span><span class="sxs-lookup"><span data-stu-id="0f5a4-163">OUTPUTS</span></span>

### <span data-ttu-id="0f5a4-164">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f5a4-164">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f5a4-165">상속자</span><span class="sxs-lookup"><span data-stu-id="0f5a4-165">NOTES</span></span>

## <span data-ttu-id="0f5a4-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f5a4-166">RELATED LINKS</span></span>

[<span data-ttu-id="0f5a4-167">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f5a4-167">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f5a4-168">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f5a4-168">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0f5a4-169">제거-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f5a4-169">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="0f5a4-170">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f5a4-170">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
