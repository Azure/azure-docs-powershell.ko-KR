---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179652"
---
# <span data-ttu-id="63524-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63524-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="63524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63524-102">SYNOPSIS</span></span>
<span data-ttu-id="63524-103">부하 분산기에서 백end 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63524-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="63524-104">구문</span><span class="sxs-lookup"><span data-stu-id="63524-104">SYNTAX</span></span>

### <span data-ttu-id="63524-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63524-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63524-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63524-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63524-107">설명</span><span class="sxs-lookup"><span data-stu-id="63524-107">DESCRIPTION</span></span>
<span data-ttu-id="63524-108">부하 분산기에서 백end 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63524-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="63524-109">PSLoadBalancerBackendAddress의 배열을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="63524-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="63524-110">예제</span><span class="sxs-lookup"><span data-stu-id="63524-110">EXAMPLES</span></span>

### <span data-ttu-id="63524-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="63524-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="63524-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="63524-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="63524-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="63524-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="63524-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="63524-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="63524-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63524-115">PARAMETERS</span></span>

### <span data-ttu-id="63524-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63524-116">-DefaultProfile</span></span>
<span data-ttu-id="63524-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63524-118">-LoadBalancer</span></span>
<span data-ttu-id="63524-119">부하 균형 조정기 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63524-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="63524-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="63524-121">백end 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="63524-122">-LoadBalancerName</span></span>
<span data-ttu-id="63524-123">부하 균형 조정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-124">-Name</span><span class="sxs-lookup"><span data-stu-id="63524-124">-Name</span></span>
<span data-ttu-id="63524-125">백end 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63524-126">-ResourceGroupName</span></span>
<span data-ttu-id="63524-127">부하 균형 조정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63524-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63524-128">-Confirm</span></span>
<span data-ttu-id="63524-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63524-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63524-130">-WhatIf</span></span>
<span data-ttu-id="63524-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="63524-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63524-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63524-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63524-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63524-133">CommonParameters</span></span>
<span data-ttu-id="63524-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63524-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63524-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63524-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63524-136">입력</span><span class="sxs-lookup"><span data-stu-id="63524-136">INPUTS</span></span>

### <span data-ttu-id="63524-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63524-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="63524-138">출력</span><span class="sxs-lookup"><span data-stu-id="63524-138">OUTPUTS</span></span>

### <span data-ttu-id="63524-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63524-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="63524-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63524-140">NOTES</span></span>

## <span data-ttu-id="63524-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63524-141">RELATED LINKS</span></span>
