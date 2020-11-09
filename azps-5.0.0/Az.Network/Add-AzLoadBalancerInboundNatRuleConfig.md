---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311513"
---
# <span data-ttu-id="b770f-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b770f-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b770f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b770f-102">SYNOPSIS</span></span>
<span data-ttu-id="b770f-103">부하 분산 장치에 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b770f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b770f-104">SYNTAX</span></span>

### <span data-ttu-id="b770f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b770f-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b770f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b770f-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b770f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b770f-107">DESCRIPTION</span></span>
<span data-ttu-id="b770f-108">**Add-AzLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 인바운드 NAT (network address translation) 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b770f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b770f-109">EXAMPLES</span></span>

### <span data-ttu-id="b770f-110">예제 1: 부하 분산 장치에 인바운드 NAT 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="b770f-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="b770f-111">첫 번째 명령은 MyloadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b770f-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzLoadBalancerInboundNatRuleConfig** 에 전달 하 고,이는 인바운드 NAT 규칙 구성을 부하 분산 장치에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="b770f-113">변수</span><span class="sxs-lookup"><span data-stu-id="b770f-113">PARAMETERS</span></span>

### <span data-ttu-id="b770f-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b770f-114">-BackendPort</span></span>
<span data-ttu-id="b770f-115">규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b770f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b770f-116">-DefaultProfile</span></span>
<span data-ttu-id="b770f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b770f-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b770f-118">-EnableFloatingIP</span></span>
<span data-ttu-id="b770f-119">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b770f-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b770f-120">-EnableTcpReset</span></span>
<span data-ttu-id="b770f-121">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b770f-122">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b770f-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b770f-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b770f-124">인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b770f-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b770f-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b770f-126">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b770f-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b770f-127">-FrontendPort</span></span>
<span data-ttu-id="b770f-128">규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="b770f-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b770f-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b770f-130">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b770f-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b770f-131">-LoadBalancer</span></span>
<span data-ttu-id="b770f-132">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b770f-133">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b770f-134">-이름</span><span class="sxs-lookup"><span data-stu-id="b770f-134">-Name</span></span>
<span data-ttu-id="b770f-135">추가할 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="b770f-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b770f-136">-Protocol</span></span>
<span data-ttu-id="b770f-137">인바운드 NAT 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="b770f-138">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b770f-139">-확인</span><span class="sxs-lookup"><span data-stu-id="b770f-139">-Confirm</span></span>
<span data-ttu-id="b770f-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b770f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b770f-141">-WhatIf</span></span>
<span data-ttu-id="b770f-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b770f-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b770f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b770f-144">CommonParameters</span></span>
<span data-ttu-id="b770f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b770f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b770f-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b770f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b770f-147">입력</span><span class="sxs-lookup"><span data-stu-id="b770f-147">INPUTS</span></span>

### <span data-ttu-id="b770f-148">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b770f-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b770f-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b770f-149">System.String</span></span>

### <span data-ttu-id="b770f-150">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b770f-150">System.Int32</span></span>

### <span data-ttu-id="b770f-151">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b770f-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b770f-152">출력</span><span class="sxs-lookup"><span data-stu-id="b770f-152">OUTPUTS</span></span>

### <span data-ttu-id="b770f-153">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b770f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b770f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="b770f-154">NOTES</span></span>

## <span data-ttu-id="b770f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b770f-155">RELATED LINKS</span></span>

[<span data-ttu-id="b770f-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b770f-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b770f-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b770f-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b770f-158">새로운 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b770f-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b770f-159">제거-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b770f-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b770f-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b770f-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="b770f-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b770f-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


