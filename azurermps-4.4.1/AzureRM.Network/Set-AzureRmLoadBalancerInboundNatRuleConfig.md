---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529285"
---
# <span data-ttu-id="d1ee6-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1ee6-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d1ee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ee6-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ee6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1ee6-104">SYNTAX</span></span>

### <span data-ttu-id="d1ee6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1ee6-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ee6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d1ee6-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ee6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ee6-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (network address translation) 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d1ee6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d1ee6-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ee6-110">예제 1: 부하 분산 장치에서 인바운드 NAT 규칙 구성 수정</span><span class="sxs-lookup"><span data-stu-id="d1ee6-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="d1ee6-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="d1ee6-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzureRmLoadBalancerInboundNatRuleConfig에 전달 하 여 인바운드 NAT 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="d1ee6-113">세 번째 명령은 인바운드 NAT 규칙 구성을 저장 하 고 업데이트 하는 부하 분산을 **설정-AzureRmLoadBalancerInboundNatRuleConfig** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="d1ee6-114">이전 명령에서 사용 하도록 설정 된 부동 IP를 사용 하지 않고 규칙 구성이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="d1ee6-115">변수</span><span class="sxs-lookup"><span data-stu-id="d1ee6-115">PARAMETERS</span></span>

### <span data-ttu-id="d1ee6-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d1ee6-116">-BackendPort</span></span>
<span data-ttu-id="d1ee6-117">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="d1ee6-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d1ee6-118">-EnableFloatingIP</span></span>
<span data-ttu-id="d1ee6-119">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d1ee6-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ee6-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d1ee6-121">인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d1ee6-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d1ee6-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d1ee6-123">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-123">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d1ee6-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1ee6-124">-FrontendPort</span></span>
<span data-ttu-id="d1ee6-125">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="d1ee6-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d1ee6-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d1ee6-127">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d1ee6-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1ee6-128">-LoadBalancer</span></span>
<span data-ttu-id="d1ee6-129">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-129">Specifies a load balancer.</span></span>
<span data-ttu-id="d1ee6-130">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1ee6-131">-이름</span><span class="sxs-lookup"><span data-stu-id="d1ee6-131">-Name</span></span>
<span data-ttu-id="d1ee6-132">인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d1ee6-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="d1ee6-133">-Protocol</span></span>
<span data-ttu-id="d1ee6-134">인바운드 NAT 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="d1ee6-135">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d1ee6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ee6-136">-DefaultProfile</span></span>
<span data-ttu-id="d1ee6-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ee6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ee6-138">CommonParameters</span></span>
<span data-ttu-id="d1ee6-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ee6-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ee6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ee6-141">입력</span><span class="sxs-lookup"><span data-stu-id="d1ee6-141">INPUTS</span></span>

### <span data-ttu-id="d1ee6-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1ee6-142">PSLoadBalancer</span></span>
<span data-ttu-id="d1ee6-143">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ee6-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d1ee6-144">출력</span><span class="sxs-lookup"><span data-stu-id="d1ee6-144">OUTPUTS</span></span>

### <span data-ttu-id="d1ee6-145">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1ee6-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d1ee6-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d1ee6-146">NOTES</span></span>

## <span data-ttu-id="d1ee6-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1ee6-147">RELATED LINKS</span></span>

[<span data-ttu-id="d1ee6-148">추가-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1ee6-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d1ee6-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1ee6-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d1ee6-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1ee6-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d1ee6-151">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1ee6-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d1ee6-152">제거-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1ee6-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

