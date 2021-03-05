---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: 7bef36412f8b1b5977e94b32d0645ccdaa8d0324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970939"
---
# <span data-ttu-id="b9c75-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="b9c75-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="b9c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c75-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c75-103">규칙 엔진 만들기를 위한 PSRulesEngineRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="b9c75-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9c75-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c75-105">설명</span><span class="sxs-lookup"><span data-stu-id="b9c75-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c75-106">규칙 엔진 만들기를 위한 PSRulesEngineRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="b9c75-107">cmdlet "New-AzFrontDoorRulesEngineActionObject"를 사용하여 PSRulesEngineAction 개체를 만들어 "-Action" 매개 변수에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="b9c75-108">cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject"를 사용하여 PSRulesEngineMatchCondition 개체를 만들어 "-MatchCondition" 매개 변수에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="b9c75-109">예제</span><span class="sxs-lookup"><span data-stu-id="b9c75-109">EXAMPLES</span></span>

### <span data-ttu-id="b9c75-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9c75-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="b9c75-111">새 PSRulesEngineRule 개체를 만들고 하위 필드를 보는 방법을 보여 옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="b9c75-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9c75-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="b9c75-113">잘못된 우선 순위 값을 전달할 때 출력을 예상합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="b9c75-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9c75-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c75-115">-Action</span><span class="sxs-lookup"><span data-stu-id="b9c75-115">-Action</span></span>
<span data-ttu-id="b9c75-116">모든 일치 조건이 충족된 경우 요청 및 응답에서 수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c75-117">-DefaultProfile</span></span>
<span data-ttu-id="b9c75-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c75-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b9c75-119">-MatchCondition</span></span>
<span data-ttu-id="b9c75-120">이 규칙의 작업을 실행하기 위해 충족해야 하는 일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="b9c75-121">일치 조건이 없는 경우 작업이 항상 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="b9c75-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="b9c75-123">이 규칙이 일치하면 규칙 엔진이 나머지 규칙을 계속 실행하거나 중지해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="b9c75-124">가능한 값은 계속 및 중지입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="b9c75-125">없는 경우 기본값은 계속으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b9c75-126">-Name</span></span>
<span data-ttu-id="b9c75-127">이 특정 규칙을 참조하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-127">A name to refer to this specific rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="b9c75-128">-Priority</span></span>
<span data-ttu-id="b9c75-129">이 규칙에 할당된 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="b9c75-130">음수일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c75-131">CommonParameters</span></span>
<span data-ttu-id="b9c75-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c75-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9c75-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c75-134">입력</span><span class="sxs-lookup"><span data-stu-id="b9c75-134">INPUTS</span></span>

### <span data-ttu-id="b9c75-135">없음</span><span class="sxs-lookup"><span data-stu-id="b9c75-135">None</span></span>

## <span data-ttu-id="b9c75-136">출력</span><span class="sxs-lookup"><span data-stu-id="b9c75-136">OUTPUTS</span></span>

### <span data-ttu-id="b9c75-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="b9c75-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="b9c75-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9c75-138">NOTES</span></span>

## <span data-ttu-id="b9c75-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c75-139">RELATED LINKS</span></span>
