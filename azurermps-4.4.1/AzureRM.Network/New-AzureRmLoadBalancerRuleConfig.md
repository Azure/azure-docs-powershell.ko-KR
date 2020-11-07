---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: fad24c7cb9b6146ecb5fa1f0c2c21e1f2c0adbf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703685"
---
# <span data-ttu-id="39dba-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39dba-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="39dba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39dba-102">SYNOPSIS</span></span>
<span data-ttu-id="39dba-103">부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39dba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39dba-104">SYNTAX</span></span>

### <span data-ttu-id="39dba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39dba-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39dba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="39dba-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39dba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39dba-107">DESCRIPTION</span></span>
<span data-ttu-id="39dba-108">**AzureRmLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="39dba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39dba-109">EXAMPLES</span></span>

### <span data-ttu-id="39dba-110">1: Azure 부하 분산 장치에 대 한 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="39dba-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="39dba-111">처음 세 개의 명령은 공용 IP, 프론트 엔드, 그리고 위의 명령에서 규칙 구성에 대 한 프로브를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="39dba-112">위의 명령은 특정 사양을 사용 하 여 MyLBrule 이라는 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="39dba-113">변수</span><span class="sxs-lookup"><span data-stu-id="39dba-113">PARAMETERS</span></span>

### <span data-ttu-id="39dba-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39dba-114">-BackendAddressPool</span></span>
<span data-ttu-id="39dba-115">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="39dba-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="39dba-117">부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="39dba-118">-BackendPort</span></span>
<span data-ttu-id="39dba-119">이 부하 분산 장치 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-120">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="39dba-120">-DisableOutboundSNAT</span></span>
<span data-ttu-id="39dba-121">부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-121">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="39dba-122">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="39dba-122">-EnableFloatingIP</span></span>
<span data-ttu-id="39dba-123">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-123">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="39dba-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39dba-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="39dba-125">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-125">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39dba-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="39dba-127">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-127">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="39dba-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="39dba-128">-FrontendPort</span></span>
<span data-ttu-id="39dba-129">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-129">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="39dba-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="39dba-131">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="39dba-132">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="39dba-132">-LoadDistribution</span></span>
<span data-ttu-id="39dba-133">부하 분포를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-133">Specifies a load distribution.</span></span>
<span data-ttu-id="39dba-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39dba-135">기본값</span><span class="sxs-lookup"><span data-stu-id="39dba-135">Default</span></span>
- <span data-ttu-id="39dba-136">SourceIP</span><span class="sxs-lookup"><span data-stu-id="39dba-136">SourceIP</span></span>
- <span data-ttu-id="39dba-137">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="39dba-137">SourceIPProtocol</span></span>

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

### <span data-ttu-id="39dba-138">-이름</span><span class="sxs-lookup"><span data-stu-id="39dba-138">-Name</span></span>
<span data-ttu-id="39dba-139">이 cmdlet이 만드는 부하 분산 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-139">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="39dba-140">-프로브</span><span class="sxs-lookup"><span data-stu-id="39dba-140">-Probe</span></span>
<span data-ttu-id="39dba-141">부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-141">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-142">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="39dba-142">-ProbeId</span></span>
<span data-ttu-id="39dba-143">부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-143">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39dba-144">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="39dba-144">-Protocol</span></span>
<span data-ttu-id="39dba-145">부하 분산 장치 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-145">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="39dba-146">이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-146">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="39dba-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dba-147">-DefaultProfile</span></span>
<span data-ttu-id="39dba-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39dba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dba-149">CommonParameters</span></span>
<span data-ttu-id="39dba-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dba-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39dba-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dba-152">입력</span><span class="sxs-lookup"><span data-stu-id="39dba-152">INPUTS</span></span>

## <span data-ttu-id="39dba-153">출력</span><span class="sxs-lookup"><span data-stu-id="39dba-153">OUTPUTS</span></span>

### <span data-ttu-id="39dba-154">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="39dba-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="39dba-155">상속자</span><span class="sxs-lookup"><span data-stu-id="39dba-155">NOTES</span></span>

## <span data-ttu-id="39dba-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39dba-156">RELATED LINKS</span></span>

[<span data-ttu-id="39dba-157">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39dba-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="39dba-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39dba-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="39dba-159">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39dba-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="39dba-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39dba-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


