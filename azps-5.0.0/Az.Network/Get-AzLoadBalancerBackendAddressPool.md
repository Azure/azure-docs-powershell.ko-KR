---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226211"
---
# <span data-ttu-id="d5890-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5890-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="d5890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5890-102">SYNOPSIS</span></span>
<span data-ttu-id="d5890-103">Get-AzLoadBalancerBackendAddressPool 부하 분산 장치와 연결 된 하나 이상의 백엔드 주소 풀을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="d5890-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5890-104">SYNTAX</span></span>

### <span data-ttu-id="d5890-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5890-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5890-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5890-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5890-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5890-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5890-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d5890-108">DESCRIPTION</span></span>
<span data-ttu-id="d5890-109">Get-AzLoadBalancerBackendAddressPool 부하 분산 장치와 연결 된 하나 이상의 백엔드 주소 풀을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="d5890-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5890-110">EXAMPLES</span></span>

### <span data-ttu-id="d5890-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5890-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="d5890-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d5890-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="d5890-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="d5890-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="d5890-114">변수</span><span class="sxs-lookup"><span data-stu-id="d5890-114">PARAMETERS</span></span>

### <span data-ttu-id="d5890-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5890-115">-DefaultProfile</span></span>
<span data-ttu-id="d5890-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5890-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5890-117">-LoadBalancer</span></span>
<span data-ttu-id="d5890-118">{{LoadBalancer 정보 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="d5890-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="d5890-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="d5890-119">-LoadBalancerName</span></span>
<span data-ttu-id="d5890-120">부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="d5890-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d5890-121">-Name</span></span>
<span data-ttu-id="d5890-122">백 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="d5890-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5890-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5890-124">부하 분산 장치의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="d5890-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5890-125">-ResourceId</span></span>

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

### <span data-ttu-id="d5890-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5890-126">CommonParameters</span></span>
<span data-ttu-id="d5890-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5890-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5890-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5890-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5890-129">입력</span><span class="sxs-lookup"><span data-stu-id="d5890-129">INPUTS</span></span>

### <span data-ttu-id="d5890-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5890-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d5890-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5890-131">System.String</span></span>

## <span data-ttu-id="d5890-132">출력</span><span class="sxs-lookup"><span data-stu-id="d5890-132">OUTPUTS</span></span>

### <span data-ttu-id="d5890-133">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d5890-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d5890-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d5890-134">NOTES</span></span>

## <span data-ttu-id="d5890-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5890-135">RELATED LINKS</span></span>
