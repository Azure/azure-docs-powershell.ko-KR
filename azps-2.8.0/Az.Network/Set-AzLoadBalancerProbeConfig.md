---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 475a85353e4731a1bdb8f95a88328ffa27f99cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869557"
---
# <span data-ttu-id="8b95d-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b95d-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="8b95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b95d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b95d-103">부하 분산 장치에 대 한 프로브 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="8b95d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b95d-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b95d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b95d-105">DESCRIPTION</span></span>
<span data-ttu-id="8b95d-106">**AzLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에 대 한 프로브 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="8b95d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b95d-107">EXAMPLES</span></span>

### <span data-ttu-id="8b95d-108">예제 1: 부하 분산 장치에서 프로브 구성 수정</span><span class="sxs-lookup"><span data-stu-id="8b95d-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="8b95d-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8b95d-110">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 추가-AzLoadBalancerProbeConfig에 전달 하 여 새 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="8b95d-111">세 번째 명령은 새 구성을 설정 하는 **AzLoadBalancerProbeConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="8b95d-112">이전 명령에 지정 된 것과 동일한 매개 변수 중 몇 개는 현재 cmdlet에 필요 하므로 반드시 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="8b95d-113">변수</span><span class="sxs-lookup"><span data-stu-id="8b95d-113">PARAMETERS</span></span>

### <span data-ttu-id="8b95d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b95d-114">-DefaultProfile</span></span>
<span data-ttu-id="8b95d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b95d-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8b95d-116">-IntervalInSeconds</span></span>
<span data-ttu-id="8b95d-117">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="8b95d-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b95d-118">-LoadBalancer</span></span>
<span data-ttu-id="8b95d-119">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-119">Specifies a load balancer.</span></span>
<span data-ttu-id="8b95d-120">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 프로브 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b95d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8b95d-121">-Name</span></span>
<span data-ttu-id="8b95d-122">이 cmdlet이 설정 하는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8b95d-123">-포트</span><span class="sxs-lookup"><span data-stu-id="8b95d-123">-Port</span></span>
<span data-ttu-id="8b95d-124">프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="8b95d-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="8b95d-125">-ProbeCount</span></span>
<span data-ttu-id="8b95d-126">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="8b95d-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="8b95d-127">-Protocol</span></span>
<span data-ttu-id="8b95d-128">검색에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="8b95d-129">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="8b95d-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="8b95d-130">-RequestPath</span></span>
<span data-ttu-id="8b95d-131">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="8b95d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8b95d-132">-Confirm</span></span>
<span data-ttu-id="8b95d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b95d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b95d-134">-WhatIf</span></span>
<span data-ttu-id="8b95d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b95d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b95d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b95d-137">CommonParameters</span></span>
<span data-ttu-id="8b95d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b95d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b95d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b95d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b95d-140">입력</span><span class="sxs-lookup"><span data-stu-id="8b95d-140">INPUTS</span></span>

### <span data-ttu-id="8b95d-141">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b95d-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="8b95d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8b95d-142">System.String</span></span>

### <span data-ttu-id="8b95d-143">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="8b95d-143">System.Int32</span></span>

## <span data-ttu-id="8b95d-144">출력</span><span class="sxs-lookup"><span data-stu-id="8b95d-144">OUTPUTS</span></span>

### <span data-ttu-id="8b95d-145">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b95d-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8b95d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8b95d-146">NOTES</span></span>

## <span data-ttu-id="8b95d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b95d-147">RELATED LINKS</span></span>

[<span data-ttu-id="8b95d-148">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b95d-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8b95d-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b95d-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8b95d-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b95d-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8b95d-151">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b95d-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8b95d-152">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b95d-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


