---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 65861e86f0852d0002a7c4aa6f2c7f925eabf5bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883030"
---
# <span data-ttu-id="d26ff-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d26ff-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d26ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d26ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d26ff-103">부하 분산 장치에 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d26ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d26ff-104">SYNTAX</span></span>

### <span data-ttu-id="d26ff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d26ff-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d26ff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d26ff-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d26ff-107">DESCRIPTION</span></span>
<span data-ttu-id="d26ff-108">**Add-AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 인바운드 NAT (network address translation) 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d26ff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d26ff-109">EXAMPLES</span></span>

### <span data-ttu-id="d26ff-110">예제 1: 부하 분산 장치에 인바운드 NAT 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="d26ff-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="d26ff-111">첫 번째 명령은 MyloadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="d26ff-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzureRmLoadBalancerInboundNatRuleConfig** 에 전달 하 고,이는 인바운드 NAT 규칙 구성을 부하 분산 장치에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d26ff-113">변수</span><span class="sxs-lookup"><span data-stu-id="d26ff-113">PARAMETERS</span></span>

### <span data-ttu-id="d26ff-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d26ff-114">-BackendPort</span></span>
<span data-ttu-id="d26ff-115">규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d26ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26ff-116">-DefaultProfile</span></span>
<span data-ttu-id="d26ff-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26ff-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d26ff-118">-EnableFloatingIP</span></span>
<span data-ttu-id="d26ff-119">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d26ff-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d26ff-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d26ff-121">인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d26ff-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d26ff-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d26ff-123">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d26ff-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d26ff-124">-FrontendPort</span></span>
<span data-ttu-id="d26ff-125">규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d26ff-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d26ff-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d26ff-127">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d26ff-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d26ff-128">-LoadBalancer</span></span>
<span data-ttu-id="d26ff-129">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d26ff-130">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d26ff-131">-이름</span><span class="sxs-lookup"><span data-stu-id="d26ff-131">-Name</span></span>
<span data-ttu-id="d26ff-132">추가할 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="d26ff-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="d26ff-133">-Protocol</span></span>
<span data-ttu-id="d26ff-134">인바운드 NAT 규칙에 맞는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="d26ff-135">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d26ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26ff-136">CommonParameters</span></span>
<span data-ttu-id="d26ff-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26ff-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d26ff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26ff-139">입력</span><span class="sxs-lookup"><span data-stu-id="d26ff-139">INPUTS</span></span>

### <span data-ttu-id="d26ff-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d26ff-140">PSLoadBalancer</span></span>
<span data-ttu-id="d26ff-141">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d26ff-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d26ff-142">출력</span><span class="sxs-lookup"><span data-stu-id="d26ff-142">OUTPUTS</span></span>

### <span data-ttu-id="d26ff-143">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d26ff-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d26ff-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d26ff-144">NOTES</span></span>

## <span data-ttu-id="d26ff-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d26ff-145">RELATED LINKS</span></span>

[<span data-ttu-id="d26ff-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d26ff-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d26ff-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d26ff-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d26ff-148">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d26ff-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d26ff-149">제거-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d26ff-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d26ff-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d26ff-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="d26ff-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d26ff-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


