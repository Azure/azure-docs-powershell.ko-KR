---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041978"
---
# <span data-ttu-id="638ed-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="638ed-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="638ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638ed-102">SYNOPSIS</span></span>
<span data-ttu-id="638ed-103">Azure Advisor 권장 사항 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="638ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="638ed-104">SYNTAX</span></span>

### <span data-ttu-id="638ed-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="638ed-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638ed-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="638ed-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="638ed-107">DESCRIPTION</span></span>
<span data-ttu-id="638ed-108">Azure Advisor 권장 사항 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="638ed-109">범주, 리소스 ID, 이름 등을 기준으로 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="638ed-110">예제의</span><span class="sxs-lookup"><span data-stu-id="638ed-110">EXAMPLES</span></span>

### <span data-ttu-id="638ed-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="638ed-111">Example 1</span></span>
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
<span data-ttu-id="638ed-112">모든 권장 사항 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="638ed-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="638ed-113">Example 2</span></span>
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
<span data-ttu-id="638ed-114">범주 성능에 따라 필터링 된 모든 권장 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="638ed-115">변수</span><span class="sxs-lookup"><span data-stu-id="638ed-115">PARAMETERS</span></span>

### <span data-ttu-id="638ed-116">-범주</span><span class="sxs-lookup"><span data-stu-id="638ed-116">-Category</span></span>
<span data-ttu-id="638ed-117">추천 범주</span><span class="sxs-lookup"><span data-stu-id="638ed-117">Category of the recommendation</span></span>

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

### <span data-ttu-id="638ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638ed-118">-DefaultProfile</span></span>
<span data-ttu-id="638ed-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="638ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="638ed-121">추천의 ResourceGroup 이름</span><span class="sxs-lookup"><span data-stu-id="638ed-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="638ed-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="638ed-122">-ResourceId</span></span>
<span data-ttu-id="638ed-123">권장 사항의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="638ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638ed-124">CommonParameters</span></span>
<span data-ttu-id="638ed-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="638ed-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638ed-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638ed-127">입력</span><span class="sxs-lookup"><span data-stu-id="638ed-127">INPUTS</span></span>

### <span data-ttu-id="638ed-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="638ed-128">System.String</span></span>

## <span data-ttu-id="638ed-129">출력</span><span class="sxs-lookup"><span data-stu-id="638ed-129">OUTPUTS</span></span>

### <span data-ttu-id="638ed-130">PsAzureAdvisorResourceRecommendationBase를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="638ed-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="638ed-131">상속자</span><span class="sxs-lookup"><span data-stu-id="638ed-131">NOTES</span></span>

## <span data-ttu-id="638ed-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="638ed-132">RELATED LINKS</span></span>
