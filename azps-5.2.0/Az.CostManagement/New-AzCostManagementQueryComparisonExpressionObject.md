---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336638"
---
# <span data-ttu-id="3573d-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="3573d-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="3573d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3573d-102">SYNOPSIS</span></span>
<span data-ttu-id="3573d-103">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3573d-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="3573d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3573d-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="3573d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3573d-105">DESCRIPTION</span></span>
<span data-ttu-id="3573d-106">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3573d-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="3573d-107">예제</span><span class="sxs-lookup"><span data-stu-id="3573d-107">EXAMPLES</span></span>

### <span data-ttu-id="3573d-108">예제 1: 비용 관리 내보내기 쿼리의 비교 식 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3573d-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="3573d-109">이 명령은 비용 관리 내보내기 쿼리의 비교 식 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3573d-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="3573d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3573d-110">PARAMETERS</span></span>

### <span data-ttu-id="3573d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="3573d-111">-Name</span></span>
<span data-ttu-id="3573d-112">비교에 사용할 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3573d-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="3573d-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="3573d-113">-Operator</span></span>
<span data-ttu-id="3573d-114">비교에 사용할 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="3573d-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="3573d-115">-Value</span><span class="sxs-lookup"><span data-stu-id="3573d-115">-Value</span></span>
<span data-ttu-id="3573d-116">비교에 사용할 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3573d-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="3573d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3573d-117">CommonParameters</span></span>
<span data-ttu-id="3573d-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3573d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3573d-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3573d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3573d-120">입력</span><span class="sxs-lookup"><span data-stu-id="3573d-120">INPUTS</span></span>

## <span data-ttu-id="3573d-121">출력</span><span class="sxs-lookup"><span data-stu-id="3573d-121">OUTPUTS</span></span>

### <span data-ttu-id="3573d-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="3573d-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="3573d-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3573d-123">NOTES</span></span>

<span data-ttu-id="3573d-124">별칭</span><span class="sxs-lookup"><span data-stu-id="3573d-124">ALIASES</span></span>

## <span data-ttu-id="3573d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3573d-125">RELATED LINKS</span></span>

