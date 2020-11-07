---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882574"
---
# <span data-ttu-id="74111-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74111-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="74111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74111-102">SYNOPSIS</span></span>
<span data-ttu-id="74111-103">부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74111-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74111-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74111-105">설명은</span><span class="sxs-lookup"><span data-stu-id="74111-105">DESCRIPTION</span></span>
<span data-ttu-id="74111-106">**AzureRmLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="74111-107">예제의</span><span class="sxs-lookup"><span data-stu-id="74111-107">EXAMPLES</span></span>

### <span data-ttu-id="74111-108">예제 1: 부하 분산 장치에서 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="74111-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="74111-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="74111-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyLBruleName 이라는 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="74111-111">변수</span><span class="sxs-lookup"><span data-stu-id="74111-111">PARAMETERS</span></span>

### <span data-ttu-id="74111-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74111-112">-DefaultProfile</span></span>
<span data-ttu-id="74111-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74111-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74111-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74111-114">-LoadBalancer</span></span>
<span data-ttu-id="74111-115">이 cmdlet이 제거 하는 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="74111-116">-이름</span><span class="sxs-lookup"><span data-stu-id="74111-116">-Name</span></span>
<span data-ttu-id="74111-117">이 cmdlet이 제거 하는 부하 분산 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74111-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74111-118">CommonParameters</span></span>
<span data-ttu-id="74111-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74111-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74111-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74111-121">입력</span><span class="sxs-lookup"><span data-stu-id="74111-121">INPUTS</span></span>

### <span data-ttu-id="74111-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74111-122">PSLoadBalancer</span></span>
<span data-ttu-id="74111-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="74111-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="74111-124">출력</span><span class="sxs-lookup"><span data-stu-id="74111-124">OUTPUTS</span></span>

### <span data-ttu-id="74111-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74111-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="74111-126">상속자</span><span class="sxs-lookup"><span data-stu-id="74111-126">NOTES</span></span>

## <span data-ttu-id="74111-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74111-127">RELATED LINKS</span></span>

[<span data-ttu-id="74111-128">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74111-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="74111-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74111-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="74111-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74111-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="74111-131">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74111-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="74111-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74111-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


