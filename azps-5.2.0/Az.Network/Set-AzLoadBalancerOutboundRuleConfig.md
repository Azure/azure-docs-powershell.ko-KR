---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347630"
---
# <span data-ttu-id="0175f-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0175f-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="0175f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0175f-102">SYNOPSIS</span></span>
<span data-ttu-id="0175f-103">부하 균형 조정에 대한 아웃바운드 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0175f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0175f-104">SYNTAX</span></span>

### <span data-ttu-id="0175f-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="0175f-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0175f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0175f-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0175f-107">설명</span><span class="sxs-lookup"><span data-stu-id="0175f-107">DESCRIPTION</span></span>
<span data-ttu-id="0175f-108">**Set-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure Load Balancer에 대한 아웃바운드 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0175f-109">예제</span><span class="sxs-lookup"><span data-stu-id="0175f-109">EXAMPLES</span></span>

### <span data-ttu-id="0175f-110">예제 1: 부하 균형 조정기에서 아웃바운드 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="0175f-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="0175f-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 힌트한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="0175f-112">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerOutboundRuleConfig에 전달합니다. 이 명령은 아웃바운드 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="0175f-113">세 번째 명령은 부하 분산을 **Set-AzLoadBalancerOutboundRuleConfig에** 전달합니다. 이 명령은 아웃바운드 규칙 구성을 저장하고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="0175f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0175f-114">PARAMETERS</span></span>

### <span data-ttu-id="0175f-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="0175f-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="0175f-116">NAT에 사용할 아웃바운드 포트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="0175f-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0175f-117">-BackendAddressPool</span></span>
<span data-ttu-id="0175f-118">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="0175f-119">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="0175f-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0175f-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="0175f-121">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="0175f-122">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="0175f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0175f-123">-DefaultProfile</span></span>
<span data-ttu-id="0175f-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0175f-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0175f-125">-EnableTcpReset</span></span>
<span data-ttu-id="0175f-126">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="0175f-127">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0175f-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0175f-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0175f-129">부하 균형 조정의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="0175f-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0175f-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0175f-131">TCP 유휴 연결에 대한 시간 제한</span><span class="sxs-lookup"><span data-stu-id="0175f-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="0175f-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0175f-132">-LoadBalancer</span></span>
<span data-ttu-id="0175f-133">부하 균형 조정기 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="0175f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="0175f-134">-Name</span></span>
<span data-ttu-id="0175f-135">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="0175f-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0175f-136">-Protocol</span></span>
<span data-ttu-id="0175f-137">프로토콜 - TCP, UDP 또는 모두</span><span class="sxs-lookup"><span data-stu-id="0175f-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="0175f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0175f-138">-Confirm</span></span>
<span data-ttu-id="0175f-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0175f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0175f-140">-WhatIf</span></span>
<span data-ttu-id="0175f-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0175f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0175f-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0175f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0175f-143">CommonParameters</span></span>
<span data-ttu-id="0175f-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0175f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0175f-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0175f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0175f-146">입력</span><span class="sxs-lookup"><span data-stu-id="0175f-146">INPUTS</span></span>

### <span data-ttu-id="0175f-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0175f-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0175f-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0175f-148">System.Int32</span></span>

### <span data-ttu-id="0175f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0175f-149">System.String</span></span>

### <span data-ttu-id="0175f-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="0175f-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="0175f-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0175f-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0175f-152">출력</span><span class="sxs-lookup"><span data-stu-id="0175f-152">OUTPUTS</span></span>

### <span data-ttu-id="0175f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0175f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0175f-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0175f-154">NOTES</span></span>

## <span data-ttu-id="0175f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0175f-155">RELATED LINKS</span></span>

[<span data-ttu-id="0175f-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0175f-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0175f-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0175f-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0175f-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0175f-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0175f-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0175f-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
