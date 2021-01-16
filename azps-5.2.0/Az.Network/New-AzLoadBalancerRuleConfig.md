---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364372"
---
# <span data-ttu-id="05cf6-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05cf6-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="05cf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="05cf6-103">부하 균형 조정에 대한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="05cf6-104">구문</span><span class="sxs-lookup"><span data-stu-id="05cf6-104">SYNTAX</span></span>

### <span data-ttu-id="05cf6-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="05cf6-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cf6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="05cf6-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05cf6-107">설명</span><span class="sxs-lookup"><span data-stu-id="05cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="05cf6-108">**New-AzLoadBalancerRuleConfig** cmdlet은 Azure Load Balancer에 대한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="05cf6-109">예제</span><span class="sxs-lookup"><span data-stu-id="05cf6-109">EXAMPLES</span></span>

### <span data-ttu-id="05cf6-110">예제 1: Azure Load Balancer에 대한 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="05cf6-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="05cf6-111">처음 세 명령은 forth 명령에서 규칙 구성에 대한 프로브, 공용 IP, 프런트 엔드 및 프로브를 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="05cf6-112">첫 번째 명령은 특정 사양을 사용하여 MyLBrule이라는 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="05cf6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05cf6-113">PARAMETERS</span></span>

### <span data-ttu-id="05cf6-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05cf6-114">-BackendAddressPool</span></span>
<span data-ttu-id="05cf6-115">Load Balancer 규칙 구성과 연결하기 위한 **BackendAddressPool** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="05cf6-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="05cf6-117">부하 균형 조정기 규칙 구성과 연결될 **BackendAddressPool** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="05cf6-118">-BackendPort</span></span>
<span data-ttu-id="05cf6-119">이 부하 균형 조정기 규칙 구성과 일치하는 트래픽에 대한 백 끝 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cf6-120">-DefaultProfile</span></span>
<span data-ttu-id="05cf6-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05cf6-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="05cf6-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="05cf6-123">부하 분산 규칙의 프런트 엔드에 지정된 publicIP 주소를 사용하도록 백 엔드 풀의 VM에 대한 SNAT를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="05cf6-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="05cf6-124">-EnableFloatingIP</span></span>
<span data-ttu-id="05cf6-125">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="05cf6-126">-EnableTcpReset</span></span>
<span data-ttu-id="05cf6-127">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="05cf6-128">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="05cf6-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="05cf6-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="05cf6-130">부하 균형 조정기 규칙 구성과 연결될 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="05cf6-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="05cf6-132">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="05cf6-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="05cf6-133">-FrontendPort</span></span>
<span data-ttu-id="05cf6-134">부하 균형 조정기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="05cf6-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="05cf6-136">대화 상태가 부하 균형 조정기에서 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="05cf6-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="05cf6-137">-LoadDistribution</span></span>
<span data-ttu-id="05cf6-138">부하 분산을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-138">Specifies a load distribution.</span></span>
<span data-ttu-id="05cf6-139">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="05cf6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05cf6-140">기본값</span><span class="sxs-lookup"><span data-stu-id="05cf6-140">Default</span></span>
- <span data-ttu-id="05cf6-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="05cf6-141">SourceIP</span></span>
- <span data-ttu-id="05cf6-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="05cf6-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="05cf6-143">-Name</span><span class="sxs-lookup"><span data-stu-id="05cf6-143">-Name</span></span>
<span data-ttu-id="05cf6-144">이 cmdlet에서 만드는 부하 분산 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="05cf6-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="05cf6-145">-Probe</span></span>
<span data-ttu-id="05cf6-146">부하 균형 조정기 규칙 구성과 연결하기 위한 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="05cf6-147">-ProbeId</span></span>
<span data-ttu-id="05cf6-148">부하 균형 조정기 규칙 구성과 연결될 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="05cf6-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="05cf6-149">-Protocol</span></span>
<span data-ttu-id="05cf6-150">부하 균형 조정기 규칙 구성과 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="05cf6-151">이 매개 변수에 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="05cf6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05cf6-152">-Confirm</span></span>
<span data-ttu-id="05cf6-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cf6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cf6-154">-WhatIf</span></span>
<span data-ttu-id="05cf6-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="05cf6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05cf6-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cf6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cf6-157">CommonParameters</span></span>
<span data-ttu-id="05cf6-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05cf6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cf6-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="05cf6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cf6-160">입력</span><span class="sxs-lookup"><span data-stu-id="05cf6-160">INPUTS</span></span>

### <span data-ttu-id="05cf6-161">System.String</span><span class="sxs-lookup"><span data-stu-id="05cf6-161">System.String</span></span>

### <span data-ttu-id="05cf6-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="05cf6-162">System.Int32</span></span>

### <span data-ttu-id="05cf6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="05cf6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="05cf6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05cf6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="05cf6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="05cf6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="05cf6-166">출력</span><span class="sxs-lookup"><span data-stu-id="05cf6-166">OUTPUTS</span></span>

### <span data-ttu-id="05cf6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="05cf6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="05cf6-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05cf6-168">NOTES</span></span>

## <span data-ttu-id="05cf6-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05cf6-169">RELATED LINKS</span></span>

[<span data-ttu-id="05cf6-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05cf6-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="05cf6-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05cf6-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="05cf6-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05cf6-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="05cf6-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05cf6-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

