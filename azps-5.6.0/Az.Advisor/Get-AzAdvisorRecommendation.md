---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 9d45db213cf3569837c6b35284c95dc9a076a381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967003"
---
# <span data-ttu-id="9f61e-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="9f61e-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="9f61e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f61e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f61e-103">Azure Advisor 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="9f61e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f61e-104">SYNTAX</span></span>

### <span data-ttu-id="9f61e-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f61e-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f61e-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f61e-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f61e-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f61e-107">DESCRIPTION</span></span>
<span data-ttu-id="9f61e-108">Azure Advisor 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="9f61e-109">범주, 리소스 ID, 이름 등을 통해 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="9f61e-110">예제</span><span class="sxs-lookup"><span data-stu-id="9f61e-110">EXAMPLES</span></span>

### <span data-ttu-id="9f61e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f61e-111">Example 1</span></span>
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
<span data-ttu-id="9f61e-112">모든 권장 사항 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="9f61e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9f61e-113">Example 2</span></span>
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
<span data-ttu-id="9f61e-114">범주 성능으로 필터링된 모든 권장 사항 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="9f61e-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f61e-115">PARAMETERS</span></span>

### <span data-ttu-id="9f61e-116">-Category</span><span class="sxs-lookup"><span data-stu-id="9f61e-116">-Category</span></span>
<span data-ttu-id="9f61e-117">권장 항목 범주</span><span class="sxs-lookup"><span data-stu-id="9f61e-117">Category of the recommendation</span></span>

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

### <span data-ttu-id="9f61e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f61e-118">-DefaultProfile</span></span>
<span data-ttu-id="9f61e-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f61e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f61e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f61e-121">권장의 ResourceGroup 이름</span><span class="sxs-lookup"><span data-stu-id="9f61e-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="9f61e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f61e-122">-ResourceId</span></span>
<span data-ttu-id="9f61e-123">권장의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f61e-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="9f61e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f61e-124">CommonParameters</span></span>
<span data-ttu-id="9f61e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f61e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9f61e-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f61e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f61e-127">입력</span><span class="sxs-lookup"><span data-stu-id="9f61e-127">INPUTS</span></span>

### <span data-ttu-id="9f61e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9f61e-128">System.String</span></span>

## <span data-ttu-id="9f61e-129">출력</span><span class="sxs-lookup"><span data-stu-id="9f61e-129">OUTPUTS</span></span>

### <span data-ttu-id="9f61e-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="9f61e-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="9f61e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f61e-131">NOTES</span></span>

## <span data-ttu-id="9f61e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f61e-132">RELATED LINKS</span></span>
