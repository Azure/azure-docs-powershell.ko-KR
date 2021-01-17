---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350793"
---
# <span data-ttu-id="f8fec-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f8fec-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f8fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8fec-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fec-103">부하 균형 조정에 대한 프로브 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="f8fec-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8fec-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fec-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8fec-105">DESCRIPTION</span></span>
<span data-ttu-id="f8fec-106">**Get-AzLoadBalancerProbeConfig** cmdlet은 부하 분산에 대한 하나 이상의 프로브 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="f8fec-107">예제</span><span class="sxs-lookup"><span data-stu-id="f8fec-107">EXAMPLES</span></span>

### <span data-ttu-id="f8fec-108">예제 1: 부하 균형 조정의 프로브 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="f8fec-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="f8fec-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="f8fec-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f8fec-110">두 번째 명령은 MyProbe라는 연결된 프로브 구성을 $slb.</span><span class="sxs-lookup"><span data-stu-id="f8fec-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="f8fec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8fec-111">PARAMETERS</span></span>

### <span data-ttu-id="f8fec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fec-112">-DefaultProfile</span></span>
<span data-ttu-id="f8fec-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fec-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8fec-114">-LoadBalancer</span></span>
<span data-ttu-id="f8fec-115">얻을 프로브 구성과 연결된 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="f8fec-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f8fec-116">-Name</span></span>
<span data-ttu-id="f8fec-117">얻을 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="f8fec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fec-118">CommonParameters</span></span>
<span data-ttu-id="f8fec-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fec-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8fec-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fec-121">입력</span><span class="sxs-lookup"><span data-stu-id="f8fec-121">INPUTS</span></span>

### <span data-ttu-id="f8fec-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8fec-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8fec-123">출력</span><span class="sxs-lookup"><span data-stu-id="f8fec-123">OUTPUTS</span></span>

### <span data-ttu-id="f8fec-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="f8fec-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f8fec-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8fec-125">NOTES</span></span>

## <span data-ttu-id="f8fec-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8fec-126">RELATED LINKS</span></span>

[<span data-ttu-id="f8fec-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f8fec-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f8fec-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8fec-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f8fec-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f8fec-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f8fec-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f8fec-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f8fec-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f8fec-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


