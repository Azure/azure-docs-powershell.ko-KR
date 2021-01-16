---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491036"
---
# <span data-ttu-id="a48f9-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a48f9-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="a48f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a48f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a48f9-103">부하 균형 조정에 대한 인바운드 NAT 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="a48f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a48f9-104">SYNTAX</span></span>

### <span data-ttu-id="a48f9-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a48f9-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a48f9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a48f9-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a48f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="a48f9-107">DESCRIPTION</span></span>
<span data-ttu-id="a48f9-108">**New-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산에 대한 인바운드 NAT 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="a48f9-109">예제</span><span class="sxs-lookup"><span data-stu-id="a48f9-109">EXAMPLES</span></span>

### <span data-ttu-id="a48f9-110">예제 1: 새로 고안</span><span class="sxs-lookup"><span data-stu-id="a48f9-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="a48f9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a48f9-111">PARAMETERS</span></span>

### <span data-ttu-id="a48f9-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a48f9-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48f9-113">-DefaultProfile</span></span>
<span data-ttu-id="a48f9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a48f9-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a48f9-115">-EnableFloatingIP</span></span>
<span data-ttu-id="a48f9-116">AlwaysOn 가용성 그룹을 구성하는 데 필요한 부동 IP 기능에 대해 SQL 엔드포인트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="a48f9-117">이 설정은 서버의 SQL AlwaysOn 가용성 그룹을 사용하는 SQL 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="a48f9-118">이 설정은 엔드포인트를 만든 후에 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="a48f9-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a48f9-119">-EnableTcpReset</span></span>
<span data-ttu-id="a48f9-120">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a48f9-121">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a48f9-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a48f9-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="a48f9-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a48f9-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="a48f9-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="a48f9-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48f9-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="a48f9-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48f9-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a48f9-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a48f9-127">TCP 유휴 연결에 대한 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="a48f9-128">이 값은 4분에서 30분 사이로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="a48f9-129">기본값은 4분입니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-129">The default value is 4 minutes.</span></span> <span data-ttu-id="a48f9-130">이 요소는 프로토콜이 TCP로 설정된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a48f9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a48f9-131">-Name</span></span>
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

### <span data-ttu-id="a48f9-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a48f9-132">-Protocol</span></span>
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

### <span data-ttu-id="a48f9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a48f9-133">-Confirm</span></span>
<span data-ttu-id="a48f9-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a48f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a48f9-135">-WhatIf</span></span>
<span data-ttu-id="a48f9-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a48f9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a48f9-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a48f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48f9-138">CommonParameters</span></span>
<span data-ttu-id="a48f9-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a48f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48f9-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a48f9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48f9-141">입력</span><span class="sxs-lookup"><span data-stu-id="a48f9-141">INPUTS</span></span>

### <span data-ttu-id="a48f9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a48f9-142">System.String</span></span>

### <span data-ttu-id="a48f9-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a48f9-143">System.Int32</span></span>

### <span data-ttu-id="a48f9-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a48f9-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a48f9-145">출력</span><span class="sxs-lookup"><span data-stu-id="a48f9-145">OUTPUTS</span></span>

### <span data-ttu-id="a48f9-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="a48f9-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="a48f9-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a48f9-147">NOTES</span></span>

## <span data-ttu-id="a48f9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a48f9-148">RELATED LINKS</span></span>

[<span data-ttu-id="a48f9-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a48f9-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a48f9-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a48f9-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a48f9-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a48f9-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a48f9-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a48f9-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
