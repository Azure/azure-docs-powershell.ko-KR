---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181172"
---
# <span data-ttu-id="2ca52-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="2ca52-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="2ca52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca52-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca52-103">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2ca52-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="2ca52-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ca52-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="2ca52-105">설명</span><span class="sxs-lookup"><span data-stu-id="2ca52-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca52-106">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2ca52-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="2ca52-107">예제</span><span class="sxs-lookup"><span data-stu-id="2ca52-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca52-108">예제 1: 비용 관리 내보내기 쿼리의 비교 식 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="2ca52-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="2ca52-109">이 명령은 비용 관리 내보내기 쿼리의 비교 식 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ca52-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="2ca52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ca52-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca52-111">-Name</span><span class="sxs-lookup"><span data-stu-id="2ca52-111">-Name</span></span>
<span data-ttu-id="2ca52-112">비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ca52-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="2ca52-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="2ca52-113">-Operator</span></span>
<span data-ttu-id="2ca52-114">비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="2ca52-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="2ca52-115">-Value</span><span class="sxs-lookup"><span data-stu-id="2ca52-115">-Value</span></span>
<span data-ttu-id="2ca52-116">비교에 사용할 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2ca52-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="2ca52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca52-117">CommonParameters</span></span>
<span data-ttu-id="2ca52-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca52-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ca52-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca52-120">입력</span><span class="sxs-lookup"><span data-stu-id="2ca52-120">INPUTS</span></span>

## <span data-ttu-id="2ca52-121">출력</span><span class="sxs-lookup"><span data-stu-id="2ca52-121">OUTPUTS</span></span>

### <span data-ttu-id="2ca52-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="2ca52-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="2ca52-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ca52-123">NOTES</span></span>

<span data-ttu-id="2ca52-124">별칭</span><span class="sxs-lookup"><span data-stu-id="2ca52-124">ALIASES</span></span>

## <span data-ttu-id="2ca52-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ca52-125">RELATED LINKS</span></span>

