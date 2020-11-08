---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218259"
---
# <span data-ttu-id="d1de5-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1de5-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d1de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1de5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1de5-103">Loadbalancer에 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="d1de5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1de5-104">SYNTAX</span></span>

### <span data-ttu-id="d1de5-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1de5-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1de5-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1de5-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1de5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1de5-107">DESCRIPTION</span></span>
<span data-ttu-id="d1de5-108">Loadbalancer에 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="d1de5-109">PSLoadBalancerBackendAddress의 배열을 specifiying 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="d1de5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d1de5-110">EXAMPLES</span></span>

### <span data-ttu-id="d1de5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1de5-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="d1de5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d1de5-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="d1de5-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="d1de5-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="d1de5-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="d1de5-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="d1de5-115">변수</span><span class="sxs-lookup"><span data-stu-id="d1de5-115">PARAMETERS</span></span>

### <span data-ttu-id="d1de5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1de5-116">-DefaultProfile</span></span>
<span data-ttu-id="d1de5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1de5-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1de5-118">-LoadBalancer</span></span>
<span data-ttu-id="d1de5-119">부하 분산 장치 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="d1de5-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="d1de5-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="d1de5-121">백 엔드 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-121">The backend addresses.</span></span>

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

### <span data-ttu-id="d1de5-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d1de5-122">-LoadBalancerName</span></span>
<span data-ttu-id="d1de5-123">부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="d1de5-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d1de5-124">-Name</span></span>
<span data-ttu-id="d1de5-125">백 엔드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="d1de5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1de5-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1de5-127">부하 분산 장치의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="d1de5-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d1de5-128">-Confirm</span></span>
<span data-ttu-id="d1de5-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1de5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1de5-130">-WhatIf</span></span>
<span data-ttu-id="d1de5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1de5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1de5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1de5-133">CommonParameters</span></span>
<span data-ttu-id="d1de5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1de5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1de5-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1de5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1de5-136">입력</span><span class="sxs-lookup"><span data-stu-id="d1de5-136">INPUTS</span></span>

### <span data-ttu-id="d1de5-137">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1de5-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d1de5-138">출력</span><span class="sxs-lookup"><span data-stu-id="d1de5-138">OUTPUTS</span></span>

### <span data-ttu-id="d1de5-139">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d1de5-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d1de5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d1de5-140">NOTES</span></span>

## <span data-ttu-id="d1de5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1de5-141">RELATED LINKS</span></span>
