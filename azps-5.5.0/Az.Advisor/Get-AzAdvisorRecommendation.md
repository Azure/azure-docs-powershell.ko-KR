---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192657"
---
# <span data-ttu-id="5b38d-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="5b38d-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="5b38d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b38d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b38d-103">Azure Advisor 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="5b38d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b38d-104">SYNTAX</span></span>

### <span data-ttu-id="5b38d-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b38d-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b38d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b38d-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b38d-107">설명</span><span class="sxs-lookup"><span data-stu-id="5b38d-107">DESCRIPTION</span></span>
<span data-ttu-id="5b38d-108">Azure Advisor 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="5b38d-109">범주, 리소스 ID, 이름 등을 통해 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="5b38d-110">예제</span><span class="sxs-lookup"><span data-stu-id="5b38d-110">EXAMPLES</span></span>

### <span data-ttu-id="5b38d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b38d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="5b38d-112">모든 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="5b38d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b38d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="5b38d-114">범주 성능별로 필터링된 모든 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="5b38d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b38d-115">PARAMETERS</span></span>

### <span data-ttu-id="5b38d-116">-Category</span><span class="sxs-lookup"><span data-stu-id="5b38d-116">-Category</span></span>
<span data-ttu-id="5b38d-117">권장 항목의 범주</span><span class="sxs-lookup"><span data-stu-id="5b38d-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b38d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b38d-118">-DefaultProfile</span></span>
<span data-ttu-id="5b38d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b38d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b38d-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b38d-121">권장의 ResourceGroup 이름</span><span class="sxs-lookup"><span data-stu-id="5b38d-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b38d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b38d-122">-ResourceId</span></span>
<span data-ttu-id="5b38d-123">권장의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b38d-123">ResourceId of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b38d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b38d-124">CommonParameters</span></span>
<span data-ttu-id="5b38d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b38d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b38d-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b38d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b38d-127">입력</span><span class="sxs-lookup"><span data-stu-id="5b38d-127">INPUTS</span></span>

### <span data-ttu-id="5b38d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5b38d-128">System.String</span></span>

## <span data-ttu-id="5b38d-129">출력</span><span class="sxs-lookup"><span data-stu-id="5b38d-129">OUTPUTS</span></span>

### <span data-ttu-id="5b38d-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="5b38d-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="5b38d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b38d-131">NOTES</span></span>

## <span data-ttu-id="5b38d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b38d-132">RELATED LINKS</span></span>
