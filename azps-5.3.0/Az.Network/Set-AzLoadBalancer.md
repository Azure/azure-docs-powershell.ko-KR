---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496523"
---
# <span data-ttu-id="5c5da-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="5c5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c5da-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5da-103">부하 균형 조정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-103">Updates a load balancer.</span></span>

## <span data-ttu-id="5c5da-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c5da-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c5da-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c5da-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5da-106">**Set-AzLoadBalancer** cmdlet은 부하 분산을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="5c5da-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c5da-107">EXAMPLES</span></span>

### <span data-ttu-id="5c5da-108">예제 1: 부하 균형 조정</span><span class="sxs-lookup"><span data-stu-id="5c5da-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="5c5da-109">첫 번째 명령은 NRPLB라는 부하 균형 조정을 구한 다음, $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5c5da-110">두 번째 명령은 파이프라인 연산자를 사용하여 $slb Load Balancer를 Add-AzLoadBalancerInboundNatRuleConfig에 전달합니다. 이 명령은 NewRule이라는 인바운드 NAT 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="5c5da-111">세 번째 명령은 부하 분산 시스템 구성을 업데이트하고 저장하는 **Set-AzLoadBalancer에** 부하 분산을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="5c5da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c5da-112">PARAMETERS</span></span>

### <span data-ttu-id="5c5da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c5da-113">-AsJob</span></span>
<span data-ttu-id="5c5da-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5c5da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c5da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5da-115">-DefaultProfile</span></span>
<span data-ttu-id="5c5da-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5da-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-117">-LoadBalancer</span></span>
<span data-ttu-id="5c5da-118">부하 균형 조정기를 설정해야 하는 상태를 나타내는 부하 균형 조정기 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5da-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c5da-119">-Confirm</span></span>
<span data-ttu-id="5c5da-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c5da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c5da-121">-WhatIf</span></span>
<span data-ttu-id="5c5da-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c5da-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c5da-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c5da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5da-124">CommonParameters</span></span>
<span data-ttu-id="5c5da-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c5da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5da-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5c5da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5da-127">입력</span><span class="sxs-lookup"><span data-stu-id="5c5da-127">INPUTS</span></span>

### <span data-ttu-id="5c5da-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5c5da-129">출력</span><span class="sxs-lookup"><span data-stu-id="5c5da-129">OUTPUTS</span></span>

### <span data-ttu-id="5c5da-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5c5da-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c5da-131">NOTES</span></span>

## <span data-ttu-id="5c5da-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c5da-132">RELATED LINKS</span></span>

[<span data-ttu-id="5c5da-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5c5da-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5c5da-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5c5da-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


