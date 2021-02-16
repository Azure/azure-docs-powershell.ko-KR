---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193948"
---
# <span data-ttu-id="675a6-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="675a6-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="675a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="675a6-102">SYNOPSIS</span></span>
<span data-ttu-id="675a6-103">부하 균형 조정에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="675a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="675a6-104">SYNTAX</span></span>

### <span data-ttu-id="675a6-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="675a6-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="675a6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="675a6-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="675a6-107">설명</span><span class="sxs-lookup"><span data-stu-id="675a6-107">DESCRIPTION</span></span>
<span data-ttu-id="675a6-108">**Add-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure Load Balancer에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="675a6-109">예제</span><span class="sxs-lookup"><span data-stu-id="675a6-109">EXAMPLES</span></span>

### <span data-ttu-id="675a6-110">예제 1: 부하 균형 조정에 아웃바운드 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="675a6-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="675a6-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="675a6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="675a6-112">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb **Add-AzLoadBalancerOutboundRuleConfig에** 전달합니다. 이 명령은 부하 분산에 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="675a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="675a6-113">PARAMETERS</span></span>

### <span data-ttu-id="675a6-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="675a6-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="675a6-115">NAT에 사용할 아웃바운드 포트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="675a6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="675a6-116">-BackendAddressPool</span></span>
<span data-ttu-id="675a6-117">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="675a6-118">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="675a6-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="675a6-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="675a6-120">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="675a6-121">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="675a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675a6-122">-DefaultProfile</span></span>
<span data-ttu-id="675a6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="675a6-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="675a6-124">-EnableTcpReset</span></span>
<span data-ttu-id="675a6-125">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="675a6-126">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="675a6-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="675a6-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="675a6-128">부하 균형 조정의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="675a6-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="675a6-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="675a6-130">TCP 유휴 연결에 대한 시간 제한</span><span class="sxs-lookup"><span data-stu-id="675a6-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="675a6-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="675a6-131">-LoadBalancer</span></span>
<span data-ttu-id="675a6-132">부하 균형 조정기 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="675a6-133">-Name</span><span class="sxs-lookup"><span data-stu-id="675a6-133">-Name</span></span>
<span data-ttu-id="675a6-134">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="675a6-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="675a6-135">-Protocol</span></span>
<span data-ttu-id="675a6-136">프로토콜 - TCP, UDP 또는 모두</span><span class="sxs-lookup"><span data-stu-id="675a6-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="675a6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="675a6-137">-Confirm</span></span>
<span data-ttu-id="675a6-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="675a6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="675a6-139">-WhatIf</span></span>
<span data-ttu-id="675a6-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="675a6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="675a6-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="675a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675a6-142">CommonParameters</span></span>
<span data-ttu-id="675a6-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="675a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675a6-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="675a6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675a6-145">입력</span><span class="sxs-lookup"><span data-stu-id="675a6-145">INPUTS</span></span>

### <span data-ttu-id="675a6-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="675a6-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="675a6-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="675a6-147">System.Int32</span></span>

### <span data-ttu-id="675a6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="675a6-148">System.String</span></span>

### <span data-ttu-id="675a6-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="675a6-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="675a6-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="675a6-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="675a6-151">출력</span><span class="sxs-lookup"><span data-stu-id="675a6-151">OUTPUTS</span></span>

### <span data-ttu-id="675a6-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="675a6-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="675a6-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="675a6-153">NOTES</span></span>

## <span data-ttu-id="675a6-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="675a6-154">RELATED LINKS</span></span>

[<span data-ttu-id="675a6-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="675a6-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="675a6-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="675a6-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="675a6-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="675a6-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="675a6-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="675a6-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
