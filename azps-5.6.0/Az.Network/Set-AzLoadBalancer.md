---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: b608a8fe62f7316116409d4174ea01603b928ae2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963936"
---
# <span data-ttu-id="5b238-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="5b238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b238-102">SYNOPSIS</span></span>
<span data-ttu-id="5b238-103">부하 잔액을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-103">Updates a load balancer.</span></span>

## <span data-ttu-id="5b238-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b238-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b238-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b238-105">DESCRIPTION</span></span>
<span data-ttu-id="5b238-106">**Set-AzLoadBalancer** cmdlet은 부하 분산을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="5b238-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b238-107">EXAMPLES</span></span>

### <span data-ttu-id="5b238-108">예제 1: 부하 조정기 수정</span><span class="sxs-lookup"><span data-stu-id="5b238-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="5b238-109">첫 번째 명령은 NRPLB라는 부하 $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5b238-110">두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerInboundNatRuleConfig에 전달하여 NewRule이라는 인바운드 NAT 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="5b238-111">세 번째 명령은 부하 분산기 구성을 업데이트하고 저장하는 **Set-AzLoadBalancer로** 부하 분산을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="5b238-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b238-112">PARAMETERS</span></span>

### <span data-ttu-id="5b238-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b238-113">-AsJob</span></span>
<span data-ttu-id="5b238-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b238-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b238-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b238-115">-DefaultProfile</span></span>
<span data-ttu-id="5b238-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b238-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-117">-LoadBalancer</span></span>
<span data-ttu-id="5b238-118">부하 균형 조정기를 설정해야 하는 상태를 나타내는 부하 균형기 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="5b238-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5b238-119">-Confirm</span></span>
<span data-ttu-id="5b238-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b238-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b238-121">-WhatIf</span></span>
<span data-ttu-id="5b238-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b238-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b238-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b238-124">CommonParameters</span></span>
<span data-ttu-id="5b238-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b238-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b238-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b238-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b238-127">입력</span><span class="sxs-lookup"><span data-stu-id="5b238-127">INPUTS</span></span>

### <span data-ttu-id="5b238-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5b238-129">출력</span><span class="sxs-lookup"><span data-stu-id="5b238-129">OUTPUTS</span></span>

### <span data-ttu-id="5b238-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5b238-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b238-131">NOTES</span></span>

## <span data-ttu-id="5b238-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b238-132">RELATED LINKS</span></span>

[<span data-ttu-id="5b238-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5b238-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5b238-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5b238-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


