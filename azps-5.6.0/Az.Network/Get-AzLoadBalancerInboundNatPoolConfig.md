---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 74815c263435860f9281f476babc80574b63b161
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958635"
---
# <span data-ttu-id="6c8cf-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6c8cf-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="6c8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8cf-103">부하 균형 조정기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c8cf-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="6c8cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c8cf-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c8cf-105">설명</span><span class="sxs-lookup"><span data-stu-id="6c8cf-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8cf-106">**Get-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c8cf-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="6c8cf-107">예제</span><span class="sxs-lookup"><span data-stu-id="6c8cf-107">EXAMPLES</span></span>

### <span data-ttu-id="6c8cf-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="6c8cf-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="6c8cf-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6c8cf-109">PARAMETERS</span></span>

### <span data-ttu-id="6c8cf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8cf-110">-DefaultProfile</span></span>
<span data-ttu-id="6c8cf-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c8cf-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c8cf-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c8cf-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="6c8cf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6c8cf-113">-Name</span></span>
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

### <span data-ttu-id="6c8cf-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8cf-114">CommonParameters</span></span>
<span data-ttu-id="6c8cf-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8cf-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8cf-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c8cf-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8cf-117">입력</span><span class="sxs-lookup"><span data-stu-id="6c8cf-117">INPUTS</span></span>

### <span data-ttu-id="6c8cf-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c8cf-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6c8cf-119">출력</span><span class="sxs-lookup"><span data-stu-id="6c8cf-119">OUTPUTS</span></span>

### <span data-ttu-id="6c8cf-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="6c8cf-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="6c8cf-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c8cf-121">NOTES</span></span>

## <span data-ttu-id="6c8cf-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c8cf-122">RELATED LINKS</span></span>

[<span data-ttu-id="6c8cf-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6c8cf-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6c8cf-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6c8cf-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6c8cf-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6c8cf-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6c8cf-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6c8cf-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
