---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a337446238807f3a6408d0c9b68034e4a245eb48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956811"
---
# <span data-ttu-id="a0625-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a0625-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a0625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0625-102">SYNOPSIS</span></span>
<span data-ttu-id="a0625-103">부하 저울에 대한 백던드 주소 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="a0625-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0625-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0625-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0625-105">DESCRIPTION</span></span>
<span data-ttu-id="a0625-106">**Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet은 단일 백end 주소 풀 또는 부하 분산기 내의 백end 주소 풀 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="a0625-107">예제</span><span class="sxs-lookup"><span data-stu-id="a0625-107">EXAMPLES</span></span>

### <span data-ttu-id="a0625-108">예제 1: 백던드 주소 풀을 얻다</span><span class="sxs-lookup"><span data-stu-id="a0625-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a0625-109">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyLoadBalancer라는 기존 부하 분산 장치 $loadbalancer 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a0625-110">두 번째 명령은 2018년의 부하 균형 조정기에 대해 BackendAddressPool02라는 연결된 백end 주소 풀 구성을 $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a0625-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a0625-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0625-111">PARAMETERS</span></span>

### <span data-ttu-id="a0625-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0625-112">-DefaultProfile</span></span>
<span data-ttu-id="a0625-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0625-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a0625-114">-LoadBalancer</span></span>
<span data-ttu-id="a0625-115">얻을 백end 주소 풀과 연결된 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="a0625-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a0625-116">-Name</span></span>
<span data-ttu-id="a0625-117">얻을 백던드 주소 풀을 포함하는 부하 균형 조정기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="a0625-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0625-118">CommonParameters</span></span>
<span data-ttu-id="a0625-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0625-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0625-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0625-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0625-121">입력</span><span class="sxs-lookup"><span data-stu-id="a0625-121">INPUTS</span></span>

### <span data-ttu-id="a0625-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a0625-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a0625-123">출력</span><span class="sxs-lookup"><span data-stu-id="a0625-123">OUTPUTS</span></span>

### <span data-ttu-id="a0625-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a0625-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a0625-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0625-125">NOTES</span></span>

## <span data-ttu-id="a0625-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0625-126">RELATED LINKS</span></span>

[<span data-ttu-id="a0625-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a0625-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a0625-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a0625-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a0625-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a0625-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a0625-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a0625-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


