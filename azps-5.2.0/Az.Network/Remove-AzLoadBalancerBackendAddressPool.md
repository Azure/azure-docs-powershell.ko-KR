---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322321"
---
# <span data-ttu-id="61ddc-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61ddc-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="61ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="61ddc-103">부하 균형 조정기에서 백end 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="61ddc-104">구문</span><span class="sxs-lookup"><span data-stu-id="61ddc-104">SYNTAX</span></span>

### <span data-ttu-id="61ddc-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61ddc-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ddc-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61ddc-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61ddc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61ddc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ddc-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61ddc-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ddc-109">설명</span><span class="sxs-lookup"><span data-stu-id="61ddc-109">DESCRIPTION</span></span>
<span data-ttu-id="61ddc-110">부하 균형 조정기에서 백end 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="61ddc-111">예제</span><span class="sxs-lookup"><span data-stu-id="61ddc-111">EXAMPLES</span></span>

### <span data-ttu-id="61ddc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="61ddc-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="61ddc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="61ddc-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="61ddc-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="61ddc-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="61ddc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ddc-115">PARAMETERS</span></span>

### <span data-ttu-id="61ddc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ddc-116">-DefaultProfile</span></span>
<span data-ttu-id="61ddc-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ddc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61ddc-118">-InputObject</span></span>
<span data-ttu-id="61ddc-119">제거할 백end 주소 풀</span><span class="sxs-lookup"><span data-stu-id="61ddc-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="61ddc-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61ddc-120">-LoadBalancer</span></span>
<span data-ttu-id="61ddc-121">부하 균형 조정기 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="61ddc-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="61ddc-122">-LoadBalancerName</span></span>
<span data-ttu-id="61ddc-123">부하 균형 조정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="61ddc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61ddc-124">-Name</span></span>
<span data-ttu-id="61ddc-125">부하 균형 조정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="61ddc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ddc-126">-PassThru</span></span>
<span data-ttu-id="61ddc-127">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="61ddc-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="61ddc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ddc-128">-ResourceGroupName</span></span>
<span data-ttu-id="61ddc-129">부하 균형 조정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="61ddc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61ddc-130">-ResourceId</span></span>

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

### <span data-ttu-id="61ddc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61ddc-131">-Confirm</span></span>
<span data-ttu-id="61ddc-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ddc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ddc-133">-WhatIf</span></span>
<span data-ttu-id="61ddc-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61ddc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ddc-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ddc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ddc-136">CommonParameters</span></span>
<span data-ttu-id="61ddc-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61ddc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ddc-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61ddc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ddc-139">입력</span><span class="sxs-lookup"><span data-stu-id="61ddc-139">INPUTS</span></span>

### <span data-ttu-id="61ddc-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61ddc-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="61ddc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="61ddc-141">System.String</span></span>

## <span data-ttu-id="61ddc-142">출력</span><span class="sxs-lookup"><span data-stu-id="61ddc-142">OUTPUTS</span></span>

### <span data-ttu-id="61ddc-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61ddc-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="61ddc-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61ddc-144">NOTES</span></span>

## <span data-ttu-id="61ddc-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61ddc-145">RELATED LINKS</span></span>
