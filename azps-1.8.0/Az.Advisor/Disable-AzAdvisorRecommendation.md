---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689225"
---
# <span data-ttu-id="b02e5-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="b02e5-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="b02e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b02e5-103">Azure Advisor 추천을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="b02e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b02e5-104">SYNTAX</span></span>

### <span data-ttu-id="b02e5-105">IdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b02e5-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02e5-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02e5-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02e5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02e5-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b02e5-108">DESCRIPTION</span></span>
<span data-ttu-id="b02e5-109">추천 단어에 대 한 억제를 만들어 특정 기간이 나 무한정으로 특정 권장 사항을 연기 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="b02e5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b02e5-110">EXAMPLES</span></span>

### <span data-ttu-id="b02e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b02e5-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="b02e5-112">지정 된 권고안 이름에 대 한 SuppressionName 및 default 일을-1로 사용 하 여 비 표시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="b02e5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b02e5-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="b02e5-114">지정 된 권고안 Id에 대 한 비 표시 (제거)가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="b02e5-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="b02e5-115">Example 3</span></span>
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

<span data-ttu-id="b02e5-116">Get-AzAdvisorRecommendation에서 AzAdvisorRecommendation를 사용 하지 않도록 설정 하 여 비 표시 금지, 파이핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="b02e5-117">변수</span><span class="sxs-lookup"><span data-stu-id="b02e5-117">PARAMETERS</span></span>

### <span data-ttu-id="b02e5-118">-확인</span><span class="sxs-lookup"><span data-stu-id="b02e5-118">-Confirm</span></span>
<span data-ttu-id="b02e5-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02e5-120">일</span><span class="sxs-lookup"><span data-stu-id="b02e5-120">-Days</span></span>
<span data-ttu-id="b02e5-121">사용 하지 않을 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-121">Days to disable.</span></span>

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

### <span data-ttu-id="b02e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02e5-122">-DefaultProfile</span></span>
<span data-ttu-id="b02e5-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b02e5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b02e5-124">-InputObject</span></span>
<span data-ttu-id="b02e5-125">Get-AzAdvisorRecommendation 호출에서 반환 된 powershell 개체 유형 PsAzureAdvisorResourceRecommendationBase.</span><span class="sxs-lookup"><span data-stu-id="b02e5-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="b02e5-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="b02e5-126">-RecommendationName</span></span>
<span data-ttu-id="b02e5-127">추천의 Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="b02e5-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="b02e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b02e5-128">-ResourceId</span></span>
<span data-ttu-id="b02e5-129">억제할 추천의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="b02e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02e5-130">-WhatIf</span></span>
<span data-ttu-id="b02e5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02e5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02e5-133">CommonParameters</span></span>
<span data-ttu-id="b02e5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b02e5-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02e5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02e5-136">입력</span><span class="sxs-lookup"><span data-stu-id="b02e5-136">INPUTS</span></span>

### <span data-ttu-id="b02e5-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b02e5-137">System.String</span></span>

### <span data-ttu-id="b02e5-138">PsAzureAdvisorResourceRecommendationBase를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b02e5-139">출력</span><span class="sxs-lookup"><span data-stu-id="b02e5-139">OUTPUTS</span></span>

### <span data-ttu-id="b02e5-140">PsAzureAdvisorSuppressionContract를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="b02e5-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="b02e5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b02e5-141">NOTES</span></span>

## <span data-ttu-id="b02e5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b02e5-142">RELATED LINKS</span></span>
