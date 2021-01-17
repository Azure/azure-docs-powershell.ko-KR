---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365597"
---
# <span data-ttu-id="646ee-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="646ee-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="646ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="646ee-102">SYNOPSIS</span></span>
<span data-ttu-id="646ee-103">부하 균형 조정에 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="646ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="646ee-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646ee-105">설명</span><span class="sxs-lookup"><span data-stu-id="646ee-105">DESCRIPTION</span></span>
<span data-ttu-id="646ee-106">**Add-AzLoadBalancerProbeConfig** cmdlet은 Azure Load Balancer에 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="646ee-107">예제</span><span class="sxs-lookup"><span data-stu-id="646ee-107">EXAMPLES</span></span>

### <span data-ttu-id="646ee-108">예제 1: 부하 균형 조정에 프로브 구성 추가</span><span class="sxs-lookup"><span data-stu-id="646ee-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="646ee-109">이 명령은 myLb라는 부하 분산 기능을 사용하여 지정된 프로브 구성을 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용하여 부하 분산을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="646ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="646ee-110">PARAMETERS</span></span>

### <span data-ttu-id="646ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646ee-111">-DefaultProfile</span></span>
<span data-ttu-id="646ee-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="646ee-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="646ee-113">-IntervalInSeconds</span></span>
<span data-ttu-id="646ee-114">부하가 균형 잡힌 서비스의 각 인스턴스에 대한 프로브 사이의 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="646ee-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646ee-115">-LoadBalancer</span></span>
<span data-ttu-id="646ee-116">**LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="646ee-117">이 cmdlet은 이 매개 변수가 지정하는 프로브 구성을 부하 균형 조정에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="646ee-118">-Name</span><span class="sxs-lookup"><span data-stu-id="646ee-118">-Name</span></span>
<span data-ttu-id="646ee-119">추가할 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="646ee-120">-Port</span><span class="sxs-lookup"><span data-stu-id="646ee-120">-Port</span></span>
<span data-ttu-id="646ee-121">프로브가 부하가 균형 잡힌 서비스에 연결해야 하는 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="646ee-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="646ee-122">-ProbeCount</span></span>
<span data-ttu-id="646ee-123">인스턴스가 비보안으로 간주될 인스턴스당 연속 오류 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="646ee-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="646ee-124">-Protocol</span></span>
<span data-ttu-id="646ee-125">프로브에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="646ee-126">이 매개 변수에 허용되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="646ee-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="646ee-127">-RequestPath</span></span>
<span data-ttu-id="646ee-128">상태 확인을 위해 프로브할 부하가 균형 잡힌 서비스의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="646ee-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="646ee-129">-Confirm</span></span>
<span data-ttu-id="646ee-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646ee-131">-WhatIf</span></span>
<span data-ttu-id="646ee-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="646ee-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="646ee-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646ee-134">CommonParameters</span></span>
<span data-ttu-id="646ee-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="646ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646ee-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="646ee-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646ee-137">입력</span><span class="sxs-lookup"><span data-stu-id="646ee-137">INPUTS</span></span>

### <span data-ttu-id="646ee-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646ee-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="646ee-139">System.String</span><span class="sxs-lookup"><span data-stu-id="646ee-139">System.String</span></span>

### <span data-ttu-id="646ee-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="646ee-140">System.Int32</span></span>

## <span data-ttu-id="646ee-141">출력</span><span class="sxs-lookup"><span data-stu-id="646ee-141">OUTPUTS</span></span>

### <span data-ttu-id="646ee-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646ee-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="646ee-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="646ee-143">NOTES</span></span>

## <span data-ttu-id="646ee-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="646ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="646ee-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="646ee-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="646ee-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="646ee-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="646ee-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="646ee-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="646ee-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="646ee-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="646ee-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="646ee-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


