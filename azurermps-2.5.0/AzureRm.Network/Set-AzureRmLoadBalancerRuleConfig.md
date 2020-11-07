---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 59e20a557c0e32d35dd853a0b3ff7e619ec2a955
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881310"
---
# <span data-ttu-id="3890e-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3890e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3890e-102">SYNOPSIS</span></span>
<span data-ttu-id="3890e-103">부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3890e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3890e-104">SYNTAX</span></span>

### <span data-ttu-id="3890e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3890e-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3890e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3890e-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3890e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3890e-107">DESCRIPTION</span></span>
<span data-ttu-id="3890e-108">**AzureRmLoadBalancerRuleConfig** cmdlet은 부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="3890e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3890e-109">EXAMPLES</span></span>

### <span data-ttu-id="3890e-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="3890e-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="3890e-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="3890e-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 Add-AzureRmLoadBalancerRuleConfig에 전달 하 여 NewRule 이라는 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="3890e-113">세 번째 명령은 새 규칙 구성을 설정 하는 **AzureRmLoadBalancerRuleConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="3890e-114">이 구성은 이전 명령에서 사용 하도록 설정한 부동 IP 주소를 사용 하도록 설정 하지 않는다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="3890e-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="3890e-115">변수</span><span class="sxs-lookup"><span data-stu-id="3890e-115">PARAMETERS</span></span>

### <span data-ttu-id="3890e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3890e-116">-BackendAddressPool</span></span>
<span data-ttu-id="3890e-117">부하 분산 장치 규칙과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3890e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="3890e-119">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3890e-120">-BackendPort</span></span>
<span data-ttu-id="3890e-121">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3890e-122">-DefaultProfile</span></span>
<span data-ttu-id="3890e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="3890e-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="3890e-125">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="3890e-126">-EnableFloatingIP</span></span>
<span data-ttu-id="3890e-127">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3890e-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3890e-129">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3890e-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3890e-131">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3890e-132">-FrontendPort</span></span>
<span data-ttu-id="3890e-133">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3890e-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3890e-135">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3890e-136">-LoadBalancer</span></span>
<span data-ttu-id="3890e-137">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-137">Specifies a load balancer.</span></span>
<span data-ttu-id="3890e-138">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="3890e-139">-LoadDistribution</span></span>
<span data-ttu-id="3890e-140">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-140">Specifies a load distribution.</span></span>
<span data-ttu-id="3890e-141">이 매개 변수에 허용 되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-142">-이름</span><span class="sxs-lookup"><span data-stu-id="3890e-142">-Name</span></span>
<span data-ttu-id="3890e-143">부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-143">Specifies the name of a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-144">-프로브</span><span class="sxs-lookup"><span data-stu-id="3890e-144">-Probe</span></span>
<span data-ttu-id="3890e-145">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="3890e-146">-ProbeId</span></span>
<span data-ttu-id="3890e-147">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-148">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="3890e-148">-Protocol</span></span>
<span data-ttu-id="3890e-149">부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="3890e-150">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3890e-151">CommonParameters</span></span>
<span data-ttu-id="3890e-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3890e-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3890e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3890e-154">입력</span><span class="sxs-lookup"><span data-stu-id="3890e-154">INPUTS</span></span>

### <span data-ttu-id="3890e-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3890e-155">PSLoadBalancer</span></span>
<span data-ttu-id="3890e-156">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3890e-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3890e-157">출력</span><span class="sxs-lookup"><span data-stu-id="3890e-157">OUTPUTS</span></span>

### <span data-ttu-id="3890e-158">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3890e-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3890e-159">상속자</span><span class="sxs-lookup"><span data-stu-id="3890e-159">NOTES</span></span>

## <span data-ttu-id="3890e-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3890e-160">RELATED LINKS</span></span>

[<span data-ttu-id="3890e-161">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3890e-162">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3890e-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3890e-164">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3890e-165">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3890e-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


