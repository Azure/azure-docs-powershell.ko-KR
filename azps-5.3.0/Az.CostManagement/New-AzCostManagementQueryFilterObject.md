---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495726"
---
# <span data-ttu-id="9959a-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="9959a-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="9959a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9959a-102">SYNOPSIS</span></span>
<span data-ttu-id="9959a-103">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9959a-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="9959a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9959a-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="9959a-105">설명</span><span class="sxs-lookup"><span data-stu-id="9959a-105">DESCRIPTION</span></span>
<span data-ttu-id="9959a-106">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9959a-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="9959a-107">예제</span><span class="sxs-lookup"><span data-stu-id="9959a-107">EXAMPLES</span></span>

### <span data-ttu-id="9959a-108">예제 1: 비용 관리 내보내기 쿼리의 필터 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="9959a-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="9959a-109">이 명령은 비용 관리 내보내기 쿼리의 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="9959a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9959a-110">PARAMETERS</span></span>

### <span data-ttu-id="9959a-111">-And</span><span class="sxs-lookup"><span data-stu-id="9959a-111">-And</span></span>
<span data-ttu-id="9959a-112">논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-112">The logical "AND" expression.</span></span>
<span data-ttu-id="9959a-113">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-113">Must have at least 2 items.</span></span>
<span data-ttu-id="9959a-114">생성을 위해 AND 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9959a-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="9959a-115">-Dimensions</span><span class="sxs-lookup"><span data-stu-id="9959a-115">-Dimensions</span></span>
<span data-ttu-id="9959a-116">차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="9959a-117">생성을 위해 차원 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9959a-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="9959a-118">-Not</span><span class="sxs-lookup"><span data-stu-id="9959a-118">-Not</span></span>
<span data-ttu-id="9959a-119">논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="9959a-120">구성을 위해 NOT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9959a-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9959a-121">-Or</span><span class="sxs-lookup"><span data-stu-id="9959a-121">-Or</span></span>
<span data-ttu-id="9959a-122">논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-122">The logical "OR" expression.</span></span>
<span data-ttu-id="9959a-123">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-123">Must have at least 2 items.</span></span>
<span data-ttu-id="9959a-124">구성을 위해 OR 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9959a-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="9959a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9959a-125">-Tag</span></span>
<span data-ttu-id="9959a-126">태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="9959a-127">생성을 위해 TAG 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9959a-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="9959a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9959a-128">CommonParameters</span></span>
<span data-ttu-id="9959a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9959a-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9959a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9959a-131">입력</span><span class="sxs-lookup"><span data-stu-id="9959a-131">INPUTS</span></span>

## <span data-ttu-id="9959a-132">출력</span><span class="sxs-lookup"><span data-stu-id="9959a-132">OUTPUTS</span></span>

### <span data-ttu-id="9959a-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="9959a-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="9959a-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9959a-134">NOTES</span></span>

<span data-ttu-id="9959a-135">별칭</span><span class="sxs-lookup"><span data-stu-id="9959a-135">ALIASES</span></span>

<span data-ttu-id="9959a-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9959a-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9959a-137">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9959a-138">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9959a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9959a-139">AND <IQueryFilter[]>: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="9959a-140">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-141">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9959a-142">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-143">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9959a-144">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9959a-145">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="9959a-146">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="9959a-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9959a-147">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9959a-148">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9959a-149">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-150">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9959a-151">차원: <IQueryComparisonExpression> 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="9959a-152">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="9959a-153">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="9959a-154">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="9959a-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="9959a-155">NOT: <IQueryFilter> 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9959a-156">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9959a-157">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-158">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9959a-159">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9959a-160">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="9959a-161">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="9959a-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9959a-162">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9959a-163">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9959a-164">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-165">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9959a-166">OR <IQueryFilter[]>: 논리 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="9959a-167">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-168">`[And <IQueryFilter[]>]`: 논리 "AND" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="9959a-169">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-170">`[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="9959a-171">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="9959a-172">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="9959a-173">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="9959a-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="9959a-174">`[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="9959a-175">`[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="9959a-176">항목이 2개 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="9959a-177">`[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="9959a-178">TAG: <IQueryComparisonExpression> 태그에 대한 비교 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="9959a-179">`Name <String>`: 비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="9959a-180">`Operator <OperatorType>`: 비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="9959a-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="9959a-181">`Value <String[]>`: 비교에 사용할 값의 배열</span><span class="sxs-lookup"><span data-stu-id="9959a-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="9959a-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9959a-182">RELATED LINKS</span></span>

