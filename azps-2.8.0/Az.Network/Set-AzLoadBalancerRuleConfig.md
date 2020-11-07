---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 11baabe406180e92a4a6af0f62b5e3b285e016b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871066"
---
# <span data-ttu-id="49353-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="49353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49353-102">SYNOPSIS</span></span>
<span data-ttu-id="49353-103">부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="49353-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49353-104">SYNTAX</span></span>

### <span data-ttu-id="49353-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="49353-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49353-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="49353-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49353-107">설명은</span><span class="sxs-lookup"><span data-stu-id="49353-107">DESCRIPTION</span></span>
<span data-ttu-id="49353-108">**AzLoadBalancerRuleConfig** cmdlet은 부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="49353-109">예제의</span><span class="sxs-lookup"><span data-stu-id="49353-109">EXAMPLES</span></span>

### <span data-ttu-id="49353-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="49353-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="49353-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="49353-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 Add-AzLoadBalancerRuleConfig에 전달 하 여 NewRule 이라는 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="49353-113">세 번째 명령은 새 규칙 구성을 설정 하는 **AzLoadBalancerRuleConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="49353-114">이 구성은 이전 명령에서 사용 하도록 설정한 부동 IP 주소를 사용 하도록 설정 하지 않는다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="49353-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="49353-115">변수</span><span class="sxs-lookup"><span data-stu-id="49353-115">PARAMETERS</span></span>

### <span data-ttu-id="49353-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49353-116">-BackendAddressPool</span></span>
<span data-ttu-id="49353-117">부하 분산 장치 규칙과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="49353-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="49353-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="49353-119">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49353-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="49353-120">-BackendPort</span></span>
<span data-ttu-id="49353-121">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="49353-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49353-122">-DefaultProfile</span></span>
<span data-ttu-id="49353-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49353-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49353-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="49353-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="49353-125">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="49353-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="49353-126">-EnableFloatingIP</span></span>
<span data-ttu-id="49353-127">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="49353-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="49353-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="49353-128">-EnableTcpReset</span></span>
<span data-ttu-id="49353-129">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="49353-130">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49353-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="49353-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="49353-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="49353-132">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49353-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="49353-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="49353-134">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="49353-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="49353-135">-FrontendPort</span></span>
<span data-ttu-id="49353-136">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49353-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="49353-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="49353-138">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="49353-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49353-139">-LoadBalancer</span></span>
<span data-ttu-id="49353-140">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-140">Specifies a load balancer.</span></span>
<span data-ttu-id="49353-141">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="49353-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="49353-142">-LoadDistribution</span></span>
<span data-ttu-id="49353-143">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-143">Specifies a load distribution.</span></span>
<span data-ttu-id="49353-144">이 매개 변수에 허용 되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="49353-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="49353-145">-이름</span><span class="sxs-lookup"><span data-stu-id="49353-145">-Name</span></span>
<span data-ttu-id="49353-146">부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="49353-147">-프로브</span><span class="sxs-lookup"><span data-stu-id="49353-147">-Probe</span></span>
<span data-ttu-id="49353-148">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49353-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="49353-149">-ProbeId</span></span>
<span data-ttu-id="49353-150">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49353-151">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="49353-151">-Protocol</span></span>
<span data-ttu-id="49353-152">부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="49353-153">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="49353-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="49353-154">-확인</span><span class="sxs-lookup"><span data-stu-id="49353-154">-Confirm</span></span>
<span data-ttu-id="49353-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49353-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49353-156">-WhatIf</span></span>
<span data-ttu-id="49353-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49353-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49353-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49353-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49353-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49353-159">CommonParameters</span></span>
<span data-ttu-id="49353-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49353-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49353-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49353-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49353-162">입력</span><span class="sxs-lookup"><span data-stu-id="49353-162">INPUTS</span></span>

### <span data-ttu-id="49353-163">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49353-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="49353-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49353-164">System.String</span></span>

### <span data-ttu-id="49353-165">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="49353-165">System.Int32</span></span>

### <span data-ttu-id="49353-166">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49353-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="49353-167">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49353-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="49353-168">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="49353-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="49353-169">출력</span><span class="sxs-lookup"><span data-stu-id="49353-169">OUTPUTS</span></span>

### <span data-ttu-id="49353-170">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49353-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="49353-171">상속자</span><span class="sxs-lookup"><span data-stu-id="49353-171">NOTES</span></span>

## <span data-ttu-id="49353-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49353-172">RELATED LINKS</span></span>

[<span data-ttu-id="49353-173">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49353-174">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49353-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49353-176">새로운 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49353-177">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49353-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


