---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875426"
---
# <span data-ttu-id="6e0cf-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e0cf-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6e0cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0cf-103">부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6e0cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e0cf-104">SYNTAX</span></span>

### <span data-ttu-id="6e0cf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e0cf-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e0cf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e0cf-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e0cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e0cf-107">DESCRIPTION</span></span>
<span data-ttu-id="6e0cf-108">**AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6e0cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e0cf-109">EXAMPLES</span></span>

### <span data-ttu-id="6e0cf-110">1: Azure 부하 분산 장치에 대 한 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="6e0cf-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="6e0cf-111">처음 세 개의 명령은 공용 IP, 프론트 엔드, 그리고 위의 명령에서 규칙 구성에 대 한 프로브를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="6e0cf-112">위의 명령은 특정 사양을 사용 하 여 MyLBrule 이라는 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="6e0cf-113">변수</span><span class="sxs-lookup"><span data-stu-id="6e0cf-113">PARAMETERS</span></span>

### <span data-ttu-id="6e0cf-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e0cf-114">-BackendAddressPool</span></span>
<span data-ttu-id="6e0cf-115">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6e0cf-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="6e0cf-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6e0cf-118">-BackendPort</span></span>
<span data-ttu-id="6e0cf-119">이 부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0cf-120">-DefaultProfile</span></span>
<span data-ttu-id="6e0cf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e0cf-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6e0cf-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6e0cf-123">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6e0cf-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6e0cf-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6e0cf-125">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e0cf-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6e0cf-127">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6e0cf-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6e0cf-129">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6e0cf-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0cf-130">-FrontendPort</span></span>
<span data-ttu-id="6e0cf-131">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6e0cf-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6e0cf-133">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6e0cf-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6e0cf-134">-LoadDistribution</span></span>
<span data-ttu-id="6e0cf-135">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-135">Specifies a load distribution.</span></span>
<span data-ttu-id="6e0cf-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e0cf-137">기본값</span><span class="sxs-lookup"><span data-stu-id="6e0cf-137">Default</span></span>
- <span data-ttu-id="6e0cf-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="6e0cf-138">SourceIP</span></span>
- <span data-ttu-id="6e0cf-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="6e0cf-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="6e0cf-140">-이름</span><span class="sxs-lookup"><span data-stu-id="6e0cf-140">-Name</span></span>
<span data-ttu-id="6e0cf-141">이 cmdlet이 만드는 부하 분산 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6e0cf-142">-프로브</span><span class="sxs-lookup"><span data-stu-id="6e0cf-142">-Probe</span></span>
<span data-ttu-id="6e0cf-143">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6e0cf-144">-ProbeId</span></span>
<span data-ttu-id="6e0cf-145">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6e0cf-146">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="6e0cf-146">-Protocol</span></span>
<span data-ttu-id="6e0cf-147">부하 분산 장치 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="6e0cf-148">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6e0cf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0cf-149">CommonParameters</span></span>
<span data-ttu-id="6e0cf-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0cf-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e0cf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0cf-152">입력</span><span class="sxs-lookup"><span data-stu-id="6e0cf-152">INPUTS</span></span>

## <span data-ttu-id="6e0cf-153">출력</span><span class="sxs-lookup"><span data-stu-id="6e0cf-153">OUTPUTS</span></span>

### <span data-ttu-id="6e0cf-154">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6e0cf-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="6e0cf-155">상속자</span><span class="sxs-lookup"><span data-stu-id="6e0cf-155">NOTES</span></span>

## <span data-ttu-id="6e0cf-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e0cf-156">RELATED LINKS</span></span>

[<span data-ttu-id="6e0cf-157">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e0cf-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6e0cf-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e0cf-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6e0cf-159">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e0cf-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6e0cf-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e0cf-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


