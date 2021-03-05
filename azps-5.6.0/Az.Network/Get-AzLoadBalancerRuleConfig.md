---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006427"
---
# <span data-ttu-id="8a398-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a398-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="8a398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a398-102">SYNOPSIS</span></span>
<span data-ttu-id="8a398-103">부하 저울에 대한 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8a398-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a398-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a398-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a398-105">DESCRIPTION</span></span>
<span data-ttu-id="8a398-106">**Get-AzLoadBalancerRuleConfig** cmdlet은 부하 분산기에 대한 하나 이상의 규칙 구성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="8a398-107">예제</span><span class="sxs-lookup"><span data-stu-id="8a398-107">EXAMPLES</span></span>

### <span data-ttu-id="8a398-108">예제 1: 부하 저울의 규칙 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="8a398-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 변수를 얻은 다음, 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="8a398-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="8a398-110">두 번째 명령은 MyLBrulename이라는 연결된 규칙 구성을 $slb.</span><span class="sxs-lookup"><span data-stu-id="8a398-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="8a398-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a398-111">PARAMETERS</span></span>

### <span data-ttu-id="8a398-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a398-112">-DefaultProfile</span></span>
<span data-ttu-id="8a398-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a398-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8a398-114">-LoadBalancer</span></span>
<span data-ttu-id="8a398-115">얻을 규칙 구성과 연결된 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="8a398-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8a398-116">-Name</span></span>
<span data-ttu-id="8a398-117">얻을 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="8a398-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a398-118">CommonParameters</span></span>
<span data-ttu-id="8a398-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a398-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a398-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a398-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a398-121">입력</span><span class="sxs-lookup"><span data-stu-id="8a398-121">INPUTS</span></span>

### <span data-ttu-id="8a398-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8a398-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8a398-123">출력</span><span class="sxs-lookup"><span data-stu-id="8a398-123">OUTPUTS</span></span>

### <span data-ttu-id="8a398-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="8a398-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="8a398-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a398-125">NOTES</span></span>

## <span data-ttu-id="8a398-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a398-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a398-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a398-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8a398-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8a398-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8a398-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a398-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8a398-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a398-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


