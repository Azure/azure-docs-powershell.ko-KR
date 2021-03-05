---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 6e12cc4bb296a1c523547aebc44c6992dd2b687e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993701"
---
# <span data-ttu-id="e7c95-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7c95-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="e7c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c95-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c95-103">부하 균형 조정기에서 백던드 풀 제거</span><span class="sxs-lookup"><span data-stu-id="e7c95-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="e7c95-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7c95-104">SYNTAX</span></span>

### <span data-ttu-id="e7c95-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c95-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7c95-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c95-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7c95-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c95-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7c95-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c95-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c95-109">설명</span><span class="sxs-lookup"><span data-stu-id="e7c95-109">DESCRIPTION</span></span>
<span data-ttu-id="e7c95-110">부하 균형 조정기에서 백던드 풀 제거</span><span class="sxs-lookup"><span data-stu-id="e7c95-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="e7c95-111">예제</span><span class="sxs-lookup"><span data-stu-id="e7c95-111">EXAMPLES</span></span>

### <span data-ttu-id="e7c95-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7c95-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="e7c95-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e7c95-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="e7c95-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="e7c95-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="e7c95-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7c95-115">PARAMETERS</span></span>

### <span data-ttu-id="e7c95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c95-116">-DefaultProfile</span></span>
<span data-ttu-id="e7c95-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7c95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7c95-118">-InputObject</span></span>
<span data-ttu-id="e7c95-119">제거할 백end 주소 풀</span><span class="sxs-lookup"><span data-stu-id="e7c95-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7c95-120">-LoadBalancer</span></span>
<span data-ttu-id="e7c95-121">부하 균형 조정기 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="e7c95-122">-LoadBalancerName</span></span>
<span data-ttu-id="e7c95-123">부하 균형 조정기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e7c95-124">-Name</span></span>
<span data-ttu-id="e7c95-125">부하 균형 조정기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7c95-126">-PassThru</span></span>
<span data-ttu-id="e7c95-127">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="e7c95-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e7c95-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c95-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7c95-129">부하 균형 조정기의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c95-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c95-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e7c95-131">-Confirm</span></span>
<span data-ttu-id="e7c95-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7c95-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c95-133">-WhatIf</span></span>
<span data-ttu-id="e7c95-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c95-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7c95-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c95-136">CommonParameters</span></span>
<span data-ttu-id="e7c95-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c95-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7c95-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c95-139">입력</span><span class="sxs-lookup"><span data-stu-id="e7c95-139">INPUTS</span></span>

### <span data-ttu-id="e7c95-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7c95-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e7c95-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e7c95-141">System.String</span></span>

## <span data-ttu-id="e7c95-142">출력</span><span class="sxs-lookup"><span data-stu-id="e7c95-142">OUTPUTS</span></span>

### <span data-ttu-id="e7c95-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7c95-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e7c95-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7c95-144">NOTES</span></span>

## <span data-ttu-id="e7c95-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7c95-145">RELATED LINKS</span></span>
