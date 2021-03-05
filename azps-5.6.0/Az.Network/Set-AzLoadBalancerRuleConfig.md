---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 28f71cfe18b344c1e0fbccb632e87a19cf6e8075
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003408"
---
# <span data-ttu-id="1b485-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="1b485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b485-102">SYNOPSIS</span></span>
<span data-ttu-id="1b485-103">부하 저울에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1b485-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b485-104">SYNTAX</span></span>

### <span data-ttu-id="1b485-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="1b485-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b485-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b485-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b485-107">설명</span><span class="sxs-lookup"><span data-stu-id="1b485-107">DESCRIPTION</span></span>
<span data-ttu-id="1b485-108">**Set-AzLoadBalancerRuleConfig** cmdlet은 부하 분산기에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1b485-109">예제</span><span class="sxs-lookup"><span data-stu-id="1b485-109">EXAMPLES</span></span>

### <span data-ttu-id="1b485-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="1b485-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="1b485-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산 $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1b485-112">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerRuleConfig에 전달합니다. 이 명령은 NewRule이라는 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="1b485-113">세 번째 명령은 부하 분산을 **Set-AzLoadBalancerRuleConfig로 전달하여** 새 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="1b485-114">구성은 이전 명령에서 사용하도록 설정한 부동 IP 주소를 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="1b485-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b485-115">PARAMETERS</span></span>

### <span data-ttu-id="1b485-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b485-116">-BackendAddressPool</span></span>
<span data-ttu-id="1b485-117">Load Balancer 규칙과 연결하기 위해 **BackendAddressPool** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="1b485-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1b485-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="1b485-119">Load Balancer 규칙 구성과 연결하기 위해 **BackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b485-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="1b485-120">-BackendPort</span></span>
<span data-ttu-id="1b485-121">이 규칙 구성과 일치하는 트래픽에 대한 백end 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="1b485-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b485-122">-DefaultProfile</span></span>
<span data-ttu-id="1b485-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b485-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="1b485-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="1b485-125">부하 분산 규칙의 프런트 엔드에 지정된 공용IP 주소를 사용하도록 백 엔드 풀에서 VM에 대한 SNAT를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="1b485-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="1b485-126">-EnableFloatingIP</span></span>
<span data-ttu-id="1b485-127">이 cmdlet은 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1b485-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1b485-128">-EnableTcpReset</span></span>
<span data-ttu-id="1b485-129">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="1b485-130">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1b485-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b485-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1b485-132">부하 조정기 규칙 구성과 연결하기 위한 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b485-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1b485-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1b485-134">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="1b485-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1b485-135">-FrontendPort</span></span>
<span data-ttu-id="1b485-136">부하 균형기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b485-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1b485-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1b485-138">시간의 길이(분)를 지정합니다. 이 기간은 부하 균형 조정기에서 대화 상태가 유지되는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="1b485-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b485-139">-LoadBalancer</span></span>
<span data-ttu-id="1b485-140">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-140">Specifies a load balancer.</span></span>
<span data-ttu-id="1b485-141">이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 대한 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b485-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="1b485-142">-LoadDistribution</span></span>
<span data-ttu-id="1b485-143">부하 분산을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-143">Specifies a load distribution.</span></span>
<span data-ttu-id="1b485-144">이 매개 변수에 대해 허용되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="1b485-145">-Name</span><span class="sxs-lookup"><span data-stu-id="1b485-145">-Name</span></span>
<span data-ttu-id="1b485-146">부하 균형 조정기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="1b485-147">-Probe</span><span class="sxs-lookup"><span data-stu-id="1b485-147">-Probe</span></span>
<span data-ttu-id="1b485-148">부하 균형기 규칙 구성과 연결하기 위한 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b485-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="1b485-149">-ProbeId</span></span>
<span data-ttu-id="1b485-150">부하 균형기 규칙 구성과 연결하기 위해 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1b485-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1b485-151">-Protocol</span></span>
<span data-ttu-id="1b485-152">부하 균형기 규칙과 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="1b485-153">이 매개 변수에 대해 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="1b485-154">-확인</span><span class="sxs-lookup"><span data-stu-id="1b485-154">-Confirm</span></span>
<span data-ttu-id="1b485-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b485-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b485-156">-WhatIf</span></span>
<span data-ttu-id="1b485-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b485-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b485-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b485-159">CommonParameters</span></span>
<span data-ttu-id="1b485-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b485-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b485-161">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b485-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b485-162">입력</span><span class="sxs-lookup"><span data-stu-id="1b485-162">INPUTS</span></span>

### <span data-ttu-id="1b485-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b485-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1b485-164">System.String</span><span class="sxs-lookup"><span data-stu-id="1b485-164">System.String</span></span>

### <span data-ttu-id="1b485-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1b485-165">System.Int32</span></span>

### <span data-ttu-id="1b485-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b485-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="1b485-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b485-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="1b485-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="1b485-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="1b485-169">출력</span><span class="sxs-lookup"><span data-stu-id="1b485-169">OUTPUTS</span></span>

### <span data-ttu-id="1b485-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b485-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b485-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b485-171">NOTES</span></span>

## <span data-ttu-id="1b485-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b485-172">RELATED LINKS</span></span>

[<span data-ttu-id="1b485-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b485-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b485-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b485-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="1b485-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b485-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


