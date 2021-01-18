---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496504"
---
# <span data-ttu-id="57bdb-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57bdb-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="57bdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="57bdb-103">부하 균형 조정에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="57bdb-104">구문</span><span class="sxs-lookup"><span data-stu-id="57bdb-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57bdb-105">설명</span><span class="sxs-lookup"><span data-stu-id="57bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="57bdb-106">**Set-AzLoadBalancerProbeConfig** cmdlet은 부하 분산에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="57bdb-107">예제</span><span class="sxs-lookup"><span data-stu-id="57bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="57bdb-108">예제 1: 부하 균형 조정기에서 프로브 구성 수정</span><span class="sxs-lookup"><span data-stu-id="57bdb-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="57bdb-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 변수를 구한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="57bdb-110">두 번째 명령은 파이프라인 연산자를 사용하여 새 프로브 구성을 추가하는 $slb Add-AzLoadBalancerProbeConfig에 부하 분산 기능을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="57bdb-111">세 번째 명령은 새 구성을 설정하는 **Set-AzLoadBalancerProbeConfig에** 부하 분산을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="57bdb-112">현재 cmdlet에 필요하기 때문에 이전 명령에 지정된 동일한 매개 변수 중 여러 개를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="57bdb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57bdb-113">PARAMETERS</span></span>

### <span data-ttu-id="57bdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bdb-114">-DefaultProfile</span></span>
<span data-ttu-id="57bdb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57bdb-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="57bdb-116">-IntervalInSeconds</span></span>
<span data-ttu-id="57bdb-117">부하가 균형 잡힌 서비스의 각 인스턴스에 대한 프로브 사이의 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="57bdb-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57bdb-118">-LoadBalancer</span></span>
<span data-ttu-id="57bdb-119">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-119">Specifies a load balancer.</span></span>
<span data-ttu-id="57bdb-120">이 cmdlet은 이 매개 변수가 지정하는 부하 균형 조정에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="57bdb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="57bdb-121">-Name</span></span>
<span data-ttu-id="57bdb-122">이 cmdlet이 설정하는 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="57bdb-123">-Port</span><span class="sxs-lookup"><span data-stu-id="57bdb-123">-Port</span></span>
<span data-ttu-id="57bdb-124">프로브가 부하가 균형 잡힌 서비스에 연결해야 하는 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="57bdb-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="57bdb-125">-ProbeCount</span></span>
<span data-ttu-id="57bdb-126">인스턴스가 비보안으로 간주될 인스턴스당 연속 오류 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="57bdb-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="57bdb-127">-Protocol</span></span>
<span data-ttu-id="57bdb-128">프로브에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="57bdb-129">이 매개 변수에 허용되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="57bdb-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="57bdb-130">-RequestPath</span></span>
<span data-ttu-id="57bdb-131">상태 확인을 위해 프로브할 부하가 균형 잡힌 서비스의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="57bdb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57bdb-132">-Confirm</span></span>
<span data-ttu-id="57bdb-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57bdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57bdb-134">-WhatIf</span></span>
<span data-ttu-id="57bdb-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57bdb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57bdb-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57bdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bdb-137">CommonParameters</span></span>
<span data-ttu-id="57bdb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57bdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bdb-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="57bdb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bdb-140">입력</span><span class="sxs-lookup"><span data-stu-id="57bdb-140">INPUTS</span></span>

### <span data-ttu-id="57bdb-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57bdb-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="57bdb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="57bdb-142">System.String</span></span>

### <span data-ttu-id="57bdb-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="57bdb-143">System.Int32</span></span>

## <span data-ttu-id="57bdb-144">출력</span><span class="sxs-lookup"><span data-stu-id="57bdb-144">OUTPUTS</span></span>

### <span data-ttu-id="57bdb-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57bdb-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="57bdb-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57bdb-146">NOTES</span></span>

## <span data-ttu-id="57bdb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57bdb-147">RELATED LINKS</span></span>

[<span data-ttu-id="57bdb-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57bdb-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="57bdb-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57bdb-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="57bdb-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57bdb-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="57bdb-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57bdb-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="57bdb-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57bdb-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


