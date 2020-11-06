---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531385"
---
# <span data-ttu-id="97c52-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="97c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c52-102">SYNOPSIS</span></span>
<span data-ttu-id="97c52-103">부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97c52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97c52-104">SYNTAX</span></span>

### <span data-ttu-id="97c52-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="97c52-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c52-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97c52-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c52-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97c52-107">DESCRIPTION</span></span>
<span data-ttu-id="97c52-108">**AzureRmLoadBalancerRuleConfig** cmdlet은 부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="97c52-109">예제의</span><span class="sxs-lookup"><span data-stu-id="97c52-109">EXAMPLES</span></span>

### <span data-ttu-id="97c52-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="97c52-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="97c52-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="97c52-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 Add-AzureRmLoadBalancerRuleConfig에 전달 하 여 NewRule 이라는 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="97c52-113">세 번째 명령은 새 규칙 구성을 설정 하는 **AzureRmLoadBalancerRuleConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="97c52-114">이 구성은 이전 명령에서 사용 하도록 설정한 부동 IP 주소를 사용 하도록 설정 하지 않는다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="97c52-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="97c52-115">변수</span><span class="sxs-lookup"><span data-stu-id="97c52-115">PARAMETERS</span></span>

### <span data-ttu-id="97c52-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97c52-116">-BackendAddressPool</span></span>
<span data-ttu-id="97c52-117">부하 분산 장치 규칙과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="97c52-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97c52-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="97c52-119">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="97c52-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="97c52-120">-BackendPort</span></span>
<span data-ttu-id="97c52-121">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="97c52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c52-122">-DefaultProfile</span></span>
<span data-ttu-id="97c52-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c52-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="97c52-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="97c52-125">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="97c52-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="97c52-126">-EnableFloatingIP</span></span>
<span data-ttu-id="97c52-127">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="97c52-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="97c52-128">-EnableTcpReset</span></span>
<span data-ttu-id="97c52-129">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="97c52-130">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="97c52-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c52-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="97c52-132">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="97c52-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="97c52-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="97c52-134">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="97c52-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="97c52-135">-FrontendPort</span></span>
<span data-ttu-id="97c52-136">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="97c52-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="97c52-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="97c52-138">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="97c52-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97c52-139">-LoadBalancer</span></span>
<span data-ttu-id="97c52-140">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-140">Specifies a load balancer.</span></span>
<span data-ttu-id="97c52-141">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="97c52-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="97c52-142">-LoadDistribution</span></span>
<span data-ttu-id="97c52-143">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-143">Specifies a load distribution.</span></span>
<span data-ttu-id="97c52-144">이 매개 변수에 허용 되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="97c52-145">-이름</span><span class="sxs-lookup"><span data-stu-id="97c52-145">-Name</span></span>
<span data-ttu-id="97c52-146">부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="97c52-147">-프로브</span><span class="sxs-lookup"><span data-stu-id="97c52-147">-Probe</span></span>
<span data-ttu-id="97c52-148">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="97c52-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="97c52-149">-ProbeId</span></span>
<span data-ttu-id="97c52-150">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="97c52-151">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="97c52-151">-Protocol</span></span>
<span data-ttu-id="97c52-152">부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="97c52-153">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="97c52-154">-확인</span><span class="sxs-lookup"><span data-stu-id="97c52-154">-Confirm</span></span>
<span data-ttu-id="97c52-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c52-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c52-156">-WhatIf</span></span>
<span data-ttu-id="97c52-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97c52-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c52-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c52-159">CommonParameters</span></span>
<span data-ttu-id="97c52-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c52-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c52-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c52-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c52-162">입력</span><span class="sxs-lookup"><span data-stu-id="97c52-162">INPUTS</span></span>

### <span data-ttu-id="97c52-163">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97c52-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="97c52-164">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97c52-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="97c52-165">출력</span><span class="sxs-lookup"><span data-stu-id="97c52-165">OUTPUTS</span></span>

### <span data-ttu-id="97c52-166">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97c52-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="97c52-167">상속자</span><span class="sxs-lookup"><span data-stu-id="97c52-167">NOTES</span></span>

## <span data-ttu-id="97c52-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97c52-168">RELATED LINKS</span></span>

[<span data-ttu-id="97c52-169">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="97c52-170">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="97c52-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="97c52-172">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="97c52-173">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="97c52-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


