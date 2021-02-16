---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179636"
---
# <span data-ttu-id="da48b-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="da48b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da48b-102">SYNOPSIS</span></span>
<span data-ttu-id="da48b-103">부하 균형 조정에 대한 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="da48b-104">구문</span><span class="sxs-lookup"><span data-stu-id="da48b-104">SYNTAX</span></span>

### <span data-ttu-id="da48b-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="da48b-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da48b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da48b-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da48b-107">설명</span><span class="sxs-lookup"><span data-stu-id="da48b-107">DESCRIPTION</span></span>
<span data-ttu-id="da48b-108">**New-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure Load Balancer에 대한 인바운드 NAT(네트워크 주소 변환) 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="da48b-109">예제</span><span class="sxs-lookup"><span data-stu-id="da48b-109">EXAMPLES</span></span>

### <span data-ttu-id="da48b-110">예제 1: 부하 균형 조정에 대한 인바운드 NAT 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="da48b-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="da48b-111">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyPublicIP라는 공용 IP 주소를 만든 다음, $publicip 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="da48b-112">두 번째 명령은 $publicip 공용 IP 주소를 사용하여 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="da48b-113">세 번째 명령은 명령의 프런트 엔드 개체를 사용하여 MyInboundNatRule이라는 인바운드 NAT 규칙 구성을 $frontend.</span><span class="sxs-lookup"><span data-stu-id="da48b-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="da48b-114">TCP 프로토콜이 지정되어 있으며 프런트 엔드 포트는 3389로, 이 경우 백 엔드 포트와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="da48b-115">*FrontendIpConfiguration,* *Protocol,* *FrontendPort* 및 *BackendPort* 매개 변수는 모두 인바운드 NAT 규칙 구성을 만드는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="da48b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da48b-116">PARAMETERS</span></span>

### <span data-ttu-id="da48b-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="da48b-117">-BackendPort</span></span>
<span data-ttu-id="da48b-118">이 규칙 구성과 일치하는 트래픽에 대한 백투인 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="da48b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da48b-119">-DefaultProfile</span></span>
<span data-ttu-id="da48b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da48b-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="da48b-121">-EnableFloatingIP</span></span>
<span data-ttu-id="da48b-122">이 cmdlet이 규칙 구성에 대해 부동 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="da48b-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="da48b-123">-EnableTcpReset</span></span>
<span data-ttu-id="da48b-124">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="da48b-125">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="da48b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="da48b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="da48b-127">부하 균형 조정기 규칙 구성과 연결될 프런트 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="da48b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="da48b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="da48b-129">프런트 엔드 IP 주소 구성에 대한 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="da48b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="da48b-130">-FrontendPort</span></span>
<span data-ttu-id="da48b-131">부하 균형 조정기 규칙 구성과 일치하는 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="da48b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="da48b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="da48b-133">부하 균형 조정기에서 대화 상태가 유지되는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="da48b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="da48b-134">-Name</span></span>
<span data-ttu-id="da48b-135">이 cmdlet에서 만드는 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da48b-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="da48b-136">-Protocol</span></span>
<span data-ttu-id="da48b-137">프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-137">Specifies a protocol.</span></span>
<span data-ttu-id="da48b-138">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="da48b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da48b-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="da48b-139">Tcp</span></span>
- <span data-ttu-id="da48b-140">Udp</span><span class="sxs-lookup"><span data-stu-id="da48b-140">Udp</span></span>

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

### <span data-ttu-id="da48b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da48b-141">-Confirm</span></span>
<span data-ttu-id="da48b-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da48b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da48b-143">-WhatIf</span></span>
<span data-ttu-id="da48b-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da48b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da48b-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da48b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da48b-146">CommonParameters</span></span>
<span data-ttu-id="da48b-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da48b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da48b-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="da48b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da48b-149">입력</span><span class="sxs-lookup"><span data-stu-id="da48b-149">INPUTS</span></span>

### <span data-ttu-id="da48b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="da48b-150">System.String</span></span>

### <span data-ttu-id="da48b-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="da48b-151">System.Int32</span></span>

### <span data-ttu-id="da48b-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="da48b-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="da48b-153">출력</span><span class="sxs-lookup"><span data-stu-id="da48b-153">OUTPUTS</span></span>

### <span data-ttu-id="da48b-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="da48b-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="da48b-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da48b-155">NOTES</span></span>

## <span data-ttu-id="da48b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da48b-156">RELATED LINKS</span></span>

[<span data-ttu-id="da48b-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="da48b-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="da48b-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da48b-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da48b-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="da48b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="da48b-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da48b-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


