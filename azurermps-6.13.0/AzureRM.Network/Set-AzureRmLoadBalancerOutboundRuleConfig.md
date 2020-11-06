---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1c813a7ac23ae8bc161f10df02ac618d5f6a7a81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531387"
---
# <span data-ttu-id="8d49f-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d49f-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="8d49f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d49f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d49f-103">부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-103">Sets an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d49f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d49f-104">SYNTAX</span></span>

### <span data-ttu-id="8d49f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d49f-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d49f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d49f-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d49f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d49f-107">DESCRIPTION</span></span>
<span data-ttu-id="8d49f-108">**AzureRmLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-108">The **Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8d49f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d49f-109">EXAMPLES</span></span>

### <span data-ttu-id="8d49f-110">예제 1: 부하 분산 장치에서 아웃 바운드 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="8d49f-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="8d49f-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8d49f-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 추가-AzureRmLoadBalancerOutboundRuleConfig에 전달 하 여 아웃 바운드 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="8d49f-113">세 번째 명령은 아웃 바운드 규칙 구성을 저장 하 고 업데이트 하는 부하 분산을 **설정-AzureRmLoadBalancerOutboundRuleConfig** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="8d49f-114">변수</span><span class="sxs-lookup"><span data-stu-id="8d49f-114">PARAMETERS</span></span>

### <span data-ttu-id="8d49f-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="8d49f-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="8d49f-116">NAT에 사용 되는 아웃 바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="8d49f-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8d49f-117">-BackendAddressPool</span></span>
<span data-ttu-id="8d49f-118">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8d49f-119">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="8d49f-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8d49f-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="8d49f-121">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8d49f-122">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="8d49f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d49f-123">-DefaultProfile</span></span>
<span data-ttu-id="8d49f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d49f-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8d49f-125">-EnableTcpReset</span></span>
<span data-ttu-id="8d49f-126">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="8d49f-127">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8d49f-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d49f-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8d49f-129">부하 분산 장치의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-129">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d49f-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8d49f-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8d49f-131">TCP 유휴 연결의 제한 시간</span><span class="sxs-lookup"><span data-stu-id="8d49f-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="8d49f-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d49f-132">-LoadBalancer</span></span>
<span data-ttu-id="8d49f-133">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="8d49f-134">-이름</span><span class="sxs-lookup"><span data-stu-id="8d49f-134">-Name</span></span>
<span data-ttu-id="8d49f-135">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="8d49f-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="8d49f-136">-Protocol</span></span>
<span data-ttu-id="8d49f-137">프로토콜-TCP, UDP 또는 All</span><span class="sxs-lookup"><span data-stu-id="8d49f-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="8d49f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8d49f-138">-Confirm</span></span>
<span data-ttu-id="8d49f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d49f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d49f-140">-WhatIf</span></span>
<span data-ttu-id="8d49f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d49f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d49f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d49f-143">CommonParameters</span></span>
<span data-ttu-id="8d49f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d49f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d49f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d49f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d49f-146">입력</span><span class="sxs-lookup"><span data-stu-id="8d49f-146">INPUTS</span></span>

### <span data-ttu-id="8d49f-147">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d49f-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="8d49f-148">시스템.. i n i a n. 목록 \` 1 [[Microsoft azure. PSBackendAddressPool. 모델. PSResourceId, Microsoft azure. commands. 네트워크, 버전 = 6.5.0.0, Culture = 중립, PublicKeyToken = null]] Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d49f-148">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8d49f-149">출력</span><span class="sxs-lookup"><span data-stu-id="8d49f-149">OUTPUTS</span></span>

### <span data-ttu-id="8d49f-150">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d49f-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d49f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="8d49f-151">NOTES</span></span>

## <span data-ttu-id="8d49f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d49f-152">RELATED LINKS</span></span>
