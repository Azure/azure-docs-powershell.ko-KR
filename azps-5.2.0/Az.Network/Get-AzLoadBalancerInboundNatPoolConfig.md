---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358898"
---
# <span data-ttu-id="62b73-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="62b73-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="62b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b73-102">SYNOPSIS</span></span>
<span data-ttu-id="62b73-103">부하 균형 조정기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b73-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="62b73-104">구문</span><span class="sxs-lookup"><span data-stu-id="62b73-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b73-105">설명</span><span class="sxs-lookup"><span data-stu-id="62b73-105">DESCRIPTION</span></span>
<span data-ttu-id="62b73-106">**Get-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산기에서 하나 이상의 인바운드 NAT 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b73-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="62b73-107">예제</span><span class="sxs-lookup"><span data-stu-id="62b73-107">EXAMPLES</span></span>

### <span data-ttu-id="62b73-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="62b73-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="62b73-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b73-109">PARAMETERS</span></span>

### <span data-ttu-id="62b73-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b73-110">-DefaultProfile</span></span>
<span data-ttu-id="62b73-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62b73-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b73-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62b73-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="62b73-113">-Name</span><span class="sxs-lookup"><span data-stu-id="62b73-113">-Name</span></span>
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

### <span data-ttu-id="62b73-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b73-114">CommonParameters</span></span>
<span data-ttu-id="62b73-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62b73-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b73-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62b73-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b73-117">입력</span><span class="sxs-lookup"><span data-stu-id="62b73-117">INPUTS</span></span>

### <span data-ttu-id="62b73-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62b73-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="62b73-119">출력</span><span class="sxs-lookup"><span data-stu-id="62b73-119">OUTPUTS</span></span>

### <span data-ttu-id="62b73-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="62b73-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="62b73-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62b73-121">NOTES</span></span>

## <span data-ttu-id="62b73-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62b73-122">RELATED LINKS</span></span>

[<span data-ttu-id="62b73-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="62b73-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="62b73-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="62b73-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="62b73-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="62b73-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="62b73-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="62b73-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
