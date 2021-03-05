---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50f3c3a02410adda37b26c88cd5196c4ae232f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971904"
---
# <span data-ttu-id="76321-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76321-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="76321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76321-102">SYNOPSIS</span></span>
<span data-ttu-id="76321-103">부하 저울에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76321-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="76321-104">구문</span><span class="sxs-lookup"><span data-stu-id="76321-104">SYNTAX</span></span>

### <span data-ttu-id="76321-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="76321-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76321-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76321-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76321-107">설명</span><span class="sxs-lookup"><span data-stu-id="76321-107">DESCRIPTION</span></span>
<span data-ttu-id="76321-108">**New-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure 부하 분산기에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76321-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="76321-109">예제</span><span class="sxs-lookup"><span data-stu-id="76321-109">EXAMPLES</span></span>

### <span data-ttu-id="76321-110">예제 1: 부하 저울에 대한 아웃바운드 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="76321-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="76321-111">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyPublicIP라는 공용 IP 주소를 만든 다음, 해당 ip $publicip 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="76321-112">두 번째 명령은 공용 IP 주소를 사용하여 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 $publicip 다음, $frontend 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="76321-113">세 번째 명령은 BackendAddressPool01이라는 백 엔드 주소 풀 구성을 만든 다음, 백 엔드 $backend 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="76321-114">네 번째 명령은 프런트 엔드 및 백 엔드 개체를 사용하여 MyOutboundRule이라는 아웃바운드 규칙 구성을 $frontend $backend.</span><span class="sxs-lookup"><span data-stu-id="76321-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="76321-115">*아웃바운드* 규칙 구성을 만드는 데 프로토콜, *FrontendIPConfiguration* 및 *BackendAddressPool* 매개 변수가 모두 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="76321-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="76321-116">Example 2</span></span>

<span data-ttu-id="76321-117">부하 저울에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76321-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="76321-118">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="76321-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="76321-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="76321-119">PARAMETERS</span></span>

### <span data-ttu-id="76321-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="76321-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="76321-121">NAT에 사용할 아웃바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="76321-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76321-122">-BackendAddressPool</span></span>
<span data-ttu-id="76321-123">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="76321-124">아웃바운드 트래픽은 백end IPS의 IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="76321-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76321-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="76321-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="76321-126">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="76321-127">아웃바운드 트래픽은 백end IPS의 IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="76321-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76321-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76321-128">-DefaultProfile</span></span>
<span data-ttu-id="76321-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76321-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="76321-130">-EnableTcpReset</span></span>
<span data-ttu-id="76321-131">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="76321-132">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76321-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="76321-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="76321-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="76321-134">부하 저울의 Frontend IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76321-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="76321-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="76321-136">TCP 유휴 연결의 시간 제한</span><span class="sxs-lookup"><span data-stu-id="76321-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="76321-137">-Name</span><span class="sxs-lookup"><span data-stu-id="76321-137">-Name</span></span>
<span data-ttu-id="76321-138">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76321-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="76321-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="76321-139">-Protocol</span></span>
<span data-ttu-id="76321-140">프로토콜 - TCP, UDP 또는 모두</span><span class="sxs-lookup"><span data-stu-id="76321-140">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76321-141">-확인</span><span class="sxs-lookup"><span data-stu-id="76321-141">-Confirm</span></span>
<span data-ttu-id="76321-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76321-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76321-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76321-143">-WhatIf</span></span>
<span data-ttu-id="76321-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="76321-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76321-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76321-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76321-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76321-146">CommonParameters</span></span>
<span data-ttu-id="76321-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76321-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76321-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76321-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76321-149">입력</span><span class="sxs-lookup"><span data-stu-id="76321-149">INPUTS</span></span>

### <span data-ttu-id="76321-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="76321-150">System.Int32</span></span>

### <span data-ttu-id="76321-151">System.String</span><span class="sxs-lookup"><span data-stu-id="76321-151">System.String</span></span>

### <span data-ttu-id="76321-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="76321-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="76321-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76321-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="76321-154">출력</span><span class="sxs-lookup"><span data-stu-id="76321-154">OUTPUTS</span></span>

### <span data-ttu-id="76321-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="76321-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="76321-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76321-156">NOTES</span></span>

## <span data-ttu-id="76321-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76321-157">RELATED LINKS</span></span>

[<span data-ttu-id="76321-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76321-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76321-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76321-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76321-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76321-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76321-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76321-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
