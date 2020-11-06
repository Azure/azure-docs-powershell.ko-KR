---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528918"
---
# <span data-ttu-id="b3de3-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="b3de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3de3-102">SYNOPSIS</span></span>
<span data-ttu-id="b3de3-103">부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3de3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3de3-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3de3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3de3-105">DESCRIPTION</span></span>
<span data-ttu-id="b3de3-106">**AzureRmLoadBalancer** Cmdlet은 Azure 부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="b3de3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3de3-107">EXAMPLES</span></span>

### <span data-ttu-id="b3de3-108">예제 1: 부하 분산 장치 수정</span><span class="sxs-lookup"><span data-stu-id="b3de3-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b3de3-109">첫 번째 명령은 NRPLB 이라는 부하 분산 장치를 가져온 다음이를 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b3de3-110">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 로드 균형 조정기를 Add-AzureRmLoadBalancerInboundNatRuleConfig에 전달 하 여 NewRule 이라는 인바운드 NAT 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="b3de3-111">세 번째 명령은 부하 분산 장치 구성을 업데이트 하 고 저장 하는 부하 분산을 **설정-AzureRmLoadBalancer** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="b3de3-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3de3-112">PARAMETERS</span></span>

### <span data-ttu-id="b3de3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3de3-113">-AsJob</span></span>
<span data-ttu-id="b3de3-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b3de3-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3de3-115">-DefaultProfile</span></span>
<span data-ttu-id="b3de3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de3-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-117">-LoadBalancer</span></span>
<span data-ttu-id="b3de3-118">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-118">Specifies a load balancer.</span></span>
<span data-ttu-id="b3de3-119">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3de3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3de3-120">CommonParameters</span></span>
<span data-ttu-id="b3de3-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3de3-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3de3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3de3-123">입력</span><span class="sxs-lookup"><span data-stu-id="b3de3-123">INPUTS</span></span>

### <span data-ttu-id="b3de3-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-124">PSLoadBalancer</span></span>
<span data-ttu-id="b3de3-125">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3de3-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b3de3-126">출력</span><span class="sxs-lookup"><span data-stu-id="b3de3-126">OUTPUTS</span></span>

### <span data-ttu-id="b3de3-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b3de3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b3de3-128">NOTES</span></span>

## <span data-ttu-id="b3de3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3de3-129">RELATED LINKS</span></span>

[<span data-ttu-id="b3de3-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b3de3-131">새로운 AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="b3de3-132">제거-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de3-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


