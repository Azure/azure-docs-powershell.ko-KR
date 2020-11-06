---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 2b9c835e99a088a075656cd985004663e5ef094a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529275"
---
# <span data-ttu-id="6cc82-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6cc82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc82-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc82-103">부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cc82-104">SYNTAX</span></span>

### <span data-ttu-id="6cc82-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6cc82-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cc82-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6cc82-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc82-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6cc82-107">DESCRIPTION</span></span>
<span data-ttu-id="6cc82-108">**AzureRmLoadBalancerRuleConfig** cmdlet은 부하 분산 장치 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="6cc82-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6cc82-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc82-110">예제 1: 부하 분산 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="6cc82-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="6cc82-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="6cc82-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 Add-AzureRmLoadBalancerRuleConfig에 전달 하 여 NewRule 이라는 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="6cc82-113">세 번째 명령은 새 규칙 구성을 설정 하는 **AzureRmLoadBalancerRuleConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="6cc82-114">이 구성은 이전 명령에서 사용 하도록 설정한 부동 IP 주소를 사용 하도록 설정 하지 않는다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cc82-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="6cc82-115">변수</span><span class="sxs-lookup"><span data-stu-id="6cc82-115">PARAMETERS</span></span>

### <span data-ttu-id="6cc82-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6cc82-116">-BackendAddressPool</span></span>
<span data-ttu-id="6cc82-117">부하 분산 장치 규칙과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6cc82-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6cc82-119">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6cc82-120">-BackendPort</span></span>
<span data-ttu-id="6cc82-121">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6cc82-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6cc82-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6cc82-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6cc82-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6cc82-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6cc82-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cc82-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6cc82-127">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6cc82-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6cc82-129">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6cc82-130">-FrontendPort</span></span>
<span data-ttu-id="6cc82-131">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6cc82-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6cc82-133">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cc82-134">-LoadBalancer</span></span>
<span data-ttu-id="6cc82-135">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-135">Specifies a load balancer.</span></span>
<span data-ttu-id="6cc82-136">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-136">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6cc82-137">-LoadDistribution</span></span>
<span data-ttu-id="6cc82-138">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-138">Specifies a load distribution.</span></span>
<span data-ttu-id="6cc82-139">이 매개 변수에 허용 되는 값은 SourceIP 및 SourceIPProtocol입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-139">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-140">-이름</span><span class="sxs-lookup"><span data-stu-id="6cc82-140">-Name</span></span>
<span data-ttu-id="6cc82-141">부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-141">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="6cc82-142">-프로브</span><span class="sxs-lookup"><span data-stu-id="6cc82-142">-Probe</span></span>
<span data-ttu-id="6cc82-143">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6cc82-144">-ProbeId</span></span>
<span data-ttu-id="6cc82-145">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-146">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="6cc82-146">-Protocol</span></span>
<span data-ttu-id="6cc82-147">부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-147">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6cc82-148">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc82-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc82-149">-DefaultProfile</span></span>
<span data-ttu-id="6cc82-150">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc82-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc82-151">CommonParameters</span></span>
<span data-ttu-id="6cc82-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc82-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc82-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc82-154">입력</span><span class="sxs-lookup"><span data-stu-id="6cc82-154">INPUTS</span></span>

### <span data-ttu-id="6cc82-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cc82-155">PSLoadBalancer</span></span>
<span data-ttu-id="6cc82-156">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc82-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6cc82-157">출력</span><span class="sxs-lookup"><span data-stu-id="6cc82-157">OUTPUTS</span></span>

### <span data-ttu-id="6cc82-158">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cc82-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6cc82-159">상속자</span><span class="sxs-lookup"><span data-stu-id="6cc82-159">NOTES</span></span>

## <span data-ttu-id="6cc82-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cc82-160">RELATED LINKS</span></span>

[<span data-ttu-id="6cc82-161">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6cc82-162">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6cc82-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6cc82-164">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6cc82-165">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc82-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


