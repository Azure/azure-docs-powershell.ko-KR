---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 349677b4686b2df5a72f233b729a5028dc322057
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867258"
---
# <span data-ttu-id="00bdf-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="00bdf-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="00bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="00bdf-103">메트릭 알림 조건을 구성 하는 데 사용할 수 있는 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="00bdf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00bdf-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00bdf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="00bdf-106">**AzMetricAlertRuleV2DimensionSelection** Cmdlet은 **새 AzMetricAlertRuleV2Criteria** cmdlet을 사용 하 여 메트릭 알림 조건을 구성할 수 있도록 로컬 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="00bdf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="00bdf-108">예제 1: 차원 선택 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="00bdf-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}     
```

<span data-ttu-id="00bdf-109">이 명령은 {1,3,4} 차원 "LUN"에 대해 값을 선택 해야 함을 지정 하는 차원 선택 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="00bdf-110">변수</span><span class="sxs-lookup"><span data-stu-id="00bdf-110">PARAMETERS</span></span>

### <span data-ttu-id="00bdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bdf-111">-DefaultProfile</span></span>
<span data-ttu-id="00bdf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00bdf-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="00bdf-113">-DimensionName</span></span>
<span data-ttu-id="00bdf-114">차원 이름</span><span class="sxs-lookup"><span data-stu-id="00bdf-114">The Dimension name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bdf-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="00bdf-115">-ValuesToExclude</span></span>
<span data-ttu-id="00bdf-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="00bdf-116">The ExcludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bdf-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="00bdf-117">-ValuesToInclude</span></span>
<span data-ttu-id="00bdf-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="00bdf-118">The IncludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bdf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bdf-119">CommonParameters</span></span>
<span data-ttu-id="00bdf-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00bdf-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bdf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bdf-122">입력</span><span class="sxs-lookup"><span data-stu-id="00bdf-122">INPUTS</span></span>

### <span data-ttu-id="00bdf-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00bdf-123">System.String</span></span>

### <span data-ttu-id="00bdf-124">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="00bdf-124">System.String[]</span></span>

## <span data-ttu-id="00bdf-125">출력</span><span class="sxs-lookup"><span data-stu-id="00bdf-125">OUTPUTS</span></span>

### <span data-ttu-id="00bdf-126">PSMetricDimension를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bdf-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="00bdf-127">상속자</span><span class="sxs-lookup"><span data-stu-id="00bdf-127">NOTES</span></span>

## <span data-ttu-id="00bdf-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00bdf-128">RELATED LINKS</span></span>
