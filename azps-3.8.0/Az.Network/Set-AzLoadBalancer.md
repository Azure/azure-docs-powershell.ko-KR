---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879241"
---
# <span data-ttu-id="1c51e-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="1c51e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c51e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c51e-103">부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-103">Updates a load balancer.</span></span>

## <span data-ttu-id="1c51e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c51e-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c51e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c51e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c51e-106">**AzLoadBalancer** cmdlet은 부하 분산을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="1c51e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c51e-107">EXAMPLES</span></span>

### <span data-ttu-id="1c51e-108">예제 1: 부하 분산 장치 수정</span><span class="sxs-lookup"><span data-stu-id="1c51e-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="1c51e-109">첫 번째 명령은 NRPLB 이라는 부하 분산 장치를 가져온 다음이를 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1c51e-110">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 로드 균형 조정기를 Add-AzLoadBalancerInboundNatRuleConfig에 전달 하 여 NewRule 이라는 인바운드 NAT 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="1c51e-111">세 번째 명령은 부하 분산 장치 구성을 업데이트 하 고 저장 하는 부하 분산을 **설정-AzLoadBalancer** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="1c51e-112">변수</span><span class="sxs-lookup"><span data-stu-id="1c51e-112">PARAMETERS</span></span>

### <span data-ttu-id="1c51e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c51e-113">-AsJob</span></span>
<span data-ttu-id="1c51e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1c51e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c51e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c51e-115">-DefaultProfile</span></span>
<span data-ttu-id="1c51e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c51e-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-117">-LoadBalancer</span></span>
<span data-ttu-id="1c51e-118">부하 분산을 설정 해야 하는 상태를 나타내는 부하 분산 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="1c51e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1c51e-119">-Confirm</span></span>
<span data-ttu-id="1c51e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c51e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c51e-121">-WhatIf</span></span>
<span data-ttu-id="1c51e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c51e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c51e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c51e-124">CommonParameters</span></span>
<span data-ttu-id="1c51e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c51e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c51e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c51e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c51e-127">입력</span><span class="sxs-lookup"><span data-stu-id="1c51e-127">INPUTS</span></span>

### <span data-ttu-id="1c51e-128">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1c51e-129">출력</span><span class="sxs-lookup"><span data-stu-id="1c51e-129">OUTPUTS</span></span>

### <span data-ttu-id="1c51e-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1c51e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1c51e-131">NOTES</span></span>

## <span data-ttu-id="1c51e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c51e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c51e-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1c51e-134">새로운 AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="1c51e-135">제거-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1c51e-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

