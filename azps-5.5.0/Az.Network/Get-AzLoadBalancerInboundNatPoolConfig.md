---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203081"
---
# <span data-ttu-id="9608d-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9608d-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9608d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9608d-102">SYNOPSIS</span></span>
<span data-ttu-id="9608d-103">부하 균형 조정기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608d-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="9608d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9608d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9608d-105">설명</span><span class="sxs-lookup"><span data-stu-id="9608d-105">DESCRIPTION</span></span>
<span data-ttu-id="9608d-106">**Get-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9608d-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="9608d-107">예제</span><span class="sxs-lookup"><span data-stu-id="9608d-107">EXAMPLES</span></span>

### <span data-ttu-id="9608d-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="9608d-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="9608d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9608d-109">PARAMETERS</span></span>

### <span data-ttu-id="9608d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9608d-110">-DefaultProfile</span></span>
<span data-ttu-id="9608d-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9608d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9608d-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9608d-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="9608d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9608d-113">-Name</span></span>
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

### <span data-ttu-id="9608d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9608d-114">CommonParameters</span></span>
<span data-ttu-id="9608d-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9608d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9608d-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9608d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9608d-117">입력</span><span class="sxs-lookup"><span data-stu-id="9608d-117">INPUTS</span></span>

### <span data-ttu-id="9608d-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9608d-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9608d-119">출력</span><span class="sxs-lookup"><span data-stu-id="9608d-119">OUTPUTS</span></span>

### <span data-ttu-id="9608d-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="9608d-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="9608d-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9608d-121">NOTES</span></span>

## <span data-ttu-id="9608d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9608d-122">RELATED LINKS</span></span>

[<span data-ttu-id="9608d-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9608d-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9608d-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9608d-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9608d-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9608d-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9608d-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9608d-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
