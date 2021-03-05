---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006507"
---
# <span data-ttu-id="a8df3-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8df3-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a8df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8df3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8df3-103">부하 저울에 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="a8df3-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8df3-104">SYNTAX</span></span>

### <span data-ttu-id="a8df3-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a8df3-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8df3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8df3-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8df3-107">설명</span><span class="sxs-lookup"><span data-stu-id="a8df3-107">DESCRIPTION</span></span>
<span data-ttu-id="a8df3-108">**Add-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure 부하 분산기에 NAT(인바운드 네트워크 주소 변환) 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a8df3-109">예제</span><span class="sxs-lookup"><span data-stu-id="a8df3-109">EXAMPLES</span></span>

### <span data-ttu-id="a8df3-110">예제 1: 부하 저울에 인바운드 NAT 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="a8df3-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="a8df3-111">첫 번째 명령은 MyloadBalancer라는 부하 분산 장치 를 얻은 다음 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="a8df3-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a8df3-112">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb **Add-AzLoadBalancerInboundNatRuleConfig에** 전달하여 부하 분산기에 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="a8df3-113">마지막 명령은 Set-AzLoadBalancer를 수행하지 않는 경우 부하 분산에 변경 내용이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="a8df3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8df3-114">PARAMETERS</span></span>

### <span data-ttu-id="a8df3-115">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a8df3-115">-BackendPort</span></span>
<span data-ttu-id="a8df3-116">규칙 구성과 일치하는 트래픽에 대한 백던드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="a8df3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8df3-117">-DefaultProfile</span></span>
<span data-ttu-id="a8df3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8df3-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a8df3-119">-EnableFloatingIP</span></span>
<span data-ttu-id="a8df3-120">이 cmdlet은 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a8df3-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a8df3-121">-EnableTcpReset</span></span>
<span data-ttu-id="a8df3-122">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a8df3-123">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a8df3-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8df3-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a8df3-125">인바운드 NAT 규칙 구성과 연결하기 위한 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a8df3-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a8df3-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a8df3-127">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a8df3-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a8df3-128">-FrontendPort</span></span>
<span data-ttu-id="a8df3-129">규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="a8df3-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a8df3-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a8df3-131">대화 상태가 부하 조정기에서 유지 관리되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a8df3-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8df3-132">-LoadBalancer</span></span>
<span data-ttu-id="a8df3-133">**LoadBalancer 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a8df3-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a8df3-134">이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 인바운드 NAT 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8df3-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a8df3-135">-Name</span></span>
<span data-ttu-id="a8df3-136">추가할 인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="a8df3-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a8df3-137">-Protocol</span></span>
<span data-ttu-id="a8df3-138">인바운드 NAT 규칙과 일치하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="a8df3-139">이 매개 변수에 대해 허용되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a8df3-140">-확인</span><span class="sxs-lookup"><span data-stu-id="a8df3-140">-Confirm</span></span>
<span data-ttu-id="a8df3-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8df3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8df3-142">-WhatIf</span></span>
<span data-ttu-id="a8df3-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8df3-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8df3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8df3-145">CommonParameters</span></span>
<span data-ttu-id="a8df3-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8df3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8df3-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a8df3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8df3-148">입력</span><span class="sxs-lookup"><span data-stu-id="a8df3-148">INPUTS</span></span>

### <span data-ttu-id="a8df3-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8df3-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a8df3-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a8df3-150">System.String</span></span>

### <span data-ttu-id="a8df3-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a8df3-151">System.Int32</span></span>

### <span data-ttu-id="a8df3-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8df3-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a8df3-153">출력</span><span class="sxs-lookup"><span data-stu-id="a8df3-153">OUTPUTS</span></span>

### <span data-ttu-id="a8df3-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8df3-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a8df3-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8df3-155">NOTES</span></span>

## <span data-ttu-id="a8df3-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8df3-156">RELATED LINKS</span></span>

[<span data-ttu-id="a8df3-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8df3-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a8df3-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8df3-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a8df3-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8df3-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a8df3-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8df3-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a8df3-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8df3-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="a8df3-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8df3-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


