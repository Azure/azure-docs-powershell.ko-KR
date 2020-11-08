---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214321"
---
# <span data-ttu-id="51692-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51692-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="51692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51692-102">SYNOPSIS</span></span>
<span data-ttu-id="51692-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="51692-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51692-104">SYNTAX</span></span>

### <span data-ttu-id="51692-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="51692-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51692-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51692-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51692-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51692-107">DESCRIPTION</span></span>
<span data-ttu-id="51692-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (network address translation) 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="51692-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51692-109">EXAMPLES</span></span>

### <span data-ttu-id="51692-110">예제 1: 부하 분산 장치에서 인바운드 NAT 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="51692-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="51692-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="51692-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzLoadBalancerInboundNatRuleConfig에 전달 하 여 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="51692-113">세 번째 명령은 인바운드 NAT 규칙 구성을 저장 하 고 업데이트 하는 부하 분산을 **설정-AzLoadBalancerInboundNatRuleConfig** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="51692-114">이전 명령에서 사용 하도록 설정 된 부동 IP를 사용 하지 않고 규칙 구성이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="51692-115">변수</span><span class="sxs-lookup"><span data-stu-id="51692-115">PARAMETERS</span></span>

### <span data-ttu-id="51692-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="51692-116">-BackendPort</span></span>
<span data-ttu-id="51692-117">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="51692-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51692-118">-DefaultProfile</span></span>
<span data-ttu-id="51692-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51692-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51692-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="51692-120">-EnableFloatingIP</span></span>
<span data-ttu-id="51692-121">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51692-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="51692-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="51692-122">-EnableTcpReset</span></span>
<span data-ttu-id="51692-123">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="51692-124">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51692-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="51692-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="51692-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="51692-126">인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="51692-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51692-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="51692-128">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="51692-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="51692-129">-FrontendPort</span></span>
<span data-ttu-id="51692-130">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="51692-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="51692-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="51692-132">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="51692-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51692-133">-LoadBalancer</span></span>
<span data-ttu-id="51692-134">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-134">Specifies a load balancer.</span></span>
<span data-ttu-id="51692-135">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="51692-136">-이름</span><span class="sxs-lookup"><span data-stu-id="51692-136">-Name</span></span>
<span data-ttu-id="51692-137">인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="51692-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="51692-138">-Protocol</span></span>
<span data-ttu-id="51692-139">인바운드 NAT 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="51692-140">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="51692-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="51692-141">-확인</span><span class="sxs-lookup"><span data-stu-id="51692-141">-Confirm</span></span>
<span data-ttu-id="51692-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51692-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51692-143">-WhatIf</span></span>
<span data-ttu-id="51692-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51692-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51692-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51692-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51692-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51692-146">CommonParameters</span></span>
<span data-ttu-id="51692-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51692-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51692-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51692-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51692-149">입력</span><span class="sxs-lookup"><span data-stu-id="51692-149">INPUTS</span></span>

### <span data-ttu-id="51692-150">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51692-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="51692-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51692-151">System.String</span></span>

### <span data-ttu-id="51692-152">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="51692-152">System.Int32</span></span>

### <span data-ttu-id="51692-153">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="51692-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="51692-154">출력</span><span class="sxs-lookup"><span data-stu-id="51692-154">OUTPUTS</span></span>

### <span data-ttu-id="51692-155">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51692-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="51692-156">상속자</span><span class="sxs-lookup"><span data-stu-id="51692-156">NOTES</span></span>

## <span data-ttu-id="51692-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51692-157">RELATED LINKS</span></span>

[<span data-ttu-id="51692-158">추가-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51692-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="51692-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="51692-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="51692-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51692-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="51692-161">새로운 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51692-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="51692-162">제거-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51692-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


