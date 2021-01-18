---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495133"
---
# <span data-ttu-id="d03b6-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d03b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d03b6-102">SYNOPSIS</span></span>
<span data-ttu-id="d03b6-103">부하 균형 조정에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d03b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="d03b6-104">SYNTAX</span></span>

### <span data-ttu-id="d03b6-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="d03b6-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03b6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d03b6-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d03b6-107">설명</span><span class="sxs-lookup"><span data-stu-id="d03b6-107">DESCRIPTION</span></span>
<span data-ttu-id="d03b6-108">**Set-AzLoadBalancerRuleConfig** cmdlet은 부하 분산에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d03b6-109">예제</span><span class="sxs-lookup"><span data-stu-id="d03b6-109">EXAMPLES</span></span>

### <span data-ttu-id="d03b6-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="d03b6-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="d03b6-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 힌트한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="d03b6-112">두 번째 명령은 파이프라인 연산자를 사용하여 $slb Load Balancer를 Add-AzLoadBalancerRuleConfig에 전달합니다. 이 명령은 NewRule이라는 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="d03b6-113">세 번째 명령은 새 규칙 구성을 설정하는 **Set-AzLoadBalancerRuleConfig에** 부하 분산을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="d03b6-114">구성은 이전 명령에서 사용하도록 설정한 부동 IP 주소를 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="d03b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d03b6-115">PARAMETERS</span></span>

### <span data-ttu-id="d03b6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d03b6-116">-BackendAddressPool</span></span>
<span data-ttu-id="d03b6-117">부하 균형 조정기 규칙과 연결하기 위해 **BackendAddressPool** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d03b6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="d03b6-119">부하 균형 조정기 규칙 구성과 연결될 **BackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d03b6-120">-BackendPort</span></span>
<span data-ttu-id="d03b6-121">이 규칙 구성과 일치하는 트래픽에 대한 백투인 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="d03b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03b6-122">-DefaultProfile</span></span>
<span data-ttu-id="d03b6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d03b6-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="d03b6-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="d03b6-125">부하 분산 규칙의 프런트 엔드에 지정된 publicIP 주소를 사용하도록 백 엔드 풀의 VM에 대한 SNAT를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="d03b6-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d03b6-126">-EnableFloatingIP</span></span>
<span data-ttu-id="d03b6-127">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d03b6-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d03b6-128">-EnableTcpReset</span></span>
<span data-ttu-id="d03b6-129">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d03b6-130">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d03b6-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d03b6-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d03b6-132">부하 균형 조정기 규칙 구성과 연결될 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d03b6-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d03b6-134">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d03b6-135">-FrontendPort</span></span>
<span data-ttu-id="d03b6-136">부하 균형 조정기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="d03b6-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d03b6-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d03b6-138">부하 균형 조정기에서 대화 상태가 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d03b6-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d03b6-139">-LoadBalancer</span></span>
<span data-ttu-id="d03b6-140">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-140">Specifies a load balancer.</span></span>
<span data-ttu-id="d03b6-141">이 cmdlet은 이 매개 변수가 지정하는 부하 균형 조정에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d03b6-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="d03b6-142">-LoadDistribution</span></span>
<span data-ttu-id="d03b6-143">부하 분산을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-143">Specifies a load distribution.</span></span>
<span data-ttu-id="d03b6-144">이 매개 변수에 허용되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="d03b6-145">-Name</span><span class="sxs-lookup"><span data-stu-id="d03b6-145">-Name</span></span>
<span data-ttu-id="d03b6-146">부하 균형 조정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="d03b6-147">-Probe</span><span class="sxs-lookup"><span data-stu-id="d03b6-147">-Probe</span></span>
<span data-ttu-id="d03b6-148">부하 균형 조정기 규칙 구성과 연결하기 위한 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="d03b6-149">-ProbeId</span></span>
<span data-ttu-id="d03b6-150">부하 균형 조정기 규칙 구성과 연결될 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03b6-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d03b6-151">-Protocol</span></span>
<span data-ttu-id="d03b6-152">부하 균형 조정기 규칙에 의해 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="d03b6-153">이 매개 변수에 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d03b6-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d03b6-154">-Confirm</span></span>
<span data-ttu-id="d03b6-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d03b6-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d03b6-156">-WhatIf</span></span>
<span data-ttu-id="d03b6-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d03b6-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d03b6-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d03b6-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03b6-159">CommonParameters</span></span>
<span data-ttu-id="d03b6-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d03b6-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03b6-161">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d03b6-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03b6-162">입력</span><span class="sxs-lookup"><span data-stu-id="d03b6-162">INPUTS</span></span>

### <span data-ttu-id="d03b6-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d03b6-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d03b6-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d03b6-164">System.String</span></span>

### <span data-ttu-id="d03b6-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d03b6-165">System.Int32</span></span>

### <span data-ttu-id="d03b6-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d03b6-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="d03b6-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d03b6-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="d03b6-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="d03b6-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="d03b6-169">출력</span><span class="sxs-lookup"><span data-stu-id="d03b6-169">OUTPUTS</span></span>

### <span data-ttu-id="d03b6-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d03b6-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d03b6-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d03b6-171">NOTES</span></span>

## <span data-ttu-id="d03b6-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d03b6-172">RELATED LINKS</span></span>

[<span data-ttu-id="d03b6-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d03b6-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d03b6-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d03b6-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d03b6-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d03b6-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


