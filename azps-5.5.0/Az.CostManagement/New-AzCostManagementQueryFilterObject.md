---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196676"
---
# <span data-ttu-id="86bfd-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="86bfd-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="86bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="86bfd-103">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="86bfd-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="86bfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="86bfd-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="86bfd-105">설명</span><span class="sxs-lookup"><span data-stu-id="86bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="86bfd-106">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="86bfd-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="86bfd-107">예제</span><span class="sxs-lookup"><span data-stu-id="86bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="86bfd-108">예제 1: 비용 관리 내보내기 쿼리의 필터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="86bfd-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="86bfd-109">이 명령은 비용 관리 내보내기 쿼리의 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="86bfd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86bfd-110">PARAMETERS</span></span>

### <span data-ttu-id="86bfd-111">-And</span><span class="sxs-lookup"><span data-stu-id="86bfd-111">-And</span></span>
<span data-ttu-id="86bfd-112">논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-112">The logical "AND" expression.</span></span>
<span data-ttu-id="86bfd-113">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-113">Must have at least 2 items.</span></span>
<span data-ttu-id="86bfd-114">생성을 위해 AND 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86bfd-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfd-115">-Dimensions</span><span class="sxs-lookup"><span data-stu-id="86bfd-115">-Dimensions</span></span>
<span data-ttu-id="86bfd-116">차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="86bfd-117">생성을 위해 차원 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86bfd-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfd-118">-Not</span><span class="sxs-lookup"><span data-stu-id="86bfd-118">-Not</span></span>
<span data-ttu-id="86bfd-119">논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="86bfd-120">구성을 위해 NOT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86bfd-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfd-121">-Or</span><span class="sxs-lookup"><span data-stu-id="86bfd-121">-Or</span></span>
<span data-ttu-id="86bfd-122">논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-122">The logical "OR" expression.</span></span>
<span data-ttu-id="86bfd-123">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-123">Must have at least 2 items.</span></span>
<span data-ttu-id="86bfd-124">구성을 위해 OR 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86bfd-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfd-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="86bfd-125">-Tag</span></span>
<span data-ttu-id="86bfd-126">태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="86bfd-127">생성을 위해 TAG 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86bfd-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86bfd-128">CommonParameters</span></span>
<span data-ttu-id="86bfd-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86bfd-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86bfd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86bfd-131">입력</span><span class="sxs-lookup"><span data-stu-id="86bfd-131">INPUTS</span></span>

## <span data-ttu-id="86bfd-132">출력</span><span class="sxs-lookup"><span data-stu-id="86bfd-132">OUTPUTS</span></span>

### <span data-ttu-id="86bfd-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="86bfd-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="86bfd-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86bfd-134">NOTES</span></span>

<span data-ttu-id="86bfd-135">별칭</span><span class="sxs-lookup"><span data-stu-id="86bfd-135">ALIASES</span></span>

<span data-ttu-id="86bfd-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="86bfd-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86bfd-137">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86bfd-138">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86bfd-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86bfd-139">AND <IQueryFilter[]>: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="86bfd-140">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-141">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="86bfd-142">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-143">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="86bfd-144">`Name <String>`: 비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="86bfd-145">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="86bfd-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="86bfd-146">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="86bfd-147">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="86bfd-148">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-149">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="86bfd-150">차원: <IQueryComparisonExpression> 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="86bfd-151">`Name <String>`: 비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="86bfd-152">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="86bfd-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="86bfd-153">NOT: <IQueryFilter> 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="86bfd-154">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="86bfd-155">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-156">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="86bfd-157">`Name <String>`: 비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="86bfd-158">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="86bfd-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="86bfd-159">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="86bfd-160">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="86bfd-161">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-162">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="86bfd-163">OR <IQueryFilter[]>: 논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="86bfd-164">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-165">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="86bfd-166">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-167">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="86bfd-168">`Name <String>`: 비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="86bfd-169">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="86bfd-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="86bfd-170">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="86bfd-171">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="86bfd-172">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="86bfd-173">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="86bfd-174">TAG: <IQueryComparisonExpression> 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="86bfd-175">`Name <String>`: 비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86bfd-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="86bfd-176">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="86bfd-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="86bfd-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86bfd-177">RELATED LINKS</span></span>

