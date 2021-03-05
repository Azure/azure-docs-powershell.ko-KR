---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006448"
---
# <span data-ttu-id="7fb1b-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb1b-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="7fb1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb1b-103">부하 저울에서 아웃바운드 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="7fb1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fb1b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fb1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="7fb1b-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb1b-106">**Get-AzLoadBalancerOutboundRuleConfig** cmdlet은 부하 분산기에서 아웃바운드 규칙 구성 또는 아웃바운드 규칙 구성 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="7fb1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="7fb1b-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb1b-108">예제 1: 부하 저울에서 아웃바운드 규칙 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="7fb1b-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="7fb1b-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 변수를 얻은 다음, 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="7fb1b-110">두 번째 명령은 해당 부하 균형 조정기와 연결된 MyRule이라는 아웃바운드 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="7fb1b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7fb1b-111">PARAMETERS</span></span>

### <span data-ttu-id="7fb1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb1b-112">-DefaultProfile</span></span>
<span data-ttu-id="7fb1b-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb1b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7fb1b-114">-LoadBalancer</span></span>
<span data-ttu-id="7fb1b-115">부하 균형기 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="7fb1b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7fb1b-116">-Name</span></span>
<span data-ttu-id="7fb1b-117">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="7fb1b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb1b-118">CommonParameters</span></span>
<span data-ttu-id="7fb1b-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb1b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb1b-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fb1b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb1b-121">입력</span><span class="sxs-lookup"><span data-stu-id="7fb1b-121">INPUTS</span></span>

### <span data-ttu-id="7fb1b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7fb1b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7fb1b-123">출력</span><span class="sxs-lookup"><span data-stu-id="7fb1b-123">OUTPUTS</span></span>

### <span data-ttu-id="7fb1b-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="7fb1b-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="7fb1b-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fb1b-125">NOTES</span></span>

## <span data-ttu-id="7fb1b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fb1b-126">RELATED LINKS</span></span>

[<span data-ttu-id="7fb1b-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb1b-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7fb1b-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb1b-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7fb1b-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb1b-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7fb1b-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb1b-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
