---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216077"
---
# <span data-ttu-id="9aced-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9aced-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="9aced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aced-102">SYNOPSIS</span></span>
<span data-ttu-id="9aced-103">부하 분산 장치에서 백 엔드 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="9aced-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aced-104">SYNTAX</span></span>

### <span data-ttu-id="9aced-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aced-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aced-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aced-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9aced-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aced-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aced-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aced-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aced-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9aced-109">DESCRIPTION</span></span>
<span data-ttu-id="9aced-110">부하 분산 장치에서 백 엔드 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="9aced-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9aced-111">EXAMPLES</span></span>

### <span data-ttu-id="9aced-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9aced-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="9aced-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9aced-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="9aced-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="9aced-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="9aced-115">변수</span><span class="sxs-lookup"><span data-stu-id="9aced-115">PARAMETERS</span></span>

### <span data-ttu-id="9aced-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aced-116">-DefaultProfile</span></span>
<span data-ttu-id="9aced-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aced-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aced-118">-InputObject</span></span>
<span data-ttu-id="9aced-119">제거할 백 엔드 주소 풀</span><span class="sxs-lookup"><span data-stu-id="9aced-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="9aced-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9aced-120">-LoadBalancer</span></span>
<span data-ttu-id="9aced-121">부하 분산 장치 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="9aced-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="9aced-122">-LoadBalancerName</span></span>
<span data-ttu-id="9aced-123">부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="9aced-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9aced-124">-Name</span></span>
<span data-ttu-id="9aced-125">부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="9aced-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aced-126">-PassThru</span></span>
<span data-ttu-id="9aced-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="9aced-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9aced-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aced-128">-ResourceGroupName</span></span>
<span data-ttu-id="9aced-129">부하 분산 장치의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="9aced-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aced-130">-ResourceId</span></span>

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

### <span data-ttu-id="9aced-131">-확인</span><span class="sxs-lookup"><span data-stu-id="9aced-131">-Confirm</span></span>
<span data-ttu-id="9aced-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aced-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aced-133">-WhatIf</span></span>
<span data-ttu-id="9aced-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aced-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aced-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aced-136">CommonParameters</span></span>
<span data-ttu-id="9aced-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aced-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aced-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9aced-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aced-139">입력</span><span class="sxs-lookup"><span data-stu-id="9aced-139">INPUTS</span></span>

### <span data-ttu-id="9aced-140">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9aced-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9aced-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9aced-141">System.String</span></span>

## <span data-ttu-id="9aced-142">출력</span><span class="sxs-lookup"><span data-stu-id="9aced-142">OUTPUTS</span></span>

### <span data-ttu-id="9aced-143">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9aced-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9aced-144">상속자</span><span class="sxs-lookup"><span data-stu-id="9aced-144">NOTES</span></span>

## <span data-ttu-id="9aced-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aced-145">RELATED LINKS</span></span>
