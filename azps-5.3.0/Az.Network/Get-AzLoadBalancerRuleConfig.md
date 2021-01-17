---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380087"
---
# <span data-ttu-id="f1be9-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1be9-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f1be9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1be9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1be9-103">부하 균형 조정에 대한 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f1be9-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1be9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1be9-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1be9-105">DESCRIPTION</span></span>
<span data-ttu-id="f1be9-106">**Get-AzLoadBalancerRuleConfig** cmdlet은 부하 분산에 대한 하나 이상의 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="f1be9-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1be9-107">EXAMPLES</span></span>

### <span data-ttu-id="f1be9-108">예제 1: 부하 균형 조정의 규칙 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="f1be9-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="f1be9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f1be9-110">두 번째 명령은 MyLBrulename이라는 연결된 규칙 구성을 $slb.</span><span class="sxs-lookup"><span data-stu-id="f1be9-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="f1be9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1be9-111">PARAMETERS</span></span>

### <span data-ttu-id="f1be9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1be9-112">-DefaultProfile</span></span>
<span data-ttu-id="f1be9-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1be9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1be9-114">-LoadBalancer</span></span>
<span data-ttu-id="f1be9-115">얻을 규칙 구성과 연결된 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="f1be9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f1be9-116">-Name</span></span>
<span data-ttu-id="f1be9-117">얻을 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="f1be9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1be9-118">CommonParameters</span></span>
<span data-ttu-id="f1be9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1be9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1be9-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1be9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1be9-121">입력</span><span class="sxs-lookup"><span data-stu-id="f1be9-121">INPUTS</span></span>

### <span data-ttu-id="f1be9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1be9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f1be9-123">출력</span><span class="sxs-lookup"><span data-stu-id="f1be9-123">OUTPUTS</span></span>

### <span data-ttu-id="f1be9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f1be9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="f1be9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1be9-125">NOTES</span></span>

## <span data-ttu-id="f1be9-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1be9-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1be9-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1be9-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f1be9-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f1be9-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f1be9-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1be9-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f1be9-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1be9-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


