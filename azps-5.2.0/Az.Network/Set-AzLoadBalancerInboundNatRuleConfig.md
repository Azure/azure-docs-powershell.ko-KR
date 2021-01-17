---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356665"
---
# <span data-ttu-id="a890d-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a890d-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a890d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a890d-102">SYNOPSIS</span></span>
<span data-ttu-id="a890d-103">부하 균형 조정에 대한 인바운드 NAT 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a890d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a890d-104">SYNTAX</span></span>

### <span data-ttu-id="a890d-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a890d-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a890d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a890d-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a890d-107">설명</span><span class="sxs-lookup"><span data-stu-id="a890d-107">DESCRIPTION</span></span>
<span data-ttu-id="a890d-108">**Set-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure Load Balancer에 대한 인바운드 NAT(네트워크 주소 변환) 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a890d-109">예제</span><span class="sxs-lookup"><span data-stu-id="a890d-109">EXAMPLES</span></span>

### <span data-ttu-id="a890d-110">예제 1: 부하 균형 조정기에서 인바운드 NAT 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="a890d-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="a890d-111">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 힌트한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a890d-112">두 번째 명령은 파이프라인 연산자를 사용하여 $slb Load Balancer를 Add-AzLoadBalancerInboundNatRuleConfig에 전달합니다. 이 명령은 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="a890d-113">세 번째 명령은 Load **Balancer를 Set-AzLoadBalancerInboundNatRuleConfig에** 전달합니다. 이 명령은 인바운드 NAT 규칙 구성을 저장하고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="a890d-114">규칙 구성은 이전 명령에서 사용하도록 설정한 부동 IP를 사용하도록 설정하지 않고 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="a890d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a890d-115">PARAMETERS</span></span>

### <span data-ttu-id="a890d-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a890d-116">-BackendPort</span></span>
<span data-ttu-id="a890d-117">이 규칙 구성과 일치하는 트래픽에 대한 백투인 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a890d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a890d-118">-DefaultProfile</span></span>
<span data-ttu-id="a890d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a890d-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a890d-120">-EnableFloatingIP</span></span>
<span data-ttu-id="a890d-121">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a890d-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a890d-122">-EnableTcpReset</span></span>
<span data-ttu-id="a890d-123">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a890d-124">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a890d-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a890d-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a890d-126">인바운드 NAT 규칙 구성과 연결하기 위한 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a890d-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a890d-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a890d-128">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a890d-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a890d-129">-FrontendPort</span></span>
<span data-ttu-id="a890d-130">부하 균형 조정기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a890d-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a890d-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a890d-132">대화 상태가 부하 균형 조정기에서 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a890d-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a890d-133">-LoadBalancer</span></span>
<span data-ttu-id="a890d-134">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-134">Specifies a load balancer.</span></span>
<span data-ttu-id="a890d-135">이 cmdlet은 이 매개 변수가 지정하는 부하 균형 조정에 대한 인바운드 NAT 규칙 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a890d-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a890d-136">-Name</span></span>
<span data-ttu-id="a890d-137">인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a890d-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a890d-138">-Protocol</span></span>
<span data-ttu-id="a890d-139">인바운드 NAT 규칙 구성과 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="a890d-140">이 매개 변수에 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a890d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a890d-141">-Confirm</span></span>
<span data-ttu-id="a890d-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a890d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a890d-143">-WhatIf</span></span>
<span data-ttu-id="a890d-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a890d-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a890d-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a890d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a890d-146">CommonParameters</span></span>
<span data-ttu-id="a890d-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a890d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a890d-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a890d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a890d-149">입력</span><span class="sxs-lookup"><span data-stu-id="a890d-149">INPUTS</span></span>

### <span data-ttu-id="a890d-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a890d-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a890d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a890d-151">System.String</span></span>

### <span data-ttu-id="a890d-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a890d-152">System.Int32</span></span>

### <span data-ttu-id="a890d-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a890d-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a890d-154">출력</span><span class="sxs-lookup"><span data-stu-id="a890d-154">OUTPUTS</span></span>

### <span data-ttu-id="a890d-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a890d-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a890d-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a890d-156">NOTES</span></span>

## <span data-ttu-id="a890d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a890d-157">RELATED LINKS</span></span>

[<span data-ttu-id="a890d-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a890d-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a890d-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a890d-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a890d-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a890d-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a890d-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a890d-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a890d-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a890d-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


