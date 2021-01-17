---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365548"
---
# <span data-ttu-id="018b8-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="018b8-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="018b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018b8-102">SYNOPSIS</span></span>
<span data-ttu-id="018b8-103">Get-AzLoadBalancerBackendAddressPool 부하 균형 조정과 연결된 하나 이상의 백드 주소 풀을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="018b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="018b8-104">SYNTAX</span></span>

### <span data-ttu-id="018b8-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="018b8-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="018b8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="018b8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="018b8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="018b8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="018b8-108">설명</span><span class="sxs-lookup"><span data-stu-id="018b8-108">DESCRIPTION</span></span>
<span data-ttu-id="018b8-109">Get-AzLoadBalancerBackendAddressPool 부하 균형 조정과 연결된 하나 이상의 백드 주소 풀을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="018b8-110">예제</span><span class="sxs-lookup"><span data-stu-id="018b8-110">EXAMPLES</span></span>

### <span data-ttu-id="018b8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="018b8-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="018b8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="018b8-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="018b8-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="018b8-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="018b8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="018b8-114">PARAMETERS</span></span>

### <span data-ttu-id="018b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018b8-115">-DefaultProfile</span></span>
<span data-ttu-id="018b8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018b8-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="018b8-117">-LoadBalancer</span></span>
<span data-ttu-id="018b8-118">{{ LoadBalancer 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="018b8-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="018b8-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="018b8-119">-LoadBalancerName</span></span>
<span data-ttu-id="018b8-120">부하 균형 조정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="018b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="018b8-121">-Name</span></span>
<span data-ttu-id="018b8-122">백end 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="018b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="018b8-124">부하 균형 조정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="018b8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="018b8-125">-ResourceId</span></span>

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

### <span data-ttu-id="018b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018b8-126">CommonParameters</span></span>
<span data-ttu-id="018b8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="018b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018b8-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="018b8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018b8-129">입력</span><span class="sxs-lookup"><span data-stu-id="018b8-129">INPUTS</span></span>

### <span data-ttu-id="018b8-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="018b8-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="018b8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="018b8-131">System.String</span></span>

## <span data-ttu-id="018b8-132">출력</span><span class="sxs-lookup"><span data-stu-id="018b8-132">OUTPUTS</span></span>

### <span data-ttu-id="018b8-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="018b8-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="018b8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="018b8-134">NOTES</span></span>

## <span data-ttu-id="018b8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="018b8-135">RELATED LINKS</span></span>
