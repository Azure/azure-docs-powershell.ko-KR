---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954560"
---
# <span data-ttu-id="57f9b-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57f9b-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="57f9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="57f9b-103">부하 저울에 대한 인바운드 NAT 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="57f9b-104">구문</span><span class="sxs-lookup"><span data-stu-id="57f9b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f9b-105">설명</span><span class="sxs-lookup"><span data-stu-id="57f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="57f9b-106">**Get-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure 부하 분산기에서 하나 이상의 NAT(인바운드 네트워크 주소 변환) 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="57f9b-107">예제</span><span class="sxs-lookup"><span data-stu-id="57f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="57f9b-108">예제 1: 인바운드 NAT 규칙 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="57f9b-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="57f9b-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 변수를 얻게 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="57f9b-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="57f9b-110">두 번째 명령은 MyInboundNatRule1이라는 연결된 NAT 규칙을 부하 $slb.</span><span class="sxs-lookup"><span data-stu-id="57f9b-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="57f9b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57f9b-111">PARAMETERS</span></span>

### <span data-ttu-id="57f9b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f9b-112">-DefaultProfile</span></span>
<span data-ttu-id="57f9b-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57f9b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57f9b-114">-LoadBalancer</span></span>
<span data-ttu-id="57f9b-115">얻을 인바운드 NAT 규칙 구성과 연결된 부하 균형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="57f9b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="57f9b-116">-Name</span></span>
<span data-ttu-id="57f9b-117">얻을 인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="57f9b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f9b-118">CommonParameters</span></span>
<span data-ttu-id="57f9b-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57f9b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f9b-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57f9b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f9b-121">입력</span><span class="sxs-lookup"><span data-stu-id="57f9b-121">INPUTS</span></span>

### <span data-ttu-id="57f9b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57f9b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="57f9b-123">출력</span><span class="sxs-lookup"><span data-stu-id="57f9b-123">OUTPUTS</span></span>

### <span data-ttu-id="57f9b-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="57f9b-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="57f9b-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57f9b-125">NOTES</span></span>

## <span data-ttu-id="57f9b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57f9b-126">RELATED LINKS</span></span>

[<span data-ttu-id="57f9b-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="57f9b-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="57f9b-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57f9b-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="57f9b-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57f9b-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="57f9b-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57f9b-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


