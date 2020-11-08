---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216219"
---
# <span data-ttu-id="81659-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81659-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="81659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81659-102">SYNOPSIS</span></span>
<span data-ttu-id="81659-103">부하 분산 장치에 대 한 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81659-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="81659-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81659-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81659-105">설명은</span><span class="sxs-lookup"><span data-stu-id="81659-105">DESCRIPTION</span></span>
<span data-ttu-id="81659-106">**AzLoadBalancerRuleConfig** cmdlet은 부하 분산 장치에 대 한 하나 이상의 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81659-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="81659-107">예제의</span><span class="sxs-lookup"><span data-stu-id="81659-107">EXAMPLES</span></span>

### <span data-ttu-id="81659-108">예제 1: 부하 분산 장치에 대 한 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="81659-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="81659-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="81659-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="81659-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyLBrulename 이라는 연결 된 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81659-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="81659-111">변수</span><span class="sxs-lookup"><span data-stu-id="81659-111">PARAMETERS</span></span>

### <span data-ttu-id="81659-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81659-112">-DefaultProfile</span></span>
<span data-ttu-id="81659-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81659-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81659-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="81659-114">-LoadBalancer</span></span>
<span data-ttu-id="81659-115">가져올 규칙 구성에 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81659-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="81659-116">-이름</span><span class="sxs-lookup"><span data-stu-id="81659-116">-Name</span></span>
<span data-ttu-id="81659-117">가져올 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81659-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="81659-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81659-118">CommonParameters</span></span>
<span data-ttu-id="81659-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81659-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81659-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81659-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81659-121">입력</span><span class="sxs-lookup"><span data-stu-id="81659-121">INPUTS</span></span>

### <span data-ttu-id="81659-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="81659-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="81659-123">출력</span><span class="sxs-lookup"><span data-stu-id="81659-123">OUTPUTS</span></span>

### <span data-ttu-id="81659-124">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="81659-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="81659-125">상속자</span><span class="sxs-lookup"><span data-stu-id="81659-125">NOTES</span></span>

## <span data-ttu-id="81659-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81659-126">RELATED LINKS</span></span>

[<span data-ttu-id="81659-127">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81659-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="81659-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="81659-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="81659-129">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81659-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="81659-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="81659-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


