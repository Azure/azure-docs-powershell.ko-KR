---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875668"
---
# <span data-ttu-id="6f2b6-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f2b6-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6f2b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2b6-103">부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="6f2b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f2b6-104">SYNTAX</span></span>

### <span data-ttu-id="6f2b6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f2b6-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f2b6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6f2b6-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f2b6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f2b6-107">DESCRIPTION</span></span>
<span data-ttu-id="6f2b6-108">**Add-AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="6f2b6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6f2b6-109">EXAMPLES</span></span>

### <span data-ttu-id="6f2b6-110">예제 1: 부하 분산 장치에 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="6f2b6-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="6f2b6-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="6f2b6-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzLoadBalancerRuleConfig** 에 전달 하 고 newrule 이라는 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="6f2b6-113">변수</span><span class="sxs-lookup"><span data-stu-id="6f2b6-113">PARAMETERS</span></span>

### <span data-ttu-id="6f2b6-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6f2b6-114">-BackendAddressPool</span></span>
<span data-ttu-id="6f2b6-115">부하 분산 장치 규칙 구성과 연결할 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6f2b6-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="6f2b6-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6f2b6-118">-BackendPort</span></span>
<span data-ttu-id="6f2b6-119">부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2b6-120">-DefaultProfile</span></span>
<span data-ttu-id="6f2b6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f2b6-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6f2b6-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6f2b6-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6f2b6-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6f2b6-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6f2b6-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f2b6-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6f2b6-127">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6f2b6-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6f2b6-129">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6f2b6-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f2b6-130">-FrontendPort</span></span>
<span data-ttu-id="6f2b6-131">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6f2b6-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6f2b6-133">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="6f2b6-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6f2b6-134">-LoadBalancer</span></span>
<span data-ttu-id="6f2b6-135">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="6f2b6-136">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f2b6-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6f2b6-137">-LoadDistribution</span></span>
<span data-ttu-id="6f2b6-138">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="6f2b6-139">-이름</span><span class="sxs-lookup"><span data-stu-id="6f2b6-139">-Name</span></span>
<span data-ttu-id="6f2b6-140">부하 분산 장치 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-141">-프로브</span><span class="sxs-lookup"><span data-stu-id="6f2b6-141">-Probe</span></span>
<span data-ttu-id="6f2b6-142">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6f2b6-143">-ProbeId</span></span>
<span data-ttu-id="6f2b6-144">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6f2b6-145">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="6f2b6-145">-Protocol</span></span>
<span data-ttu-id="6f2b6-146">부하 분산 장치 규칙에 맞는 프로토콜을 Specfies 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6f2b6-147">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6f2b6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2b6-148">CommonParameters</span></span>
<span data-ttu-id="6f2b6-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2b6-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2b6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2b6-151">입력</span><span class="sxs-lookup"><span data-stu-id="6f2b6-151">INPUTS</span></span>

### <span data-ttu-id="6f2b6-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6f2b6-152">PSLoadBalancer</span></span>
<span data-ttu-id="6f2b6-153">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2b6-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6f2b6-154">출력</span><span class="sxs-lookup"><span data-stu-id="6f2b6-154">OUTPUTS</span></span>

### <span data-ttu-id="6f2b6-155">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6f2b6-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6f2b6-156">상속자</span><span class="sxs-lookup"><span data-stu-id="6f2b6-156">NOTES</span></span>

## <span data-ttu-id="6f2b6-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f2b6-157">RELATED LINKS</span></span>

[<span data-ttu-id="6f2b6-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6f2b6-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6f2b6-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f2b6-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6f2b6-160">새로운 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f2b6-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6f2b6-161">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f2b6-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6f2b6-162">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f2b6-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


