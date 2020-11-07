---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 04c48c96ee70896f221bfa824c3fefa06ffa89d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870390"
---
# <span data-ttu-id="f40d7-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f40d7-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="f40d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f40d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f40d7-103">메트릭 알림 조건을 구성 하는 데 사용할 수 있는 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="f40d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f40d7-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f40d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f40d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f40d7-106">**AzMetricAlertRuleV2DimensionSelection** Cmdlet은 **새 AzMetricAlertRuleV2Criteria** cmdlet을 사용 하 여 메트릭 알림 조건을 구성할 수 있도록 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="f40d7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f40d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f40d7-108">예제 1: 차원 선택 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="f40d7-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="f40d7-109">이 명령은 {1,3,4} 차원 "LUN"에 대해 값을 선택 해야 함을 지정 하는 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="f40d7-110">변수</span><span class="sxs-lookup"><span data-stu-id="f40d7-110">PARAMETERS</span></span>

### <span data-ttu-id="f40d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40d7-111">-DefaultProfile</span></span>
<span data-ttu-id="f40d7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f40d7-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="f40d7-113">-DimensionName</span></span>
<span data-ttu-id="f40d7-114">차원 이름</span><span class="sxs-lookup"><span data-stu-id="f40d7-114">The Dimension name</span></span>

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

### <span data-ttu-id="f40d7-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="f40d7-115">-ValuesToExclude</span></span>
<span data-ttu-id="f40d7-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="f40d7-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="f40d7-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="f40d7-117">-ValuesToInclude</span></span>
<span data-ttu-id="f40d7-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="f40d7-118">The IncludeValues</span></span>

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

### <span data-ttu-id="f40d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40d7-119">CommonParameters</span></span>
<span data-ttu-id="f40d7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40d7-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f40d7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40d7-122">입력</span><span class="sxs-lookup"><span data-stu-id="f40d7-122">INPUTS</span></span>

### <span data-ttu-id="f40d7-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f40d7-123">System.String</span></span>

### <span data-ttu-id="f40d7-124">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f40d7-124">System.String[]</span></span>

## <span data-ttu-id="f40d7-125">출력</span><span class="sxs-lookup"><span data-stu-id="f40d7-125">OUTPUTS</span></span>

### <span data-ttu-id="f40d7-126">PSMetricDimension를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f40d7-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="f40d7-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f40d7-127">NOTES</span></span>

## <span data-ttu-id="f40d7-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f40d7-128">RELATED LINKS</span></span>
