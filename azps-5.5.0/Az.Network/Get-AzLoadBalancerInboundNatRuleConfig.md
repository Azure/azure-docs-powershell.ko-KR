---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193860"
---
# <span data-ttu-id="c5229-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5229-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c5229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5229-102">SYNOPSIS</span></span>
<span data-ttu-id="c5229-103">부하 균형 조정에 대한 인바운드 NAT 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c5229-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5229-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5229-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5229-105">DESCRIPTION</span></span>
<span data-ttu-id="c5229-106">**Get-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure Load Balancer에서 하나 이상의 인바운드 NAT(네트워크 주소 변환) 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="c5229-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5229-107">EXAMPLES</span></span>

### <span data-ttu-id="c5229-108">예제 1: 인바운드 NAT 규칙 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="c5229-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="c5229-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 값을 사용하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="c5229-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="c5229-110">두 번째 명령은 MyInboundNatRule1이라는 연결된 NAT 규칙을 $slb.</span><span class="sxs-lookup"><span data-stu-id="c5229-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="c5229-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5229-111">PARAMETERS</span></span>

### <span data-ttu-id="c5229-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5229-112">-DefaultProfile</span></span>
<span data-ttu-id="c5229-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5229-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5229-114">-LoadBalancer</span></span>
<span data-ttu-id="c5229-115">얻을 인바운드 NAT 규칙 구성과 연결된 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="c5229-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c5229-116">-Name</span></span>
<span data-ttu-id="c5229-117">얻을 인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="c5229-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5229-118">CommonParameters</span></span>
<span data-ttu-id="c5229-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5229-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5229-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5229-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5229-121">입력</span><span class="sxs-lookup"><span data-stu-id="c5229-121">INPUTS</span></span>

### <span data-ttu-id="c5229-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5229-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c5229-123">출력</span><span class="sxs-lookup"><span data-stu-id="c5229-123">OUTPUTS</span></span>

### <span data-ttu-id="c5229-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c5229-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="c5229-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5229-125">NOTES</span></span>

## <span data-ttu-id="c5229-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5229-126">RELATED LINKS</span></span>

[<span data-ttu-id="c5229-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c5229-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c5229-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5229-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c5229-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5229-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c5229-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c5229-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


