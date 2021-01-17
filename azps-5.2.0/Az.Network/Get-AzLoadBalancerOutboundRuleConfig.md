---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345489"
---
# <span data-ttu-id="54be1-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54be1-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="54be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54be1-102">SYNOPSIS</span></span>
<span data-ttu-id="54be1-103">부하 균형 조정기에서 아웃바운드 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="54be1-104">구문</span><span class="sxs-lookup"><span data-stu-id="54be1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54be1-105">설명</span><span class="sxs-lookup"><span data-stu-id="54be1-105">DESCRIPTION</span></span>
<span data-ttu-id="54be1-106">**Get-AzLoadBalancerOutboundRuleConfig** cmdlet은 부하 분산의 아웃바운드 규칙 구성 또는 아웃바운드 규칙 구성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="54be1-107">예제</span><span class="sxs-lookup"><span data-stu-id="54be1-107">EXAMPLES</span></span>

### <span data-ttu-id="54be1-108">예제 1: 부하 균형 조정기에서 아웃바운드 규칙 구성을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="54be1-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="54be1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="54be1-110">두 번째 명령은 해당 부하 균형 조정과 연결된 MyRule이라는 아웃바운드 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="54be1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54be1-111">PARAMETERS</span></span>

### <span data-ttu-id="54be1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54be1-112">-DefaultProfile</span></span>
<span data-ttu-id="54be1-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54be1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54be1-114">-LoadBalancer</span></span>
<span data-ttu-id="54be1-115">부하 균형 조정기 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="54be1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="54be1-116">-Name</span></span>
<span data-ttu-id="54be1-117">아웃바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="54be1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54be1-118">CommonParameters</span></span>
<span data-ttu-id="54be1-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54be1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54be1-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54be1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54be1-121">입력</span><span class="sxs-lookup"><span data-stu-id="54be1-121">INPUTS</span></span>

### <span data-ttu-id="54be1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54be1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="54be1-123">출력</span><span class="sxs-lookup"><span data-stu-id="54be1-123">OUTPUTS</span></span>

### <span data-ttu-id="54be1-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="54be1-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="54be1-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54be1-125">NOTES</span></span>

## <span data-ttu-id="54be1-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54be1-126">RELATED LINKS</span></span>

[<span data-ttu-id="54be1-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54be1-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="54be1-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54be1-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="54be1-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54be1-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="54be1-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54be1-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
