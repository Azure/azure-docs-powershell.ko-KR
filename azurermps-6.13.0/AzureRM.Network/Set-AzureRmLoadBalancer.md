---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531977"
---
# <span data-ttu-id="1e9f6-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="1e9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9f6-103">부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e9f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e9f6-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e9f6-105">DESCRIPTION</span></span>
<span data-ttu-id="1e9f6-106">**AzureRmLoadBalancer** Cmdlet은 Azure 부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="1e9f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e9f6-107">EXAMPLES</span></span>

### <span data-ttu-id="1e9f6-108">예제 1: 부하 분산 장치 수정</span><span class="sxs-lookup"><span data-stu-id="1e9f6-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="1e9f6-109">첫 번째 명령은 NRPLB 이라는 부하 분산 장치를 가져온 다음이를 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1e9f6-110">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 로드 균형 조정기를 Add-AzureRmLoadBalancerInboundNatRuleConfig에 전달 하 여 NewRule 이라는 인바운드 NAT 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="1e9f6-111">세 번째 명령은 부하 분산 장치 구성을 업데이트 하 고 저장 하는 부하 분산을 **설정-AzureRmLoadBalancer** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="1e9f6-112">변수</span><span class="sxs-lookup"><span data-stu-id="1e9f6-112">PARAMETERS</span></span>

### <span data-ttu-id="1e9f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e9f6-113">-AsJob</span></span>
<span data-ttu-id="1e9f6-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1e9f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e9f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9f6-115">-DefaultProfile</span></span>
<span data-ttu-id="1e9f6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9f6-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-117">-LoadBalancer</span></span>
<span data-ttu-id="1e9f6-118">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-118">Specifies a load balancer.</span></span>
<span data-ttu-id="1e9f6-119">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e9f6-120">-확인</span><span class="sxs-lookup"><span data-stu-id="1e9f6-120">-Confirm</span></span>
<span data-ttu-id="1e9f6-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9f6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9f6-122">-WhatIf</span></span>
<span data-ttu-id="1e9f6-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e9f6-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9f6-125">CommonParameters</span></span>
<span data-ttu-id="1e9f6-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9f6-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e9f6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9f6-128">입력</span><span class="sxs-lookup"><span data-stu-id="1e9f6-128">INPUTS</span></span>

### <span data-ttu-id="1e9f6-129">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="1e9f6-130">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e9f6-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="1e9f6-131">출력</span><span class="sxs-lookup"><span data-stu-id="1e9f6-131">OUTPUTS</span></span>

### <span data-ttu-id="1e9f6-132">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1e9f6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="1e9f6-133">NOTES</span></span>

## <span data-ttu-id="1e9f6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e9f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e9f6-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="1e9f6-136">새로운 AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="1e9f6-137">제거-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e9f6-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

