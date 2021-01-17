---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491848"
---
# <span data-ttu-id="410e0-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="410e0-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="410e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410e0-102">SYNOPSIS</span></span>
<span data-ttu-id="410e0-103">부하 균형 조정에 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="410e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="410e0-104">SYNTAX</span></span>

### <span data-ttu-id="410e0-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="410e0-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="410e0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="410e0-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410e0-107">설명</span><span class="sxs-lookup"><span data-stu-id="410e0-107">DESCRIPTION</span></span>
<span data-ttu-id="410e0-108">**Add-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure Load Balancer에 인바운드 NAT(네트워크 주소 변환) 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="410e0-109">예제</span><span class="sxs-lookup"><span data-stu-id="410e0-109">EXAMPLES</span></span>

### <span data-ttu-id="410e0-110">예제 1: 부하 균형 조정에 인바운드 NAT 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="410e0-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="410e0-111">첫 번째 명령은 MyloadBalancer라는 부하 분산 장치와 해당 부하 분산 $slb.</span><span class="sxs-lookup"><span data-stu-id="410e0-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="410e0-112">두 번째 명령은 파이프라인 연산자를 사용하여 $slb Load Balancer에 인바운드 NAT 규칙 구성을 추가하는 **Add-AzLoadBalancerInboundNatRuleConfig에** 부하 분산을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="410e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="410e0-113">PARAMETERS</span></span>

### <span data-ttu-id="410e0-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="410e0-114">-BackendPort</span></span>
<span data-ttu-id="410e0-115">규칙 구성에 의해 일치된 트래픽에 대한 백 끝 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="410e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410e0-116">-DefaultProfile</span></span>
<span data-ttu-id="410e0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="410e0-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="410e0-118">-EnableFloatingIP</span></span>
<span data-ttu-id="410e0-119">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="410e0-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="410e0-120">-EnableTcpReset</span></span>
<span data-ttu-id="410e0-121">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="410e0-122">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="410e0-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="410e0-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="410e0-124">인바운드 NAT 규칙 구성과 연결하기 위한 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="410e0-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="410e0-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="410e0-126">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="410e0-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="410e0-127">-FrontendPort</span></span>
<span data-ttu-id="410e0-128">규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="410e0-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="410e0-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="410e0-130">대화 상태가 부하 균형 조정기에서 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="410e0-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="410e0-131">-LoadBalancer</span></span>
<span data-ttu-id="410e0-132">**LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="410e0-133">이 cmdlet은 이 매개 변수가 지정하는 부하 균형 조정에 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="410e0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="410e0-134">-Name</span></span>
<span data-ttu-id="410e0-135">추가할 인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="410e0-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="410e0-136">-Protocol</span></span>
<span data-ttu-id="410e0-137">인바운드 NAT 규칙과 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="410e0-138">이 매개 변수에 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="410e0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="410e0-139">-Confirm</span></span>
<span data-ttu-id="410e0-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410e0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410e0-141">-WhatIf</span></span>
<span data-ttu-id="410e0-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="410e0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="410e0-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410e0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410e0-144">CommonParameters</span></span>
<span data-ttu-id="410e0-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="410e0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410e0-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="410e0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410e0-147">입력</span><span class="sxs-lookup"><span data-stu-id="410e0-147">INPUTS</span></span>

### <span data-ttu-id="410e0-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="410e0-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="410e0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="410e0-149">System.String</span></span>

### <span data-ttu-id="410e0-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="410e0-150">System.Int32</span></span>

### <span data-ttu-id="410e0-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="410e0-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="410e0-152">출력</span><span class="sxs-lookup"><span data-stu-id="410e0-152">OUTPUTS</span></span>

### <span data-ttu-id="410e0-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="410e0-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="410e0-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="410e0-154">NOTES</span></span>

## <span data-ttu-id="410e0-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="410e0-155">RELATED LINKS</span></span>

[<span data-ttu-id="410e0-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="410e0-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="410e0-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="410e0-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="410e0-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="410e0-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="410e0-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="410e0-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="410e0-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="410e0-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="410e0-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="410e0-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


