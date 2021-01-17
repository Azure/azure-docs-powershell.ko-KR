---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342566"
---
# <span data-ttu-id="911cf-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="911cf-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="911cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="911cf-102">SYNOPSIS</span></span>
<span data-ttu-id="911cf-103">Azure Advisor 권장을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="911cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="911cf-104">SYNTAX</span></span>

### <span data-ttu-id="911cf-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="911cf-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="911cf-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="911cf-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="911cf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="911cf-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="911cf-108">설명</span><span class="sxs-lookup"><span data-stu-id="911cf-108">DESCRIPTION</span></span>
<span data-ttu-id="911cf-109">이 cmdlet을 사용하면 이전에 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="911cf-110">권장과 연결된 모든 표시 안 을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="911cf-111">예제</span><span class="sxs-lookup"><span data-stu-id="911cf-111">EXAMPLES</span></span>

### <span data-ttu-id="911cf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="911cf-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="911cf-113">"recommendation_id"라는 이름으로 지정한 권장에 대한 모든 표시를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="911cf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="911cf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="911cf-115">파이프라인에서 전달된 주어진 권장에 대한 모든 표시를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="911cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="911cf-116">PARAMETERS</span></span>

### <span data-ttu-id="911cf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="911cf-117">-Confirm</span></span>
<span data-ttu-id="911cf-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="911cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911cf-119">-DefaultProfile</span></span>
<span data-ttu-id="911cf-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="911cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="911cf-121">-InputObject</span></span>
<span data-ttu-id="911cf-122">powershell 개체 형식 PsAzureAdvisorResourceRecommendationBase는 Get-AzAdvisorRecommendation 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="911cf-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="911cf-123">-RecommendationName</span></span>
<span data-ttu-id="911cf-124">권장의 ResourceName입니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="911cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="911cf-125">-ResourceId</span></span>
<span data-ttu-id="911cf-126">표시 안 하게 될 권장의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="911cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="911cf-127">-WhatIf</span></span>
<span data-ttu-id="911cf-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="911cf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="911cf-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="911cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911cf-130">CommonParameters</span></span>
<span data-ttu-id="911cf-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="911cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="911cf-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="911cf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911cf-133">입력</span><span class="sxs-lookup"><span data-stu-id="911cf-133">INPUTS</span></span>

### <span data-ttu-id="911cf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="911cf-134">System.String</span></span>

### <span data-ttu-id="911cf-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="911cf-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="911cf-136">출력</span><span class="sxs-lookup"><span data-stu-id="911cf-136">OUTPUTS</span></span>

### <span data-ttu-id="911cf-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="911cf-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="911cf-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="911cf-138">NOTES</span></span>

## <span data-ttu-id="911cf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="911cf-139">RELATED LINKS</span></span>
