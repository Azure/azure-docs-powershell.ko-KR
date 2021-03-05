---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998172"
---
# <span data-ttu-id="20649-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="20649-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="20649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20649-102">SYNOPSIS</span></span>
<span data-ttu-id="20649-103">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="20649-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="20649-104">구문</span><span class="sxs-lookup"><span data-stu-id="20649-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="20649-105">설명</span><span class="sxs-lookup"><span data-stu-id="20649-105">DESCRIPTION</span></span>
<span data-ttu-id="20649-106">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="20649-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="20649-107">예제</span><span class="sxs-lookup"><span data-stu-id="20649-107">EXAMPLES</span></span>

### <span data-ttu-id="20649-108">예제 1: 비용 관리 내보내기 쿼리의 비교 식 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="20649-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="20649-109">이 명령은 비용 관리 내보내기에 대한 쿼리의 비교 식 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20649-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="20649-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20649-110">PARAMETERS</span></span>

### <span data-ttu-id="20649-111">-Name</span><span class="sxs-lookup"><span data-stu-id="20649-111">-Name</span></span>
<span data-ttu-id="20649-112">비교하여 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20649-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="20649-113">-연산자</span><span class="sxs-lookup"><span data-stu-id="20649-113">-Operator</span></span>
<span data-ttu-id="20649-114">비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="20649-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20649-115">-Value</span><span class="sxs-lookup"><span data-stu-id="20649-115">-Value</span></span>
<span data-ttu-id="20649-116">비교에 사용할 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="20649-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20649-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20649-117">CommonParameters</span></span>
<span data-ttu-id="20649-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20649-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20649-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20649-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20649-120">입력</span><span class="sxs-lookup"><span data-stu-id="20649-120">INPUTS</span></span>

## <span data-ttu-id="20649-121">출력</span><span class="sxs-lookup"><span data-stu-id="20649-121">OUTPUTS</span></span>

### <span data-ttu-id="20649-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="20649-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="20649-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20649-123">NOTES</span></span>

<span data-ttu-id="20649-124">별칭</span><span class="sxs-lookup"><span data-stu-id="20649-124">ALIASES</span></span>

## <span data-ttu-id="20649-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20649-125">RELATED LINKS</span></span>

