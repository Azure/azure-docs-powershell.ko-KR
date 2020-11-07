---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: e6df07d9d3f133390c6c6d14e092e7983324f753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870846"
---
# <span data-ttu-id="94b22-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94b22-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="94b22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b22-102">SYNOPSIS</span></span>
<span data-ttu-id="94b22-103">부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="94b22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94b22-104">SYNTAX</span></span>

### <span data-ttu-id="94b22-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="94b22-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b22-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94b22-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b22-107">설명은</span><span class="sxs-lookup"><span data-stu-id="94b22-107">DESCRIPTION</span></span>
<span data-ttu-id="94b22-108">**Add-AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="94b22-109">예제의</span><span class="sxs-lookup"><span data-stu-id="94b22-109">EXAMPLES</span></span>

### <span data-ttu-id="94b22-110">예제 1: 부하 분산 장치에 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="94b22-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="94b22-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="94b22-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzLoadBalancerRuleConfig** 에 전달 하 고 newrule 이라는 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="94b22-113">세 번째 명령은 새 부하 분산 장치 규칙 구성을 사용 하 여 azure에서 부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="94b22-114">변수</span><span class="sxs-lookup"><span data-stu-id="94b22-114">PARAMETERS</span></span>

### <span data-ttu-id="94b22-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="94b22-115">-BackendAddressPool</span></span>
<span data-ttu-id="94b22-116">부하 분산 장치 규칙 구성과 연결할 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="94b22-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="94b22-118">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="94b22-119">-BackendPort</span></span>
<span data-ttu-id="94b22-120">부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b22-121">-DefaultProfile</span></span>
<span data-ttu-id="94b22-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94b22-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="94b22-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="94b22-124">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="94b22-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="94b22-125">-EnableFloatingIP</span></span>
<span data-ttu-id="94b22-126">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="94b22-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="94b22-127">-EnableTcpReset</span></span>
<span data-ttu-id="94b22-128">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="94b22-129">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="94b22-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="94b22-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="94b22-131">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="94b22-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="94b22-133">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="94b22-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="94b22-134">-FrontendPort</span></span>
<span data-ttu-id="94b22-135">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="94b22-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="94b22-137">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="94b22-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94b22-138">-LoadBalancer</span></span>
<span data-ttu-id="94b22-139">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="94b22-140">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="94b22-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="94b22-141">-LoadDistribution</span></span>
<span data-ttu-id="94b22-142">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="94b22-143">-이름</span><span class="sxs-lookup"><span data-stu-id="94b22-143">-Name</span></span>
<span data-ttu-id="94b22-144">부하 분산 장치 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-145">-프로브</span><span class="sxs-lookup"><span data-stu-id="94b22-145">-Probe</span></span>
<span data-ttu-id="94b22-146">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="94b22-147">-ProbeId</span></span>
<span data-ttu-id="94b22-148">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="94b22-149">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="94b22-149">-Protocol</span></span>
<span data-ttu-id="94b22-150">부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="94b22-151">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="94b22-152">-확인</span><span class="sxs-lookup"><span data-stu-id="94b22-152">-Confirm</span></span>
<span data-ttu-id="94b22-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b22-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b22-154">-WhatIf</span></span>
<span data-ttu-id="94b22-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94b22-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b22-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b22-157">CommonParameters</span></span>
<span data-ttu-id="94b22-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b22-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b22-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b22-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b22-160">입력</span><span class="sxs-lookup"><span data-stu-id="94b22-160">INPUTS</span></span>

### <span data-ttu-id="94b22-161">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94b22-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="94b22-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94b22-162">System.String</span></span>

### <span data-ttu-id="94b22-163">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="94b22-163">System.Int32</span></span>

### <span data-ttu-id="94b22-164">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="94b22-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="94b22-165">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="94b22-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="94b22-166">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="94b22-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="94b22-167">출력</span><span class="sxs-lookup"><span data-stu-id="94b22-167">OUTPUTS</span></span>

### <span data-ttu-id="94b22-168">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94b22-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="94b22-169">상속자</span><span class="sxs-lookup"><span data-stu-id="94b22-169">NOTES</span></span>

## <span data-ttu-id="94b22-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94b22-170">RELATED LINKS</span></span>

[<span data-ttu-id="94b22-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94b22-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="94b22-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94b22-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="94b22-173">새로운 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94b22-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="94b22-174">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94b22-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="94b22-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94b22-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


