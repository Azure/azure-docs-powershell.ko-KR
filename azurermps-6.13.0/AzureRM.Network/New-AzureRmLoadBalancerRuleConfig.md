---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530189"
---
# <span data-ttu-id="dda26-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dda26-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="dda26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda26-102">SYNOPSIS</span></span>
<span data-ttu-id="dda26-103">부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dda26-104">SYNTAX</span></span>

### <span data-ttu-id="dda26-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="dda26-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda26-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dda26-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda26-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dda26-107">DESCRIPTION</span></span>
<span data-ttu-id="dda26-108">**AzureRmLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="dda26-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dda26-109">EXAMPLES</span></span>

### <span data-ttu-id="dda26-110">1: Azure 부하 분산 장치에 대 한 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="dda26-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="dda26-111">처음 세 개의 명령은 공용 IP, 프론트 엔드, 그리고 위의 명령에서 규칙 구성에 대 한 프로브를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="dda26-112">위의 명령은 특정 사양을 사용 하 여 MyLBrule 이라는 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="dda26-113">변수</span><span class="sxs-lookup"><span data-stu-id="dda26-113">PARAMETERS</span></span>

### <span data-ttu-id="dda26-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dda26-114">-BackendAddressPool</span></span>
<span data-ttu-id="dda26-115">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="dda26-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="dda26-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dda26-118">-BackendPort</span></span>
<span data-ttu-id="dda26-119">이 부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda26-120">-DefaultProfile</span></span>
<span data-ttu-id="dda26-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda26-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="dda26-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="dda26-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="dda26-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="dda26-124">-EnableFloatingIP</span></span>
<span data-ttu-id="dda26-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="dda26-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="dda26-126">-EnableTcpReset</span></span>
<span data-ttu-id="dda26-127">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="dda26-128">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dda26-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dda26-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="dda26-130">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dda26-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="dda26-132">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="dda26-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="dda26-133">-FrontendPort</span></span>
<span data-ttu-id="dda26-134">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dda26-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dda26-136">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="dda26-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="dda26-137">-LoadDistribution</span></span>
<span data-ttu-id="dda26-138">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-138">Specifies a load distribution.</span></span>
<span data-ttu-id="dda26-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dda26-140">기본값</span><span class="sxs-lookup"><span data-stu-id="dda26-140">Default</span></span>
- <span data-ttu-id="dda26-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="dda26-141">SourceIP</span></span>
- <span data-ttu-id="dda26-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="dda26-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="dda26-143">-이름</span><span class="sxs-lookup"><span data-stu-id="dda26-143">-Name</span></span>
<span data-ttu-id="dda26-144">이 cmdlet이 만드는 부하 분산 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dda26-145">-프로브</span><span class="sxs-lookup"><span data-stu-id="dda26-145">-Probe</span></span>
<span data-ttu-id="dda26-146">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="dda26-147">-ProbeId</span></span>
<span data-ttu-id="dda26-148">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dda26-149">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="dda26-149">-Protocol</span></span>
<span data-ttu-id="dda26-150">부하 분산 장치 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="dda26-151">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="dda26-152">-확인</span><span class="sxs-lookup"><span data-stu-id="dda26-152">-Confirm</span></span>
<span data-ttu-id="dda26-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda26-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda26-154">-WhatIf</span></span>
<span data-ttu-id="dda26-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dda26-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda26-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda26-157">CommonParameters</span></span>
<span data-ttu-id="dda26-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda26-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda26-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda26-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda26-160">입력</span><span class="sxs-lookup"><span data-stu-id="dda26-160">INPUTS</span></span>

### <span data-ttu-id="dda26-161">않아야</span><span class="sxs-lookup"><span data-stu-id="dda26-161">None</span></span>

## <span data-ttu-id="dda26-162">출력</span><span class="sxs-lookup"><span data-stu-id="dda26-162">OUTPUTS</span></span>

### <span data-ttu-id="dda26-163">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dda26-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="dda26-164">상속자</span><span class="sxs-lookup"><span data-stu-id="dda26-164">NOTES</span></span>

## <span data-ttu-id="dda26-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dda26-165">RELATED LINKS</span></span>

[<span data-ttu-id="dda26-166">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dda26-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dda26-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dda26-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dda26-168">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dda26-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="dda26-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dda26-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


