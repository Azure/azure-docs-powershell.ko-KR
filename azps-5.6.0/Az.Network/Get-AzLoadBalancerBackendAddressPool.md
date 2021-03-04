---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956832"
---
# <span data-ttu-id="f98ef-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f98ef-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="f98ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f98ef-103">Get-AzLoadBalancerBackendAddressPool 균형 조정기와 연결된 하나 이상의 백던드 주소 풀을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="f98ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="f98ef-104">SYNTAX</span></span>

### <span data-ttu-id="f98ef-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ef-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f98ef-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ef-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f98ef-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ef-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f98ef-108">설명</span><span class="sxs-lookup"><span data-stu-id="f98ef-108">DESCRIPTION</span></span>
<span data-ttu-id="f98ef-109">Get-AzLoadBalancerBackendAddressPool 균형 조정기와 연결된 하나 이상의 백던드 주소 풀을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="f98ef-110">예제</span><span class="sxs-lookup"><span data-stu-id="f98ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f98ef-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f98ef-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="f98ef-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f98ef-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="f98ef-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="f98ef-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="f98ef-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f98ef-114">PARAMETERS</span></span>

### <span data-ttu-id="f98ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98ef-115">-DefaultProfile</span></span>
<span data-ttu-id="f98ef-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98ef-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f98ef-117">-LoadBalancer</span></span>
<span data-ttu-id="f98ef-118">{{ LoadBalancer 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="f98ef-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="f98ef-119">-LoadBalancerName</span></span>
<span data-ttu-id="f98ef-120">부하 균형 조정기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f98ef-121">-Name</span></span>
<span data-ttu-id="f98ef-122">백던드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="f98ef-124">부하 균형 조정기의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f98ef-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98ef-126">CommonParameters</span></span>
<span data-ttu-id="f98ef-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f98ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98ef-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f98ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98ef-129">입력</span><span class="sxs-lookup"><span data-stu-id="f98ef-129">INPUTS</span></span>

### <span data-ttu-id="f98ef-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f98ef-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f98ef-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f98ef-131">System.String</span></span>

## <span data-ttu-id="f98ef-132">출력</span><span class="sxs-lookup"><span data-stu-id="f98ef-132">OUTPUTS</span></span>

### <span data-ttu-id="f98ef-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f98ef-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f98ef-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f98ef-134">NOTES</span></span>

## <span data-ttu-id="f98ef-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f98ef-135">RELATED LINKS</span></span>
