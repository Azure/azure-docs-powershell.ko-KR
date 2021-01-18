---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492689"
---
# <span data-ttu-id="bc80a-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="bc80a-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="bc80a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc80a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc80a-103">Azure Advisor 권장을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="bc80a-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc80a-104">SYNTAX</span></span>

### <span data-ttu-id="bc80a-105">IdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc80a-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc80a-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc80a-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc80a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc80a-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc80a-108">설명</span><span class="sxs-lookup"><span data-stu-id="bc80a-108">DESCRIPTION</span></span>
<span data-ttu-id="bc80a-109">권장을 표시하지 않습니다. 이렇게 하면 특정 권장을 특정 기간 동안 또는 무한정 연기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="bc80a-110">예제</span><span class="sxs-lookup"><span data-stu-id="bc80a-110">EXAMPLES</span></span>

### <span data-ttu-id="bc80a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc80a-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="bc80a-112">default-SuppressionName 및 기본 일 수를 -1로 사용하여 지정한 권장 이름에 대한 표시 안 을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="bc80a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="bc80a-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="bc80a-114">제공된 권장 ID에 대한 표시 안 움선이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="bc80a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="bc80a-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="bc80a-116">표시 안 을 만들고, Get-AzAdvisorRecommendation-AzAdvisorRecommendation으로 파이핑합니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="bc80a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc80a-117">PARAMETERS</span></span>

### <span data-ttu-id="bc80a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc80a-118">-Confirm</span></span>
<span data-ttu-id="bc80a-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc80a-120">-Days</span><span class="sxs-lookup"><span data-stu-id="bc80a-120">-Days</span></span>
<span data-ttu-id="bc80a-121">비활성화할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc80a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc80a-122">-DefaultProfile</span></span>
<span data-ttu-id="bc80a-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc80a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc80a-124">-InputObject</span></span>
<span data-ttu-id="bc80a-125">powershell 개체 형식 PsAzureAdvisorResourceRecommendationBase는 Get-AzAdvisorRecommendation 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="bc80a-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="bc80a-126">-RecommendationName</span></span>
<span data-ttu-id="bc80a-127">권장의 ResourceName</span><span class="sxs-lookup"><span data-stu-id="bc80a-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="bc80a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc80a-128">-ResourceId</span></span>
<span data-ttu-id="bc80a-129">표시 안 하게 될 권장의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc80a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc80a-130">-WhatIf</span></span>
<span data-ttu-id="bc80a-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bc80a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc80a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc80a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc80a-133">CommonParameters</span></span>
<span data-ttu-id="bc80a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc80a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bc80a-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc80a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc80a-136">입력</span><span class="sxs-lookup"><span data-stu-id="bc80a-136">INPUTS</span></span>

### <span data-ttu-id="bc80a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bc80a-137">System.String</span></span>

### <span data-ttu-id="bc80a-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="bc80a-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="bc80a-139">출력</span><span class="sxs-lookup"><span data-stu-id="bc80a-139">OUTPUTS</span></span>

### <span data-ttu-id="bc80a-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="bc80a-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="bc80a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc80a-141">NOTES</span></span>

## <span data-ttu-id="bc80a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc80a-142">RELATED LINKS</span></span>
