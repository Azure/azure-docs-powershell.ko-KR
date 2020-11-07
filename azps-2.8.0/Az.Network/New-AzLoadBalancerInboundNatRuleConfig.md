---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871406"
---
# <span data-ttu-id="c13a3-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c13a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c13a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c13a3-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c13a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c13a3-104">SYNTAX</span></span>

### <span data-ttu-id="c13a3-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="c13a3-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c13a3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c13a3-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c13a3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c13a3-107">DESCRIPTION</span></span>
<span data-ttu-id="c13a3-108">**AzLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (inbound network address translation) 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c13a3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c13a3-109">EXAMPLES</span></span>

### <span data-ttu-id="c13a3-110">예제 1: 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="c13a3-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="c13a3-111">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 이라는 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="c13a3-112">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="c13a3-113">세 번째 명령은 $frontend에서 프런트 엔드 개체를 사용 하 여 MyInboundNatRule 라는 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="c13a3-114">TCP 프로토콜이 지정 되 고 프런트 엔드 포트는 3389 이며,이 경우 백 엔드 포트와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="c13a3-115">*FrontendIpConfiguration* , *Protocol* , *FrontendPort* 및 *BackendPort* 매개 변수는 모두 인바운드 NAT 규칙 구성을 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="c13a3-116">변수</span><span class="sxs-lookup"><span data-stu-id="c13a3-116">PARAMETERS</span></span>

### <span data-ttu-id="c13a3-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c13a3-117">-BackendPort</span></span>
<span data-ttu-id="c13a3-118">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="c13a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13a3-119">-DefaultProfile</span></span>
<span data-ttu-id="c13a3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c13a3-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c13a3-121">-EnableFloatingIP</span></span>
<span data-ttu-id="c13a3-122">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c13a3-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c13a3-123">-EnableTcpReset</span></span>
<span data-ttu-id="c13a3-124">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c13a3-125">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c13a3-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c13a3-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c13a3-127">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c13a3-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c13a3-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c13a3-129">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c13a3-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c13a3-130">-FrontendPort</span></span>
<span data-ttu-id="c13a3-131">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c13a3-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c13a3-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c13a3-133">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c13a3-134">-이름</span><span class="sxs-lookup"><span data-stu-id="c13a3-134">-Name</span></span>
<span data-ttu-id="c13a3-135">이 cmdlet이 만드는 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c13a3-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="c13a3-136">-Protocol</span></span>
<span data-ttu-id="c13a3-137">프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-137">Specifies a protocol.</span></span>
<span data-ttu-id="c13a3-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c13a3-139">Net.tcp</span><span class="sxs-lookup"><span data-stu-id="c13a3-139">Tcp</span></span>
- <span data-ttu-id="c13a3-140">Udp</span><span class="sxs-lookup"><span data-stu-id="c13a3-140">Udp</span></span>

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

### <span data-ttu-id="c13a3-141">-확인</span><span class="sxs-lookup"><span data-stu-id="c13a3-141">-Confirm</span></span>
<span data-ttu-id="c13a3-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c13a3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c13a3-143">-WhatIf</span></span>
<span data-ttu-id="c13a3-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c13a3-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c13a3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13a3-146">CommonParameters</span></span>
<span data-ttu-id="c13a3-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c13a3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13a3-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c13a3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13a3-149">입력</span><span class="sxs-lookup"><span data-stu-id="c13a3-149">INPUTS</span></span>

### <span data-ttu-id="c13a3-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c13a3-150">System.String</span></span>

### <span data-ttu-id="c13a3-151">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="c13a3-151">System.Int32</span></span>

### <span data-ttu-id="c13a3-152">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c13a3-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c13a3-153">출력</span><span class="sxs-lookup"><span data-stu-id="c13a3-153">OUTPUTS</span></span>

### <span data-ttu-id="c13a3-154">PSInboundNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c13a3-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="c13a3-155">상속자</span><span class="sxs-lookup"><span data-stu-id="c13a3-155">NOTES</span></span>

## <span data-ttu-id="c13a3-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c13a3-156">RELATED LINKS</span></span>

[<span data-ttu-id="c13a3-157">추가-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c13a3-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c13a3-159">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c13a3-160">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c13a3-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c13a3-161">제거-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c13a3-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c13a3-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


