---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003424"
---
# <span data-ttu-id="0f694-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f694-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0f694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f694-102">SYNOPSIS</span></span>
<span data-ttu-id="0f694-103">부하 저울에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="0f694-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f694-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f694-105">설명</span><span class="sxs-lookup"><span data-stu-id="0f694-105">DESCRIPTION</span></span>
<span data-ttu-id="0f694-106">**Set-AzLoadBalancerProbeConfig** cmdlet은 부하 분산기에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="0f694-107">예제</span><span class="sxs-lookup"><span data-stu-id="0f694-107">EXAMPLES</span></span>

### <span data-ttu-id="0f694-108">예제 1: 부하 저울에서 프로브 구성 수정</span><span class="sxs-lookup"><span data-stu-id="0f694-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="0f694-109">첫 번째 명령은 MyLoadBalancer라는 loadbalancer를 구한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="0f694-110">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerProbeConfig에 전달하여 새 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="0f694-111">세 번째 명령은 부하 분산을 **Set-AzLoadBalancerProbeConfig로 전달하여** 새 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="0f694-112">현재 cmdlet에서 요구하기 때문에 이전 명령에 지정된 동일한 매개 변수 중 몇 가지를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="0f694-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f694-113">PARAMETERS</span></span>

### <span data-ttu-id="0f694-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f694-114">-DefaultProfile</span></span>
<span data-ttu-id="0f694-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f694-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0f694-116">-IntervalInSeconds</span></span>
<span data-ttu-id="0f694-117">부하 균형 서비스의 각 인스턴스에 대한 프로브 사이의 간격을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="0f694-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f694-118">-LoadBalancer</span></span>
<span data-ttu-id="0f694-119">부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-119">Specifies a load balancer.</span></span>
<span data-ttu-id="0f694-120">이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 대한 프로브 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f694-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0f694-121">-Name</span></span>
<span data-ttu-id="0f694-122">이 cmdlet에서 설정하는 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0f694-123">-Port</span><span class="sxs-lookup"><span data-stu-id="0f694-123">-Port</span></span>
<span data-ttu-id="0f694-124">부하가 조정된 서비스에 연결해야 하는 프로브의 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="0f694-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="0f694-125">-ProbeCount</span></span>
<span data-ttu-id="0f694-126">인스턴스에 대해 인스턴스당 연속 오류 수를 지정하여 부적당으로 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="0f694-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0f694-127">-Protocol</span></span>
<span data-ttu-id="0f694-128">프로비전에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="0f694-129">이 매개 변수에 대해 허용되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="0f694-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="0f694-130">-RequestPath</span></span>
<span data-ttu-id="0f694-131">상태 확인을 위해 프로브할 부하 균형 서비스의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="0f694-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0f694-132">-Confirm</span></span>
<span data-ttu-id="0f694-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f694-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f694-134">-WhatIf</span></span>
<span data-ttu-id="0f694-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f694-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f694-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f694-137">CommonParameters</span></span>
<span data-ttu-id="0f694-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f694-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f694-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f694-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f694-140">입력</span><span class="sxs-lookup"><span data-stu-id="0f694-140">INPUTS</span></span>

### <span data-ttu-id="0f694-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f694-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0f694-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0f694-142">System.String</span></span>

### <span data-ttu-id="0f694-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0f694-143">System.Int32</span></span>

## <span data-ttu-id="0f694-144">출력</span><span class="sxs-lookup"><span data-stu-id="0f694-144">OUTPUTS</span></span>

### <span data-ttu-id="0f694-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f694-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f694-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f694-146">NOTES</span></span>

## <span data-ttu-id="0f694-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f694-147">RELATED LINKS</span></span>

[<span data-ttu-id="0f694-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f694-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f694-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f694-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0f694-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f694-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f694-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f694-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f694-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f694-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


