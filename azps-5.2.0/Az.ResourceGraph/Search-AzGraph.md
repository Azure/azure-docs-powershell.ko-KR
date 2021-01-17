---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362629"
---
# <span data-ttu-id="16248-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="16248-101">Search-AzGraph</span></span>

## <span data-ttu-id="16248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16248-102">SYNOPSIS</span></span>
<span data-ttu-id="16248-103">Azure Resource Manager에서 관리하는 리소스를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="16248-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="16248-104">구문</span><span class="sxs-lookup"><span data-stu-id="16248-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16248-105">설명</span><span class="sxs-lookup"><span data-stu-id="16248-105">DESCRIPTION</span></span>
<span data-ttu-id="16248-106">다음에서 쿼리 구문에 대해 자세히 알아보십시오. https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="16248-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="16248-107">예제</span><span class="sxs-lookup"><span data-stu-id="16248-107">EXAMPLES</span></span>

### <span data-ttu-id="16248-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="16248-108">Example 1</span></span>
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

<span data-ttu-id="16248-109">단순 리소스는 리소스 필드의 하위 집합을 요청하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="16248-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="16248-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="16248-111">필드 선택, 필터링 및 요약을 특징으로 하는 리소스에 대한 복잡한 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="16248-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="16248-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="16248-113">Managed Disks를 사용하지 않는 모든 가상 머신과 구독 표시 이름을 포함하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="16248-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="16248-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="16248-115">테넌트 및 구독 표시 이름에 의해 리소스 수를 표시하는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="16248-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16248-116">PARAMETERS</span></span>

### <span data-ttu-id="16248-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16248-117">-DefaultProfile</span></span>
<span data-ttu-id="16248-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16248-119">-Query</span><span class="sxs-lookup"><span data-stu-id="16248-119">-Query</span></span>
<span data-ttu-id="16248-120">Resource Graph 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="16248-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="16248-121">-Subscription</span></span>
<span data-ttu-id="16248-122">쿼리를 실행할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="16248-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="16248-123">-Skip</span></span>
<span data-ttu-id="16248-124">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="16248-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="16248-125">-First</span><span class="sxs-lookup"><span data-stu-id="16248-125">-First</span></span>
<span data-ttu-id="16248-126">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-126">The maximum number of objects to return.</span></span> <span data-ttu-id="16248-127">허용되는 값: 1-5000</span><span class="sxs-lookup"><span data-stu-id="16248-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="16248-128">기본값은 100입니다.</span><span class="sxs-lookup"><span data-stu-id="16248-128">Default value is 100.</span></span>

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

### <span data-ttu-id="16248-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16248-129">CommonParameters</span></span>
<span data-ttu-id="16248-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16248-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16248-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16248-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16248-132">입력</span><span class="sxs-lookup"><span data-stu-id="16248-132">INPUTS</span></span>

### <span data-ttu-id="16248-133">없음</span><span class="sxs-lookup"><span data-stu-id="16248-133">None</span></span>

## <span data-ttu-id="16248-134">출력</span><span class="sxs-lookup"><span data-stu-id="16248-134">OUTPUTS</span></span>

### <span data-ttu-id="16248-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="16248-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="16248-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16248-136">NOTES</span></span>

## <span data-ttu-id="16248-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16248-137">RELATED LINKS</span></span>
