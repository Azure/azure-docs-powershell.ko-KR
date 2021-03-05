---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 622501a69632be9c9c70cfccaf4e806df94e7276
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006480"
---
# <span data-ttu-id="67e33-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="67e33-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="67e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e33-102">SYNOPSIS</span></span>
<span data-ttu-id="67e33-103">로드 밸런스에 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="67e33-104">구문</span><span class="sxs-lookup"><span data-stu-id="67e33-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e33-105">설명</span><span class="sxs-lookup"><span data-stu-id="67e33-105">DESCRIPTION</span></span>
<span data-ttu-id="67e33-106">**Add-AzLoadBalancerProbeConfig** cmdlet은 Azure 부하 분산기에 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="67e33-107">예제</span><span class="sxs-lookup"><span data-stu-id="67e33-107">EXAMPLES</span></span>

### <span data-ttu-id="67e33-108">예제 1: 부하 저울에 프로브 구성 추가</span><span class="sxs-lookup"><span data-stu-id="67e33-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="67e33-109">이 명령은 myLb라는 부하 분산 기능을 얻게 하여 지정된 프로브 구성을 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용하여 부하 분산 기능을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="67e33-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67e33-110">PARAMETERS</span></span>

### <span data-ttu-id="67e33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e33-111">-DefaultProfile</span></span>
<span data-ttu-id="67e33-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e33-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="67e33-113">-IntervalInSeconds</span></span>
<span data-ttu-id="67e33-114">부하 균형 서비스의 각 인스턴스에 대한 프로브 사이의 간격을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="67e33-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="67e33-115">-LoadBalancer</span></span>
<span data-ttu-id="67e33-116">**LoadBalancer 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="67e33-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="67e33-117">이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 프로브 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="67e33-118">-Name</span><span class="sxs-lookup"><span data-stu-id="67e33-118">-Name</span></span>
<span data-ttu-id="67e33-119">추가할 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="67e33-120">-Port</span><span class="sxs-lookup"><span data-stu-id="67e33-120">-Port</span></span>
<span data-ttu-id="67e33-121">부하가 조정된 서비스에 연결해야 하는 프로브의 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="67e33-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="67e33-122">-ProbeCount</span></span>
<span data-ttu-id="67e33-123">인스턴스에 대해 인스턴스당 연속 오류 수를 지정하여 부적당으로 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="67e33-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="67e33-124">-Protocol</span></span>
<span data-ttu-id="67e33-125">프로브에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="67e33-126">이 매개 변수에 대해 허용되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="67e33-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="67e33-127">-RequestPath</span></span>
<span data-ttu-id="67e33-128">상태 확인을 위해 프로브할 부하 균형 서비스의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="67e33-129">-확인</span><span class="sxs-lookup"><span data-stu-id="67e33-129">-Confirm</span></span>
<span data-ttu-id="67e33-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e33-131">-WhatIf</span></span>
<span data-ttu-id="67e33-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67e33-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e33-134">CommonParameters</span></span>
<span data-ttu-id="67e33-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67e33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e33-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67e33-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e33-137">입력</span><span class="sxs-lookup"><span data-stu-id="67e33-137">INPUTS</span></span>

### <span data-ttu-id="67e33-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="67e33-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="67e33-139">System.String</span><span class="sxs-lookup"><span data-stu-id="67e33-139">System.String</span></span>

### <span data-ttu-id="67e33-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="67e33-140">System.Int32</span></span>

## <span data-ttu-id="67e33-141">출력</span><span class="sxs-lookup"><span data-stu-id="67e33-141">OUTPUTS</span></span>

### <span data-ttu-id="67e33-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="67e33-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="67e33-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67e33-143">NOTES</span></span>

## <span data-ttu-id="67e33-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67e33-144">RELATED LINKS</span></span>

[<span data-ttu-id="67e33-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="67e33-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="67e33-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="67e33-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="67e33-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="67e33-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="67e33-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="67e33-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="67e33-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="67e33-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


