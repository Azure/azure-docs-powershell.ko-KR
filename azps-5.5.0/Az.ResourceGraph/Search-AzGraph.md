---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176348"
---
# <span data-ttu-id="88378-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="88378-101">Search-AzGraph</span></span>

## <span data-ttu-id="88378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88378-102">SYNOPSIS</span></span>
<span data-ttu-id="88378-103">Azure Resource Manager에서 관리하는 리소스를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="88378-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="88378-104">구문</span><span class="sxs-lookup"><span data-stu-id="88378-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88378-105">설명</span><span class="sxs-lookup"><span data-stu-id="88378-105">DESCRIPTION</span></span>
<span data-ttu-id="88378-106">다음에서 쿼리 구문에 대해 자세히 알아보십시오. https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="88378-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="88378-107">예제</span><span class="sxs-lookup"><span data-stu-id="88378-107">EXAMPLES</span></span>

### <span data-ttu-id="88378-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="88378-108">Example 1</span></span>
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

<span data-ttu-id="88378-109">단순 리소스는 리소스 필드의 하위 집합을 요청하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="88378-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="88378-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="88378-111">필드 선택, 필터링 및 요약을 특징으로 하는 리소스에 대한 복잡한 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="88378-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="88378-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="88378-113">Managed Disks를 사용하지 않는 모든 가상 머신과 구독 표시 이름을 포함하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="88378-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="88378-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="88378-115">테넌트 및 구독 표시 이름에 의해 리소스 수를 표시하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="88378-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88378-116">PARAMETERS</span></span>

### <span data-ttu-id="88378-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88378-117">-DefaultProfile</span></span>
<span data-ttu-id="88378-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88378-119">-Query</span><span class="sxs-lookup"><span data-stu-id="88378-119">-Query</span></span>
<span data-ttu-id="88378-120">Resource Graph 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="88378-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="88378-121">-Subscription</span></span>
<span data-ttu-id="88378-122">쿼리를 실행할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="88378-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="88378-123">-Skip</span></span>
<span data-ttu-id="88378-124">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88378-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="88378-125">-First</span><span class="sxs-lookup"><span data-stu-id="88378-125">-First</span></span>
<span data-ttu-id="88378-126">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-126">The maximum number of objects to return.</span></span> <span data-ttu-id="88378-127">허용되는 값: 1-5000</span><span class="sxs-lookup"><span data-stu-id="88378-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="88378-128">기본값은 100입니다.</span><span class="sxs-lookup"><span data-stu-id="88378-128">Default value is 100.</span></span>

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

### <span data-ttu-id="88378-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88378-129">CommonParameters</span></span>
<span data-ttu-id="88378-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88378-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88378-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88378-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88378-132">입력</span><span class="sxs-lookup"><span data-stu-id="88378-132">INPUTS</span></span>

### <span data-ttu-id="88378-133">없음</span><span class="sxs-lookup"><span data-stu-id="88378-133">None</span></span>

## <span data-ttu-id="88378-134">출력</span><span class="sxs-lookup"><span data-stu-id="88378-134">OUTPUTS</span></span>

### <span data-ttu-id="88378-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="88378-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="88378-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88378-136">NOTES</span></span>

## <span data-ttu-id="88378-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88378-137">RELATED LINKS</span></span>
