---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 10539a09c8849f1afd5cd3c5bd9e249929577342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963899"
---
# <span data-ttu-id="e8a12-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e8a12-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e8a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a12-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a12-103">부하 저울에 대한 인바운드 NAT 풀 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e8a12-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8a12-104">SYNTAX</span></span>

### <span data-ttu-id="e8a12-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8a12-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8a12-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8a12-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8a12-107">설명</span><span class="sxs-lookup"><span data-stu-id="e8a12-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a12-108">**Set-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산기에 대한 인바운드 NAT 풀 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e8a12-109">예제</span><span class="sxs-lookup"><span data-stu-id="e8a12-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a12-110">예제 1: 설정</span><span class="sxs-lookup"><span data-stu-id="e8a12-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="e8a12-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8a12-111">PARAMETERS</span></span>

### <span data-ttu-id="e8a12-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e8a12-112">-BackendPort</span></span>
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

### <span data-ttu-id="e8a12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a12-113">-DefaultProfile</span></span>
<span data-ttu-id="e8a12-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a12-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e8a12-115">-EnableFloatingIP</span></span>
<span data-ttu-id="e8a12-116">AlwaysOn 가용성 그룹을 구성하는 데 필요한 부동 IP 기능에 SQL 엔드포인트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="e8a12-117">이 설정은 서버의 SQL AlwaysOn 가용성 그룹을 사용할 SQL 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="e8a12-118">엔드포인트를 만든 후 이 설정을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="e8a12-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e8a12-119">-EnableTcpReset</span></span>
<span data-ttu-id="e8a12-120">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료에서 양방향 TCP 재설정을 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="e8a12-121">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e8a12-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8a12-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="e8a12-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e8a12-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="e8a12-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="e8a12-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="e8a12-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="e8a12-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="e8a12-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e8a12-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e8a12-127">TCP 유휴 연결의 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="e8a12-128">값은 4분에서 30분 사이로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="e8a12-129">기본값은 4분입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-129">The default value is 4 minutes.</span></span> <span data-ttu-id="e8a12-130">이 요소는 프로토콜이 TCP로 설정되어 있는 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e8a12-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e8a12-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="e8a12-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e8a12-132">-Name</span></span>
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

### <span data-ttu-id="e8a12-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e8a12-133">-Protocol</span></span>
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

### <span data-ttu-id="e8a12-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e8a12-134">-Confirm</span></span>
<span data-ttu-id="e8a12-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a12-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a12-136">-WhatIf</span></span>
<span data-ttu-id="e8a12-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8a12-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a12-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a12-139">CommonParameters</span></span>
<span data-ttu-id="e8a12-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a12-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a12-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8a12-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a12-142">입력</span><span class="sxs-lookup"><span data-stu-id="e8a12-142">INPUTS</span></span>

### <span data-ttu-id="e8a12-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e8a12-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e8a12-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e8a12-144">System.String</span></span>

### <span data-ttu-id="e8a12-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e8a12-145">System.Int32</span></span>

### <span data-ttu-id="e8a12-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8a12-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e8a12-147">출력</span><span class="sxs-lookup"><span data-stu-id="e8a12-147">OUTPUTS</span></span>

### <span data-ttu-id="e8a12-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e8a12-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e8a12-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8a12-149">NOTES</span></span>

## <span data-ttu-id="e8a12-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8a12-150">RELATED LINKS</span></span>

[<span data-ttu-id="e8a12-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e8a12-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e8a12-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e8a12-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e8a12-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e8a12-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e8a12-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e8a12-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
