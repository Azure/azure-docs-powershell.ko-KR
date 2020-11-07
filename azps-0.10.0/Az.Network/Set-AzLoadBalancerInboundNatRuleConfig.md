---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876579"
---
# <span data-ttu-id="b8eb2-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8eb2-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b8eb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b8eb2-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b8eb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8eb2-104">SYNTAX</span></span>

### <span data-ttu-id="b8eb2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8eb2-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8eb2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8eb2-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8eb2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8eb2-107">DESCRIPTION</span></span>
<span data-ttu-id="b8eb2-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (network address translation) 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b8eb2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8eb2-109">EXAMPLES</span></span>

### <span data-ttu-id="b8eb2-110">예제 1: 부하 분산 장치에서 인바운드 NAT 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="b8eb2-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="b8eb2-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b8eb2-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzLoadBalancerInboundNatRuleConfig에 전달 하 여 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="b8eb2-113">세 번째 명령은 인바운드 NAT 규칙 구성을 저장 하 고 업데이트 하는 부하 분산을 **설정-AzLoadBalancerInboundNatRuleConfig** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="b8eb2-114">이전 명령에서 사용 하도록 설정 된 부동 IP를 사용 하지 않고 규칙 구성이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="b8eb2-115">변수</span><span class="sxs-lookup"><span data-stu-id="b8eb2-115">PARAMETERS</span></span>

### <span data-ttu-id="b8eb2-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b8eb2-116">-BackendPort</span></span>
<span data-ttu-id="b8eb2-117">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="b8eb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8eb2-118">-DefaultProfile</span></span>
<span data-ttu-id="b8eb2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8eb2-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b8eb2-120">-EnableFloatingIP</span></span>
<span data-ttu-id="b8eb2-121">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b8eb2-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8eb2-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b8eb2-123">인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b8eb2-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b8eb2-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b8eb2-125">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b8eb2-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8eb2-126">-FrontendPort</span></span>
<span data-ttu-id="b8eb2-127">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b8eb2-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b8eb2-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b8eb2-129">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b8eb2-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8eb2-130">-LoadBalancer</span></span>
<span data-ttu-id="b8eb2-131">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-131">Specifies a load balancer.</span></span>
<span data-ttu-id="b8eb2-132">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8eb2-133">-이름</span><span class="sxs-lookup"><span data-stu-id="b8eb2-133">-Name</span></span>
<span data-ttu-id="b8eb2-134">인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b8eb2-135">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b8eb2-135">-Protocol</span></span>
<span data-ttu-id="b8eb2-136">인바운드 NAT 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="b8eb2-137">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8eb2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8eb2-138">CommonParameters</span></span>
<span data-ttu-id="b8eb2-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8eb2-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8eb2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8eb2-141">입력</span><span class="sxs-lookup"><span data-stu-id="b8eb2-141">INPUTS</span></span>

### <span data-ttu-id="b8eb2-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8eb2-142">PSLoadBalancer</span></span>
<span data-ttu-id="b8eb2-143">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb2-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b8eb2-144">출력</span><span class="sxs-lookup"><span data-stu-id="b8eb2-144">OUTPUTS</span></span>

### <span data-ttu-id="b8eb2-145">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8eb2-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b8eb2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b8eb2-146">NOTES</span></span>

## <span data-ttu-id="b8eb2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8eb2-147">RELATED LINKS</span></span>

[<span data-ttu-id="b8eb2-148">추가-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8eb2-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b8eb2-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8eb2-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b8eb2-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8eb2-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b8eb2-151">새로운 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8eb2-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b8eb2-152">제거-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8eb2-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


