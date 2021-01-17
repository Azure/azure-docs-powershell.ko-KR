---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362475"
---
# <span data-ttu-id="7f33a-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f33a-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="7f33a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f33a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f33a-103">부하 균형 조정에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7f33a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f33a-104">SYNTAX</span></span>

### <span data-ttu-id="7f33a-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f33a-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f33a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f33a-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f33a-107">설명</span><span class="sxs-lookup"><span data-stu-id="7f33a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f33a-108">**New-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure Load Balancer에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7f33a-109">예제</span><span class="sxs-lookup"><span data-stu-id="7f33a-109">EXAMPLES</span></span>

### <span data-ttu-id="7f33a-110">예제 1: 부하 균형 조정에 대한 아웃바운드 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="7f33a-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="7f33a-111">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyPublicIP라는 공용 IP 주소를 만든 다음, $publicip 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="7f33a-112">두 번째 명령은 $publicip 공용 IP 주소를 사용하여 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="7f33a-113">세 번째 명령은 BackendAddressPool01이라는 백 엔드 주소 풀 구성을 만든 다음 $backend 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="7f33a-114">네 번째 명령은 프런트 엔드 및 백 엔드 개체를 사용하여 MyOutboundRule이라는 아웃바운드 규칙 구성을 $frontend $backend.</span><span class="sxs-lookup"><span data-stu-id="7f33a-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="7f33a-115">*프로토콜,* *FrontendIPConfiguration* 및 *BackendAddressPool* 매개 변수는 모두 아웃바운드 규칙 구성을 만드는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="7f33a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="7f33a-116">Example 2</span></span>

<span data-ttu-id="7f33a-117">부하 균형 조정에 대한 아웃바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="7f33a-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="7f33a-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="7f33a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f33a-119">PARAMETERS</span></span>

### <span data-ttu-id="7f33a-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="7f33a-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="7f33a-121">NAT에 사용할 아웃바운드 포트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="7f33a-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f33a-122">-BackendAddressPool</span></span>
<span data-ttu-id="7f33a-123">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="7f33a-124">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="7f33a-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7f33a-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="7f33a-126">DIP 풀에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="7f33a-127">아웃바운드 트래픽은 백end IP에서 임의로 부하가 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="7f33a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f33a-128">-DefaultProfile</span></span>
<span data-ttu-id="7f33a-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f33a-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7f33a-130">-EnableTcpReset</span></span>
<span data-ttu-id="7f33a-131">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="7f33a-132">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7f33a-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f33a-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7f33a-134">부하 균형 조정의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-134">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="7f33a-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7f33a-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7f33a-136">TCP 유휴 연결에 대한 시간 제한</span><span class="sxs-lookup"><span data-stu-id="7f33a-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="7f33a-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7f33a-137">-Name</span></span>
<span data-ttu-id="7f33a-138">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="7f33a-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7f33a-139">-Protocol</span></span>
<span data-ttu-id="7f33a-140">프로토콜 - TCP, UDP 또는 모두</span><span class="sxs-lookup"><span data-stu-id="7f33a-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="7f33a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f33a-141">-Confirm</span></span>
<span data-ttu-id="7f33a-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f33a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f33a-143">-WhatIf</span></span>
<span data-ttu-id="7f33a-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7f33a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f33a-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f33a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f33a-146">CommonParameters</span></span>
<span data-ttu-id="7f33a-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f33a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f33a-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7f33a-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f33a-149">입력</span><span class="sxs-lookup"><span data-stu-id="7f33a-149">INPUTS</span></span>

### <span data-ttu-id="7f33a-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7f33a-150">System.Int32</span></span>

### <span data-ttu-id="7f33a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7f33a-151">System.String</span></span>

### <span data-ttu-id="7f33a-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="7f33a-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="7f33a-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f33a-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="7f33a-154">출력</span><span class="sxs-lookup"><span data-stu-id="7f33a-154">OUTPUTS</span></span>

### <span data-ttu-id="7f33a-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="7f33a-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="7f33a-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f33a-156">NOTES</span></span>

## <span data-ttu-id="7f33a-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f33a-157">RELATED LINKS</span></span>

[<span data-ttu-id="7f33a-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f33a-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7f33a-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f33a-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7f33a-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f33a-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7f33a-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f33a-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
