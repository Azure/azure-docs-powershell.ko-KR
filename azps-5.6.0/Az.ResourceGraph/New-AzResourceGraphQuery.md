---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: c20e7c63fac01459d3df9d417b0fcec6aed83d36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000139"
---
# <span data-ttu-id="da714-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="da714-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="da714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da714-102">SYNOPSIS</span></span>
<span data-ttu-id="da714-103">새 그래프 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da714-103">Create a new graph query.</span></span>

## <span data-ttu-id="da714-104">구문</span><span class="sxs-lookup"><span data-stu-id="da714-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da714-105">설명</span><span class="sxs-lookup"><span data-stu-id="da714-105">DESCRIPTION</span></span>
<span data-ttu-id="da714-106">새 그래프 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da714-106">Create a new graph query.</span></span>

## <span data-ttu-id="da714-107">예제</span><span class="sxs-lookup"><span data-stu-id="da714-107">EXAMPLES</span></span>

### <span data-ttu-id="da714-108">예제 1: 쿼리 매개 변수에 의해 리소스 그래프 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="da714-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="da714-109">이 명령은 쿼리 매개 변수에 따라 리소스 그래프 쿼리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da714-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="da714-110">예제 2: 파일 매개 변수에 의해 리소스 그래프 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="da714-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="da714-111">이 명령은 파일 매개 변수에 따라 리소스 그래프 쿼리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da714-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="da714-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="da714-112">PARAMETERS</span></span>

### <span data-ttu-id="da714-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da714-113">-DefaultProfile</span></span>
<span data-ttu-id="da714-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-115">-Description</span><span class="sxs-lookup"><span data-stu-id="da714-115">-Description</span></span>
<span data-ttu-id="da714-116">그래프 쿼리에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-116">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-117">-File</span><span class="sxs-lookup"><span data-stu-id="da714-117">-File</span></span>
<span data-ttu-id="da714-118">파일의 콘텐츠가 쿼리 매개 변수에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="da714-118">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-119">-Location</span><span class="sxs-lookup"><span data-stu-id="da714-119">-Location</span></span>
<span data-ttu-id="da714-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="da714-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-121">-Name</span><span class="sxs-lookup"><span data-stu-id="da714-121">-Name</span></span>
<span data-ttu-id="da714-122">그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-122">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-123">-쿼리</span><span class="sxs-lookup"><span data-stu-id="da714-123">-Query</span></span>
<span data-ttu-id="da714-124">그래프가 될 KQL 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-124">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da714-125">-ResourceGroupName</span></span>
<span data-ttu-id="da714-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da714-127">-SubscriptionId</span></span>
<span data-ttu-id="da714-128">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="da714-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="da714-129">-Tag</span></span>
<span data-ttu-id="da714-130">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="da714-130">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-131">-확인</span><span class="sxs-lookup"><span data-stu-id="da714-131">-Confirm</span></span>
<span data-ttu-id="da714-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da714-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da714-133">-WhatIf</span></span>
<span data-ttu-id="da714-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="da714-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da714-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da714-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da714-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da714-136">CommonParameters</span></span>
<span data-ttu-id="da714-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da714-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da714-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da714-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da714-139">입력</span><span class="sxs-lookup"><span data-stu-id="da714-139">INPUTS</span></span>

### <span data-ttu-id="da714-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="da714-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="da714-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="da714-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="da714-142">출력</span><span class="sxs-lookup"><span data-stu-id="da714-142">OUTPUTS</span></span>

### <span data-ttu-id="da714-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="da714-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="da714-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da714-144">NOTES</span></span>

<span data-ttu-id="da714-145">별칭</span><span class="sxs-lookup"><span data-stu-id="da714-145">ALIASES</span></span>

## <span data-ttu-id="da714-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da714-146">RELATED LINKS</span></span>

