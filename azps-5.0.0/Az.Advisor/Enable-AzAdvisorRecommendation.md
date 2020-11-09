---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311675"
---
# <span data-ttu-id="b8bec-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8bec-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="b8bec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8bec-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bec-103">Azure Advisor 추천을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="b8bec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8bec-104">SYNTAX</span></span>

### <span data-ttu-id="b8bec-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8bec-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8bec-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8bec-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8bec-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8bec-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8bec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8bec-108">DESCRIPTION</span></span>
<span data-ttu-id="b8bec-109">이 cmdlet은 이전에 억제 된 권고안을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="b8bec-110">권장 하는 것과 관련 된 비 표시 오류도 모두 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="b8bec-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b8bec-111">EXAMPLES</span></span>

### <span data-ttu-id="b8bec-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8bec-112">Example 1</span></span>
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

<span data-ttu-id="b8bec-113">"Recommendation_id" 이름을 사용 하 여 지정 된 추천에 대 한 모든 비 대 인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="b8bec-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8bec-114">Example 2</span></span>
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

<span data-ttu-id="b8bec-115">파이프라인에서 전달 된 주어진 권장 사항에 대 한 모든 비 대 인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="b8bec-116">변수</span><span class="sxs-lookup"><span data-stu-id="b8bec-116">PARAMETERS</span></span>

### <span data-ttu-id="b8bec-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b8bec-117">-Confirm</span></span>
<span data-ttu-id="b8bec-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8bec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bec-119">-DefaultProfile</span></span>
<span data-ttu-id="b8bec-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8bec-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8bec-121">-InputObject</span></span>
<span data-ttu-id="b8bec-122">Get-AzAdvisorRecommendation 호출에서 반환 된 powershell 개체 유형 PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="b8bec-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="b8bec-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="b8bec-123">-RecommendationName</span></span>
<span data-ttu-id="b8bec-124">이 권고안의 Context.resourcename입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="b8bec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8bec-125">-ResourceId</span></span>
<span data-ttu-id="b8bec-126">억제할 추천의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="b8bec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8bec-127">-WhatIf</span></span>
<span data-ttu-id="b8bec-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8bec-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8bec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bec-130">CommonParameters</span></span>
<span data-ttu-id="b8bec-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b8bec-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8bec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bec-133">입력</span><span class="sxs-lookup"><span data-stu-id="b8bec-133">INPUTS</span></span>

### <span data-ttu-id="b8bec-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8bec-134">System.String</span></span>

### <span data-ttu-id="b8bec-135">PsAzureAdvisorResourceRecommendationBase를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b8bec-136">출력</span><span class="sxs-lookup"><span data-stu-id="b8bec-136">OUTPUTS</span></span>

### <span data-ttu-id="b8bec-137">PsAzureAdvisorResourceRecommendationBase를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bec-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b8bec-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b8bec-138">NOTES</span></span>

## <span data-ttu-id="b8bec-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8bec-139">RELATED LINKS</span></span>
