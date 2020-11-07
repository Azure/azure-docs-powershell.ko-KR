---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699466"
---
# <span data-ttu-id="2ee03-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="2ee03-101">Search-AzGraph</span></span>

## <span data-ttu-id="2ee03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee03-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee03-103">Azure 리소스 관리자가 관리 하는 리소스를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="2ee03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ee03-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee03-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ee03-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee03-106">쿼리 구문에 대 한 자세한 내용은 다음을 참고 하세요. https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="2ee03-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="2ee03-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ee03-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee03-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ee03-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="2ee03-109">리소스 필드의 하위 집합을 요청 하는 단순 리소스 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="2ee03-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ee03-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="2ee03-111">필드 선택, 필터링 및 요약 기능을 갖춘 리소스에 대 한 복잡 한 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="2ee03-112">변수</span><span class="sxs-lookup"><span data-stu-id="2ee03-112">PARAMETERS</span></span>

### <span data-ttu-id="2ee03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee03-113">-DefaultProfile</span></span>
<span data-ttu-id="2ee03-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee03-115">-쿼리</span><span class="sxs-lookup"><span data-stu-id="2ee03-115">-Query</span></span>
<span data-ttu-id="2ee03-116">자원 그래프 쿼리.</span><span class="sxs-lookup"><span data-stu-id="2ee03-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee03-117">-구독</span><span class="sxs-lookup"><span data-stu-id="2ee03-117">-Subscription</span></span>
<span data-ttu-id="2ee03-118">쿼리를 실행할 대상 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee03-119">-생략</span><span class="sxs-lookup"><span data-stu-id="2ee03-119">-Skip</span></span>
<span data-ttu-id="2ee03-120">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee03-121">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="2ee03-121">-First</span></span>
<span data-ttu-id="2ee03-122">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-122">The maximum number of objects to return.</span></span> <span data-ttu-id="2ee03-123">허용 되는 값: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="2ee03-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="2ee03-124">기본값은 100입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee03-125">CommonParameters</span></span>
<span data-ttu-id="2ee03-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee03-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee03-128">입력</span><span class="sxs-lookup"><span data-stu-id="2ee03-128">INPUTS</span></span>

### <span data-ttu-id="2ee03-129">않아야</span><span class="sxs-lookup"><span data-stu-id="2ee03-129">None</span></span>

## <span data-ttu-id="2ee03-130">출력</span><span class="sxs-lookup"><span data-stu-id="2ee03-130">OUTPUTS</span></span>

### <span data-ttu-id="2ee03-131">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="2ee03-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2ee03-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2ee03-132">NOTES</span></span>

## <span data-ttu-id="2ee03-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ee03-133">RELATED LINKS</span></span>
