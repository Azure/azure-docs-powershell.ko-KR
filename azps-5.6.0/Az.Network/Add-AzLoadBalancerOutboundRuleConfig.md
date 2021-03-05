---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006491"
---
# <span data-ttu-id="3f979-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f979-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="3f979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f979-102">SYNOPSIS</span></span>
<span data-ttu-id="3f979-103">부하 저울에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="3f979-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f979-104">SYNTAX</span></span>

### <span data-ttu-id="3f979-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f979-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f979-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f979-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f979-107">설명</span><span class="sxs-lookup"><span data-stu-id="3f979-107">DESCRIPTION</span></span>
<span data-ttu-id="3f979-108">**Add-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure 부하 분산기에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="3f979-109">예제</span><span class="sxs-lookup"><span data-stu-id="3f979-109">EXAMPLES</span></span>

### <span data-ttu-id="3f979-110">예제 1: 부하 저울에 아웃바운드 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="3f979-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="3f979-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산 변수를 얻은 다음, 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="3f979-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="3f979-112">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb **Add-AzLoadBalancerOutboundRuleConfig에** 전달하여 부하 분산기에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="3f979-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f979-113">PARAMETERS</span></span>

### <span data-ttu-id="3f979-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="3f979-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="3f979-115">NAT에 사용할 아웃바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f979-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f979-116">-BackendAddressPool</span></span>
<span data-ttu-id="3f979-117">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="3f979-118">아웃바운드 트래픽은 백end IPS의 IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f979-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3f979-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="3f979-120">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="3f979-121">아웃바운드 트래픽은 백end IPS의 IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f979-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f979-122">-DefaultProfile</span></span>
<span data-ttu-id="3f979-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f979-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="3f979-124">-EnableTcpReset</span></span>
<span data-ttu-id="3f979-125">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="3f979-126">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="3f979-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f979-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3f979-128">부하 저울의 Frontend IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f979-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3f979-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3f979-130">TCP 유휴 연결의 시간 제한</span><span class="sxs-lookup"><span data-stu-id="3f979-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f979-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f979-131">-LoadBalancer</span></span>
<span data-ttu-id="3f979-132">부하 균형기 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="3f979-133">-Name</span><span class="sxs-lookup"><span data-stu-id="3f979-133">-Name</span></span>
<span data-ttu-id="3f979-134">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="3f979-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3f979-135">-Protocol</span></span>
<span data-ttu-id="3f979-136">프로토콜 - TCP, UDP 또는 모두</span><span class="sxs-lookup"><span data-stu-id="3f979-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="3f979-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3f979-137">-Confirm</span></span>
<span data-ttu-id="3f979-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f979-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f979-139">-WhatIf</span></span>
<span data-ttu-id="3f979-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f979-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f979-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f979-142">CommonParameters</span></span>
<span data-ttu-id="3f979-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f979-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f979-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3f979-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f979-145">입력</span><span class="sxs-lookup"><span data-stu-id="3f979-145">INPUTS</span></span>

### <span data-ttu-id="3f979-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f979-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3f979-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3f979-147">System.Int32</span></span>

### <span data-ttu-id="3f979-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3f979-148">System.String</span></span>

### <span data-ttu-id="3f979-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="3f979-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="3f979-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f979-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3f979-151">출력</span><span class="sxs-lookup"><span data-stu-id="3f979-151">OUTPUTS</span></span>

### <span data-ttu-id="3f979-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f979-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3f979-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f979-153">NOTES</span></span>

## <span data-ttu-id="3f979-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f979-154">RELATED LINKS</span></span>

[<span data-ttu-id="3f979-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f979-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3f979-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f979-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3f979-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f979-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="3f979-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f979-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
