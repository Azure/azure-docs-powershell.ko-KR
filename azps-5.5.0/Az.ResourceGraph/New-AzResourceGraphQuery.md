---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176417"
---
# <span data-ttu-id="264da-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="264da-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="264da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="264da-102">SYNOPSIS</span></span>
<span data-ttu-id="264da-103">새 그래프 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="264da-103">Create a new graph query.</span></span>

## <span data-ttu-id="264da-104">구문</span><span class="sxs-lookup"><span data-stu-id="264da-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="264da-105">설명</span><span class="sxs-lookup"><span data-stu-id="264da-105">DESCRIPTION</span></span>
<span data-ttu-id="264da-106">새 그래프 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="264da-106">Create a new graph query.</span></span>

## <span data-ttu-id="264da-107">예제</span><span class="sxs-lookup"><span data-stu-id="264da-107">EXAMPLES</span></span>

### <span data-ttu-id="264da-108">예제 1: 쿼리 매개 변수를 사용하여 리소스 그래프 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="264da-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="264da-109">이 명령은 쿼리 매개 변수에 의해 리소스 그래프 쿼리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="264da-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="264da-110">예제 2: 파일 매개 변수로 리소스 그래프 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="264da-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="264da-111">이 명령은 파일 매개 변수에 의해 리소스 그래프 쿼리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="264da-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="264da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="264da-112">PARAMETERS</span></span>

### <span data-ttu-id="264da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264da-113">-DefaultProfile</span></span>
<span data-ttu-id="264da-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="264da-115">-Description</span><span class="sxs-lookup"><span data-stu-id="264da-115">-Description</span></span>
<span data-ttu-id="264da-116">그래프 쿼리에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="264da-117">-File</span><span class="sxs-lookup"><span data-stu-id="264da-117">-File</span></span>
<span data-ttu-id="264da-118">파일의 콘텐츠가 쿼리 매개 변수에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="264da-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="264da-119">-Location</span><span class="sxs-lookup"><span data-stu-id="264da-119">-Location</span></span>
<span data-ttu-id="264da-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="264da-120">The location of the resource</span></span>

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

### <span data-ttu-id="264da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="264da-121">-Name</span></span>
<span data-ttu-id="264da-122">그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="264da-123">-Query</span><span class="sxs-lookup"><span data-stu-id="264da-123">-Query</span></span>
<span data-ttu-id="264da-124">그래프가 될 KQL 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="264da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="264da-125">-ResourceGroupName</span></span>
<span data-ttu-id="264da-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="264da-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="264da-127">-SubscriptionId</span></span>
<span data-ttu-id="264da-128">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="264da-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="264da-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="264da-129">-Tag</span></span>
<span data-ttu-id="264da-130">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="264da-130">Resource tags</span></span>

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

### <span data-ttu-id="264da-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="264da-131">-Confirm</span></span>
<span data-ttu-id="264da-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="264da-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="264da-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="264da-133">-WhatIf</span></span>
<span data-ttu-id="264da-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="264da-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="264da-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="264da-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="264da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264da-136">CommonParameters</span></span>
<span data-ttu-id="264da-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="264da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264da-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="264da-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264da-139">입력</span><span class="sxs-lookup"><span data-stu-id="264da-139">INPUTS</span></span>

### <span data-ttu-id="264da-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="264da-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="264da-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="264da-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="264da-142">출력</span><span class="sxs-lookup"><span data-stu-id="264da-142">OUTPUTS</span></span>

### <span data-ttu-id="264da-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="264da-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="264da-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="264da-144">NOTES</span></span>

<span data-ttu-id="264da-145">별칭</span><span class="sxs-lookup"><span data-stu-id="264da-145">ALIASES</span></span>

## <span data-ttu-id="264da-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="264da-146">RELATED LINKS</span></span>

