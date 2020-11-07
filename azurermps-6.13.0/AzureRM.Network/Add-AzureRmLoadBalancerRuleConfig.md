---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711665"
---
# <span data-ttu-id="33e5f-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33e5f-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="33e5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="33e5f-103">부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33e5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33e5f-104">SYNTAX</span></span>

### <span data-ttu-id="33e5f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="33e5f-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e5f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="33e5f-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33e5f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="33e5f-107">DESCRIPTION</span></span>
<span data-ttu-id="33e5f-108">**Add-AzureRmLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="33e5f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="33e5f-109">EXAMPLES</span></span>

### <span data-ttu-id="33e5f-110">예제 1: 부하 분산 장치에 규칙 구성 추가</span><span class="sxs-lookup"><span data-stu-id="33e5f-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="33e5f-111">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="33e5f-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 **추가-AzureRmLoadBalancerRuleConfig** 에 전달 하 고 newrule 이라는 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="33e5f-113">변수</span><span class="sxs-lookup"><span data-stu-id="33e5f-113">PARAMETERS</span></span>

### <span data-ttu-id="33e5f-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="33e5f-114">-BackendAddressPool</span></span>
<span data-ttu-id="33e5f-115">부하 분산 장치 규칙 구성과 연결할 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e5f-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="33e5f-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="33e5f-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="33e5f-118">-BackendPort</span></span>
<span data-ttu-id="33e5f-119">부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e5f-120">-DefaultProfile</span></span>
<span data-ttu-id="33e5f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e5f-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="33e5f-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="33e5f-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="33e5f-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="33e5f-124">-EnableFloatingIP</span></span>
<span data-ttu-id="33e5f-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="33e5f-126">-EnableTcpReset</span></span>
<span data-ttu-id="33e5f-127">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="33e5f-128">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="33e5f-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="33e5f-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="33e5f-130">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="33e5f-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="33e5f-132">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="33e5f-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="33e5f-133">-FrontendPort</span></span>
<span data-ttu-id="33e5f-134">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="33e5f-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="33e5f-136">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="33e5f-137">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33e5f-137">-LoadBalancer</span></span>
<span data-ttu-id="33e5f-138">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="33e5f-139">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="33e5f-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="33e5f-140">-LoadDistribution</span></span>
<span data-ttu-id="33e5f-141">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="33e5f-142">-이름</span><span class="sxs-lookup"><span data-stu-id="33e5f-142">-Name</span></span>
<span data-ttu-id="33e5f-143">부하 분산 장치 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-144">-프로브</span><span class="sxs-lookup"><span data-stu-id="33e5f-144">-Probe</span></span>
<span data-ttu-id="33e5f-145">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e5f-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="33e5f-146">-ProbeId</span></span>
<span data-ttu-id="33e5f-147">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="33e5f-148">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="33e5f-148">-Protocol</span></span>
<span data-ttu-id="33e5f-149">부하 분산 장치 규칙에 맞는 프로토콜을 Specfies 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="33e5f-150">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="33e5f-151">-확인</span><span class="sxs-lookup"><span data-stu-id="33e5f-151">-Confirm</span></span>
<span data-ttu-id="33e5f-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33e5f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e5f-153">-WhatIf</span></span>
<span data-ttu-id="33e5f-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33e5f-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33e5f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e5f-156">CommonParameters</span></span>
<span data-ttu-id="33e5f-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e5f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e5f-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e5f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e5f-159">입력</span><span class="sxs-lookup"><span data-stu-id="33e5f-159">INPUTS</span></span>

### <span data-ttu-id="33e5f-160">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33e5f-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="33e5f-161">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33e5f-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="33e5f-162">출력</span><span class="sxs-lookup"><span data-stu-id="33e5f-162">OUTPUTS</span></span>

### <span data-ttu-id="33e5f-163">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33e5f-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="33e5f-164">상속자</span><span class="sxs-lookup"><span data-stu-id="33e5f-164">NOTES</span></span>

## <span data-ttu-id="33e5f-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33e5f-165">RELATED LINKS</span></span>

[<span data-ttu-id="33e5f-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33e5f-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="33e5f-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33e5f-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="33e5f-168">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33e5f-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="33e5f-169">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33e5f-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="33e5f-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33e5f-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


