---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492557"
---
# <span data-ttu-id="27280-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27280-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="27280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27280-102">SYNOPSIS</span></span>
<span data-ttu-id="27280-103">부하 균형 조정기에서 프로브 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="27280-104">구문</span><span class="sxs-lookup"><span data-stu-id="27280-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27280-105">설명</span><span class="sxs-lookup"><span data-stu-id="27280-105">DESCRIPTION</span></span>
<span data-ttu-id="27280-106">**Remove-AzLoadBalancerProbeConfig** cmdlet은 부하 분산기에서 프로브 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="27280-107">예제</span><span class="sxs-lookup"><span data-stu-id="27280-107">EXAMPLES</span></span>

### <span data-ttu-id="27280-108">예제 1: 부하 균형 조정기에서 프로브 구성 제거</span><span class="sxs-lookup"><span data-stu-id="27280-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="27280-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 $loadbalancer 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="27280-110">두 번째 명령은 MyProbe라는 구성을 해당 명령의 부하 $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="27280-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="27280-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27280-111">PARAMETERS</span></span>

### <span data-ttu-id="27280-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27280-112">-DefaultProfile</span></span>
<span data-ttu-id="27280-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27280-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27280-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27280-114">-LoadBalancer</span></span>
<span data-ttu-id="27280-115">이 cmdlet에서 제거하는 프로브 구성을 포함하는 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27280-116">-Name</span><span class="sxs-lookup"><span data-stu-id="27280-116">-Name</span></span>
<span data-ttu-id="27280-117">이 cmdlet이 제거하는 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27280-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27280-118">-Confirm</span></span>
<span data-ttu-id="27280-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27280-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27280-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27280-120">-WhatIf</span></span>
<span data-ttu-id="27280-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="27280-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27280-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27280-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27280-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27280-123">CommonParameters</span></span>
<span data-ttu-id="27280-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27280-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27280-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27280-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27280-126">입력</span><span class="sxs-lookup"><span data-stu-id="27280-126">INPUTS</span></span>

### <span data-ttu-id="27280-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27280-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27280-128">출력</span><span class="sxs-lookup"><span data-stu-id="27280-128">OUTPUTS</span></span>

### <span data-ttu-id="27280-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27280-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27280-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27280-130">NOTES</span></span>

## <span data-ttu-id="27280-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27280-131">RELATED LINKS</span></span>

[<span data-ttu-id="27280-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27280-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27280-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27280-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27280-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27280-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27280-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27280-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="27280-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="27280-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


