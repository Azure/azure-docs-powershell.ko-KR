---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187260"
---
# <span data-ttu-id="39131-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39131-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="39131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39131-102">SYNOPSIS</span></span>
<span data-ttu-id="39131-103">부하 균형 조정에 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="39131-104">구문</span><span class="sxs-lookup"><span data-stu-id="39131-104">SYNTAX</span></span>

### <span data-ttu-id="39131-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="39131-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39131-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39131-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39131-107">설명</span><span class="sxs-lookup"><span data-stu-id="39131-107">DESCRIPTION</span></span>
<span data-ttu-id="39131-108">**Add-AzLoadBalancerRuleConfig** cmdlet은 Azure Load Balancer에 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="39131-109">예제</span><span class="sxs-lookup"><span data-stu-id="39131-109">EXAMPLES</span></span>

### <span data-ttu-id="39131-110">예제 1: 부하 균형 조정에 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="39131-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="39131-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 힌트한 다음, 해당 부하 분산 $slb.</span><span class="sxs-lookup"><span data-stu-id="39131-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="39131-112">두 번째 명령은 파이프라인 연산자를 사용하여 $slb Load **Balancer를 Add-AzLoadBalancerRuleConfig에** 전달합니다. 이 명령은 NewRule이라는 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="39131-113">세 번째 명령은 새 Load Balancer 규칙 구성을 사용하여 Azure의 부하 균형 조정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="39131-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39131-114">PARAMETERS</span></span>

### <span data-ttu-id="39131-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39131-115">-BackendAddressPool</span></span>
<span data-ttu-id="39131-116">부하 균형 조정기 규칙 구성과 연결될 백안 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="39131-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="39131-118">부하 균형 조정기 규칙 구성과 연결될 **BackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="39131-119">-BackendPort</span></span>
<span data-ttu-id="39131-120">부하 균형 조정기 규칙 구성에 의해 일치되는 트래픽에 대한 백 끝 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39131-121">-DefaultProfile</span></span>
<span data-ttu-id="39131-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39131-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39131-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="39131-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="39131-124">부하 분산 규칙의 프런트 엔드에 지정된 publicIP 주소를 사용하도록 백 엔드 풀의 VM에 대한 SNAT를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="39131-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="39131-125">-EnableFloatingIP</span></span>
<span data-ttu-id="39131-126">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39131-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="39131-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="39131-127">-EnableTcpReset</span></span>
<span data-ttu-id="39131-128">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="39131-129">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="39131-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="39131-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39131-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="39131-131">부하 균형 조정기 규칙 구성과 연결될 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39131-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="39131-133">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="39131-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="39131-134">-FrontendPort</span></span>
<span data-ttu-id="39131-135">부하 균형 조정기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="39131-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="39131-137">부하 균형 조정기에서 대화 상태가 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="39131-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39131-138">-LoadBalancer</span></span>
<span data-ttu-id="39131-139">**LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="39131-140">이 cmdlet은 이 매개 변수가 지정하는 규칙 구성을 부하 균형 조정에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="39131-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="39131-141">-LoadDistribution</span></span>
<span data-ttu-id="39131-142">부하 분산을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="39131-143">-Name</span><span class="sxs-lookup"><span data-stu-id="39131-143">-Name</span></span>
<span data-ttu-id="39131-144">부하 균형 조정기 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="39131-145">-Probe</span></span>
<span data-ttu-id="39131-146">부하 균형 조정기 규칙 구성과 연결하기 위한 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="39131-147">-ProbeId</span></span>
<span data-ttu-id="39131-148">부하 균형 조정기 규칙 구성과 연결될 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39131-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="39131-149">-Protocol</span></span>
<span data-ttu-id="39131-150">부하 균형 조정기 규칙에 의해 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="39131-151">이 매개 변수에 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="39131-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="39131-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39131-152">-Confirm</span></span>
<span data-ttu-id="39131-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39131-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39131-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39131-154">-WhatIf</span></span>
<span data-ttu-id="39131-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="39131-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39131-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39131-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39131-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39131-157">CommonParameters</span></span>
<span data-ttu-id="39131-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39131-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39131-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="39131-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39131-160">입력</span><span class="sxs-lookup"><span data-stu-id="39131-160">INPUTS</span></span>

### <span data-ttu-id="39131-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39131-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="39131-162">System.String</span><span class="sxs-lookup"><span data-stu-id="39131-162">System.String</span></span>

### <span data-ttu-id="39131-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="39131-163">System.Int32</span></span>

### <span data-ttu-id="39131-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="39131-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="39131-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39131-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="39131-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="39131-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="39131-167">출력</span><span class="sxs-lookup"><span data-stu-id="39131-167">OUTPUTS</span></span>

### <span data-ttu-id="39131-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39131-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="39131-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39131-169">NOTES</span></span>

## <span data-ttu-id="39131-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39131-170">RELATED LINKS</span></span>

[<span data-ttu-id="39131-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39131-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="39131-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39131-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39131-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39131-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39131-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39131-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39131-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39131-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


