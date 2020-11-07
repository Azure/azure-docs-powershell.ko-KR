---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 28545d2e92e75a08de7381c03ddc4bf3782d59d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869909"
---
# <span data-ttu-id="7b1e0-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b1e0-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7b1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1e0-103">부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7b1e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b1e0-104">SYNTAX</span></span>

### <span data-ttu-id="7b1e0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b1e0-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b1e0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b1e0-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7b1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="7b1e0-108">**AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7b1e0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7b1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="7b1e0-110">1: Azure 부하 분산 장치에 대 한 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="7b1e0-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="7b1e0-111">처음 세 개의 명령은 공용 IP, 프론트 엔드, 그리고 위의 명령에서 규칙 구성에 대 한 프로브를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="7b1e0-112">위의 명령은 특정 사양을 사용 하 여 MyLBrule 이라는 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="7b1e0-113">변수</span><span class="sxs-lookup"><span data-stu-id="7b1e0-113">PARAMETERS</span></span>

### <span data-ttu-id="7b1e0-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b1e0-114">-BackendAddressPool</span></span>
<span data-ttu-id="7b1e0-115">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7b1e0-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="7b1e0-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7b1e0-118">-BackendPort</span></span>
<span data-ttu-id="7b1e0-119">이 부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1e0-120">-DefaultProfile</span></span>
<span data-ttu-id="7b1e0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1e0-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7b1e0-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7b1e0-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7b1e0-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7b1e0-124">-EnableFloatingIP</span></span>
<span data-ttu-id="7b1e0-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7b1e0-126">-EnableTcpReset</span></span>
<span data-ttu-id="7b1e0-127">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7b1e0-128">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7b1e0-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b1e0-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7b1e0-130">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7b1e0-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7b1e0-132">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7b1e0-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7b1e0-133">-FrontendPort</span></span>
<span data-ttu-id="7b1e0-134">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b1e0-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7b1e0-136">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7b1e0-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7b1e0-137">-LoadDistribution</span></span>
<span data-ttu-id="7b1e0-138">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-138">Specifies a load distribution.</span></span>
<span data-ttu-id="7b1e0-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7b1e0-140">기본값</span><span class="sxs-lookup"><span data-stu-id="7b1e0-140">Default</span></span>
- <span data-ttu-id="7b1e0-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="7b1e0-141">SourceIP</span></span>
- <span data-ttu-id="7b1e0-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="7b1e0-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="7b1e0-143">-이름</span><span class="sxs-lookup"><span data-stu-id="7b1e0-143">-Name</span></span>
<span data-ttu-id="7b1e0-144">이 cmdlet이 만드는 부하 분산 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7b1e0-145">-프로브</span><span class="sxs-lookup"><span data-stu-id="7b1e0-145">-Probe</span></span>
<span data-ttu-id="7b1e0-146">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="7b1e0-147">-ProbeId</span></span>
<span data-ttu-id="7b1e0-148">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7b1e0-149">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7b1e0-149">-Protocol</span></span>
<span data-ttu-id="7b1e0-150">부하 분산 장치 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="7b1e0-151">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7b1e0-152">-확인</span><span class="sxs-lookup"><span data-stu-id="7b1e0-152">-Confirm</span></span>
<span data-ttu-id="7b1e0-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1e0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b1e0-154">-WhatIf</span></span>
<span data-ttu-id="7b1e0-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b1e0-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1e0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1e0-157">CommonParameters</span></span>
<span data-ttu-id="7b1e0-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1e0-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b1e0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1e0-160">입력</span><span class="sxs-lookup"><span data-stu-id="7b1e0-160">INPUTS</span></span>

### <span data-ttu-id="7b1e0-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b1e0-161">System.String</span></span>

### <span data-ttu-id="7b1e0-162">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-162">System.Int32</span></span>

### <span data-ttu-id="7b1e0-163">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="7b1e0-164">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="7b1e0-165">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="7b1e0-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="7b1e0-166">출력</span><span class="sxs-lookup"><span data-stu-id="7b1e0-166">OUTPUTS</span></span>

### <span data-ttu-id="7b1e0-167">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b1e0-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="7b1e0-168">상속자</span><span class="sxs-lookup"><span data-stu-id="7b1e0-168">NOTES</span></span>

## <span data-ttu-id="7b1e0-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b1e0-169">RELATED LINKS</span></span>

[<span data-ttu-id="7b1e0-170">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b1e0-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b1e0-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b1e0-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b1e0-172">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b1e0-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7b1e0-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b1e0-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


