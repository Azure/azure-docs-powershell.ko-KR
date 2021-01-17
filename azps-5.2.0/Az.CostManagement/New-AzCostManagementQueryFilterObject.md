---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336614"
---
# <span data-ttu-id="97683-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="97683-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="97683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97683-102">SYNOPSIS</span></span>
<span data-ttu-id="97683-103">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="97683-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="97683-104">구문</span><span class="sxs-lookup"><span data-stu-id="97683-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="97683-105">설명</span><span class="sxs-lookup"><span data-stu-id="97683-105">DESCRIPTION</span></span>
<span data-ttu-id="97683-106">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="97683-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="97683-107">예제</span><span class="sxs-lookup"><span data-stu-id="97683-107">EXAMPLES</span></span>

### <span data-ttu-id="97683-108">예제 1: 비용 관리 내보내기 쿼리의 필터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="97683-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="97683-109">이 명령은 비용 관리 내보내기 쿼리의 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97683-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="97683-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97683-110">PARAMETERS</span></span>

### <span data-ttu-id="97683-111">-And</span><span class="sxs-lookup"><span data-stu-id="97683-111">-And</span></span>
<span data-ttu-id="97683-112">논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-112">The logical "AND" expression.</span></span>
<span data-ttu-id="97683-113">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-113">Must have at least 2 items.</span></span>
<span data-ttu-id="97683-114">생성을 위해 AND 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="97683-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="97683-115">-Dimensions</span><span class="sxs-lookup"><span data-stu-id="97683-115">-Dimensions</span></span>
<span data-ttu-id="97683-116">차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="97683-117">생성을 위해 차원 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="97683-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="97683-118">-Not</span><span class="sxs-lookup"><span data-stu-id="97683-118">-Not</span></span>
<span data-ttu-id="97683-119">논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="97683-120">구성을 위해 NOT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="97683-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97683-121">-Or</span><span class="sxs-lookup"><span data-stu-id="97683-121">-Or</span></span>
<span data-ttu-id="97683-122">논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-122">The logical "OR" expression.</span></span>
<span data-ttu-id="97683-123">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-123">Must have at least 2 items.</span></span>
<span data-ttu-id="97683-124">구성을 위해 OR 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="97683-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="97683-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="97683-125">-Tag</span></span>
<span data-ttu-id="97683-126">태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="97683-127">생성을 위해 TAG 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="97683-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="97683-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97683-128">CommonParameters</span></span>
<span data-ttu-id="97683-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97683-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97683-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97683-131">입력</span><span class="sxs-lookup"><span data-stu-id="97683-131">INPUTS</span></span>

## <span data-ttu-id="97683-132">출력</span><span class="sxs-lookup"><span data-stu-id="97683-132">OUTPUTS</span></span>

### <span data-ttu-id="97683-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="97683-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="97683-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97683-134">NOTES</span></span>

<span data-ttu-id="97683-135">별칭</span><span class="sxs-lookup"><span data-stu-id="97683-135">ALIASES</span></span>

<span data-ttu-id="97683-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="97683-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97683-137">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97683-138">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97683-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97683-139">AND <IQueryFilter[]>: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="97683-140">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-141">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="97683-142">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-143">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="97683-144">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="97683-145">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="97683-146">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="97683-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="97683-147">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="97683-148">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="97683-149">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-150">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="97683-151">차원: <IQueryComparisonExpression> 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="97683-152">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="97683-153">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="97683-154">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="97683-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="97683-155">NOT: <IQueryFilter> 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="97683-156">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="97683-157">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-158">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="97683-159">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="97683-160">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="97683-161">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="97683-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="97683-162">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="97683-163">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="97683-164">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-165">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="97683-166">OR <IQueryFilter[]>: 논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="97683-167">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-168">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="97683-169">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-170">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="97683-171">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="97683-172">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="97683-173">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="97683-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="97683-174">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="97683-175">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="97683-176">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97683-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="97683-177">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="97683-178">TAG: <IQueryComparisonExpression> 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97683-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="97683-179">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="97683-180">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="97683-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="97683-181">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="97683-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="97683-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97683-182">RELATED LINKS</span></span>

