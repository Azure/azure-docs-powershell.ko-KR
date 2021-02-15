---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190121"
---
# <span data-ttu-id="77311-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="77311-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="77311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77311-102">SYNOPSIS</span></span>
<span data-ttu-id="77311-103">메트릭 경고 조건을 생성하는 데 사용할 수 있는 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77311-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="77311-104">구문</span><span class="sxs-lookup"><span data-stu-id="77311-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77311-105">설명</span><span class="sxs-lookup"><span data-stu-id="77311-105">DESCRIPTION</span></span>
<span data-ttu-id="77311-106">**New-AzMetricAlertRuleV2DimensionSelection** cmdlet은 [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet을 사용하여 메트릭 경고 조건의 생성에 도움이 되는 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77311-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="77311-107">예제</span><span class="sxs-lookup"><span data-stu-id="77311-107">EXAMPLES</span></span>

### <span data-ttu-id="77311-108">예제 1: 차원 선택 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="77311-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="77311-109">이 명령은 차원 "LUN"에 대해 값을 선택해야 하게 지정하는 차원 선택 개체를 {1,3,4} 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77311-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="77311-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77311-110">PARAMETERS</span></span>

### <span data-ttu-id="77311-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77311-111">-DefaultProfile</span></span>
<span data-ttu-id="77311-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77311-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77311-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="77311-113">-DimensionName</span></span>
<span data-ttu-id="77311-114">차원 이름</span><span class="sxs-lookup"><span data-stu-id="77311-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77311-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="77311-115">-ValuesToExclude</span></span>
<span data-ttu-id="77311-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="77311-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77311-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="77311-117">-ValuesToInclude</span></span>
<span data-ttu-id="77311-118">The IncludeValues</span><span class="sxs-lookup"><span data-stu-id="77311-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77311-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77311-119">CommonParameters</span></span>
<span data-ttu-id="77311-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77311-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77311-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77311-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77311-122">입력</span><span class="sxs-lookup"><span data-stu-id="77311-122">INPUTS</span></span>

### <span data-ttu-id="77311-123">System.String</span><span class="sxs-lookup"><span data-stu-id="77311-123">System.String</span></span>

### <span data-ttu-id="77311-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="77311-124">System.String[]</span></span>

## <span data-ttu-id="77311-125">출력</span><span class="sxs-lookup"><span data-stu-id="77311-125">OUTPUTS</span></span>

### <span data-ttu-id="77311-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="77311-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="77311-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77311-127">NOTES</span></span>

## <span data-ttu-id="77311-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77311-128">RELATED LINKS</span></span>
