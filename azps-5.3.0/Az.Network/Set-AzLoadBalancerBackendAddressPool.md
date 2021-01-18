---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496519"
---
# <span data-ttu-id="4188c-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4188c-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="4188c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4188c-102">SYNOPSIS</span></span>
<span data-ttu-id="4188c-103">부하 분산기에서 백end 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="4188c-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="4188c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4188c-104">SYNTAX</span></span>

### <span data-ttu-id="4188c-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4188c-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4188c-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4188c-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4188c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4188c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4188c-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4188c-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4188c-109">설명</span><span class="sxs-lookup"><span data-stu-id="4188c-109">DESCRIPTION</span></span>
<span data-ttu-id="4188c-110">부하 분산기에서 백end 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="4188c-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="4188c-111">예제</span><span class="sxs-lookup"><span data-stu-id="4188c-111">EXAMPLES</span></span>

### <span data-ttu-id="4188c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4188c-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="4188c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4188c-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="4188c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="4188c-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="4188c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4188c-115">PARAMETERS</span></span>

### <span data-ttu-id="4188c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4188c-116">-DefaultProfile</span></span>
<span data-ttu-id="4188c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4188c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4188c-118">-Force</span></span>
<span data-ttu-id="4188c-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4188c-120">-InputObject</span></span>
<span data-ttu-id="4188c-121">설정할 백end 주소 풀</span><span class="sxs-lookup"><span data-stu-id="4188c-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4188c-122">-LoadBalancer</span></span>
<span data-ttu-id="4188c-123">부하 균형 조정기 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="4188c-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="4188c-125">백end 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="4188c-126">-LoadBalancerName</span></span>
<span data-ttu-id="4188c-127">부하 균형 조정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4188c-128">-Name</span></span>
<span data-ttu-id="4188c-129">백end 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4188c-130">-PassThru</span></span>
<span data-ttu-id="4188c-131">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="4188c-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4188c-132">-ResourceGroupName</span></span>
<span data-ttu-id="4188c-133">부하 균형 조정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4188c-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4188c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4188c-135">-Confirm</span></span>
<span data-ttu-id="4188c-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4188c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4188c-137">-WhatIf</span></span>
<span data-ttu-id="4188c-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4188c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4188c-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4188c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4188c-140">CommonParameters</span></span>
<span data-ttu-id="4188c-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4188c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4188c-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4188c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4188c-143">입력</span><span class="sxs-lookup"><span data-stu-id="4188c-143">INPUTS</span></span>

### <span data-ttu-id="4188c-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4188c-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4188c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4188c-145">System.String</span></span>

## <span data-ttu-id="4188c-146">출력</span><span class="sxs-lookup"><span data-stu-id="4188c-146">OUTPUTS</span></span>

### <span data-ttu-id="4188c-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4188c-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="4188c-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4188c-148">NOTES</span></span>

## <span data-ttu-id="4188c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4188c-149">RELATED LINKS</span></span>
