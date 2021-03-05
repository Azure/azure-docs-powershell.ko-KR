---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a6bec76345df188ca58e8b790637e35606de1f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001099"
---
# <span data-ttu-id="ea390-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ea390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea390-102">SYNOPSIS</span></span>
<span data-ttu-id="ea390-103">부하 저울에 대한 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ea390-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea390-104">SYNTAX</span></span>

### <span data-ttu-id="ea390-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea390-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea390-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea390-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea390-107">설명</span><span class="sxs-lookup"><span data-stu-id="ea390-107">DESCRIPTION</span></span>
<span data-ttu-id="ea390-108">**New-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure 부하 분산기에 대한 NAT(인바운드 네트워크 주소 변환) 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ea390-109">예제</span><span class="sxs-lookup"><span data-stu-id="ea390-109">EXAMPLES</span></span>

### <span data-ttu-id="ea390-110">예제 1: 부하 저울에 대한 인바운드 NAT 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="ea390-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="ea390-111">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyPublicIP라는 공용 IP 주소를 만든 다음, 해당 ip $publicip 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="ea390-112">두 번째 명령은 공용 IP 주소를 사용하여 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 $publicip 다음, $frontend 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="ea390-113">세 번째 명령은 프런트 엔드 개체를 사용하여 MyInboundNatRule이라는 인바운드 NAT 규칙 구성을 $frontend.</span><span class="sxs-lookup"><span data-stu-id="ea390-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="ea390-114">TCP 프로토콜이 지정되어 있으며 프런트 엔드 포트는 3389로 이 경우 백 엔드 포트와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="ea390-115">*FrontendIpConfiguration,* *Protocol,* *FrontendPort* 및 *BackendPort* 매개 변수는 모두 인바운드 NAT 규칙 구성을 만드는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="ea390-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea390-116">PARAMETERS</span></span>

### <span data-ttu-id="ea390-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ea390-117">-BackendPort</span></span>
<span data-ttu-id="ea390-118">이 규칙 구성과 일치하는 트래픽에 대한 백end 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ea390-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea390-119">-DefaultProfile</span></span>
<span data-ttu-id="ea390-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea390-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ea390-121">-EnableFloatingIP</span></span>
<span data-ttu-id="ea390-122">이 cmdlet은 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ea390-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ea390-123">-EnableTcpReset</span></span>
<span data-ttu-id="ea390-124">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ea390-125">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ea390-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea390-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ea390-127">부하 조정기 규칙 구성과 연결하기 위한 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ea390-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ea390-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ea390-129">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ea390-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ea390-130">-FrontendPort</span></span>
<span data-ttu-id="ea390-131">부하 균형기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ea390-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ea390-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ea390-133">시간의 길이(분)를 지정합니다. 이 기간은 부하 균형 조정기에서 대화 상태가 유지되는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ea390-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ea390-134">-Name</span></span>
<span data-ttu-id="ea390-135">이 cmdlet에서 만드는 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ea390-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ea390-136">-Protocol</span></span>
<span data-ttu-id="ea390-137">프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-137">Specifies a protocol.</span></span>
<span data-ttu-id="ea390-138">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea390-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="ea390-139">Tcp</span></span>
- <span data-ttu-id="ea390-140">Udp</span><span class="sxs-lookup"><span data-stu-id="ea390-140">Udp</span></span>

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

### <span data-ttu-id="ea390-141">-확인</span><span class="sxs-lookup"><span data-stu-id="ea390-141">-Confirm</span></span>
<span data-ttu-id="ea390-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea390-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea390-143">-WhatIf</span></span>
<span data-ttu-id="ea390-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea390-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea390-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea390-146">CommonParameters</span></span>
<span data-ttu-id="ea390-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea390-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea390-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea390-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea390-149">입력</span><span class="sxs-lookup"><span data-stu-id="ea390-149">INPUTS</span></span>

### <span data-ttu-id="ea390-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ea390-150">System.String</span></span>

### <span data-ttu-id="ea390-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ea390-151">System.Int32</span></span>

### <span data-ttu-id="ea390-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea390-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ea390-153">출력</span><span class="sxs-lookup"><span data-stu-id="ea390-153">OUTPUTS</span></span>

### <span data-ttu-id="ea390-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ea390-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ea390-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea390-155">NOTES</span></span>

## <span data-ttu-id="ea390-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea390-156">RELATED LINKS</span></span>

[<span data-ttu-id="ea390-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ea390-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ea390-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ea390-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea390-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ea390-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ea390-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea390-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


