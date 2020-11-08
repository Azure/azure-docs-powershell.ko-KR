---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034493"
---
# <span data-ttu-id="36aa4-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36aa4-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="36aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="36aa4-103">부하 분산 장치에 아웃 바운드 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="36aa4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36aa4-104">SYNTAX</span></span>

### <span data-ttu-id="36aa4-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="36aa4-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36aa4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36aa4-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36aa4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="36aa4-107">DESCRIPTION</span></span>
<span data-ttu-id="36aa4-108">**추가-AzLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에 아웃 바운드 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="36aa4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="36aa4-109">EXAMPLES</span></span>

### <span data-ttu-id="36aa4-110">예제 1: 부하 분산 장치에 아웃 바운드 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="36aa4-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="36aa4-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="36aa4-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzLoadBalancerOutboundRuleConfig** 에 전달 하 고,이는 아웃 바운드 규칙 구성을 부하 분산 장치에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="36aa4-113">변수</span><span class="sxs-lookup"><span data-stu-id="36aa4-113">PARAMETERS</span></span>

### <span data-ttu-id="36aa4-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="36aa4-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="36aa4-115">NAT에 사용 되는 아웃 바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="36aa4-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36aa4-116">-BackendAddressPool</span></span>
<span data-ttu-id="36aa4-117">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="36aa4-118">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36aa4-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="36aa4-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="36aa4-120">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="36aa4-121">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36aa4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36aa4-122">-DefaultProfile</span></span>
<span data-ttu-id="36aa4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36aa4-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="36aa4-124">-EnableTcpReset</span></span>
<span data-ttu-id="36aa4-125">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="36aa4-126">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="36aa4-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="36aa4-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="36aa4-128">부하 분산 장치의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36aa4-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="36aa4-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="36aa4-130">TCP 유휴 연결의 제한 시간</span><span class="sxs-lookup"><span data-stu-id="36aa4-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="36aa4-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36aa4-131">-LoadBalancer</span></span>
<span data-ttu-id="36aa4-132">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="36aa4-133">-이름</span><span class="sxs-lookup"><span data-stu-id="36aa4-133">-Name</span></span>
<span data-ttu-id="36aa4-134">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="36aa4-135">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="36aa4-135">-Protocol</span></span>
<span data-ttu-id="36aa4-136">프로토콜-TCP, UDP 또는 All</span><span class="sxs-lookup"><span data-stu-id="36aa4-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36aa4-137">-확인</span><span class="sxs-lookup"><span data-stu-id="36aa4-137">-Confirm</span></span>
<span data-ttu-id="36aa4-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36aa4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36aa4-139">-WhatIf</span></span>
<span data-ttu-id="36aa4-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36aa4-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36aa4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36aa4-142">CommonParameters</span></span>
<span data-ttu-id="36aa4-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36aa4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36aa4-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36aa4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36aa4-145">입력</span><span class="sxs-lookup"><span data-stu-id="36aa4-145">INPUTS</span></span>

### <span data-ttu-id="36aa4-146">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36aa4-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="36aa4-147">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="36aa4-147">System.Int32</span></span>

### <span data-ttu-id="36aa4-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36aa4-148">System.String</span></span>

### <span data-ttu-id="36aa4-149">Microsoft. 네트워크 모델. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="36aa4-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="36aa4-150">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="36aa4-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="36aa4-151">출력</span><span class="sxs-lookup"><span data-stu-id="36aa4-151">OUTPUTS</span></span>

### <span data-ttu-id="36aa4-152">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36aa4-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="36aa4-153">상속자</span><span class="sxs-lookup"><span data-stu-id="36aa4-153">NOTES</span></span>

## <span data-ttu-id="36aa4-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36aa4-154">RELATED LINKS</span></span>

[<span data-ttu-id="36aa4-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36aa4-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36aa4-156">새로운 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36aa4-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36aa4-157">제거-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36aa4-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="36aa4-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36aa4-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
