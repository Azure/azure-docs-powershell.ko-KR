---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047755"
---
# <span data-ttu-id="ffad7-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="ffad7-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="ffad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffad7-102">SYNOPSIS</span></span>
<span data-ttu-id="ffad7-103">규칙 엔진 만들기에 대 한 PSRulesEngineRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="ffad7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffad7-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffad7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffad7-105">DESCRIPTION</span></span>
<span data-ttu-id="ffad7-106">규칙 엔진 만들기에 대 한 PSRulesEngineRule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="ffad7-107">Cmdlet "New-AzFrontDoorRulesEngineActionObject"를 사용 하 여 PSRulesEngineAction 개체를 만들어 "-Action" 매개 변수에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="ffad7-108">Cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject"를 사용 하 여 PSRulesEngineMatchCondition 개체를 만들어 "-MatchCondition" 매개 변수에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="ffad7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ffad7-109">EXAMPLES</span></span>

### <span data-ttu-id="ffad7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffad7-110">Example 1</span></span>
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

<span data-ttu-id="ffad7-111">새 PSRulesEngineRule 개체를 만들고 하위 필드를 표시 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="ffad7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ffad7-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="ffad7-113">유효 하지 않은 우선 순위 값을 전달할 때 출력이 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="ffad7-114">변수</span><span class="sxs-lookup"><span data-stu-id="ffad7-114">PARAMETERS</span></span>

### <span data-ttu-id="ffad7-115">-작업</span><span class="sxs-lookup"><span data-stu-id="ffad7-115">-Action</span></span>
<span data-ttu-id="ffad7-116">요청 및 응답에 대해 수행할 작업입니다. 일치 조건이 모두 충족 되는 경우</span><span class="sxs-lookup"><span data-stu-id="ffad7-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="ffad7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffad7-117">-DefaultProfile</span></span>
<span data-ttu-id="ffad7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffad7-119">MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ffad7-119">-MatchCondition</span></span>
<span data-ttu-id="ffad7-120">이 규칙의 작업을 실행 하기 위해 충족 해야 하는 일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="ffad7-121">일치 조건이 없는 경우에는 작업이 항상 실행 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="ffad7-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="ffad7-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="ffad7-123">이 규칙이 일치 하는 경우 규칙 엔진이 나머지 규칙을 계속 실행 하거나 중지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="ffad7-124">사용할 수 있는 값은 계속 되 고 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="ffad7-125">표시 되지 않으면 기본적으로 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="ffad7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="ffad7-126">-Name</span></span>
<span data-ttu-id="ffad7-127">이 특정 규칙을 참조 하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="ffad7-128">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ffad7-128">-Priority</span></span>
<span data-ttu-id="ffad7-129">이 규칙에 할당 된 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="ffad7-130">음수일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="ffad7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffad7-131">CommonParameters</span></span>
<span data-ttu-id="ffad7-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffad7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffad7-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffad7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffad7-134">입력</span><span class="sxs-lookup"><span data-stu-id="ffad7-134">INPUTS</span></span>

### <span data-ttu-id="ffad7-135">않아야</span><span class="sxs-lookup"><span data-stu-id="ffad7-135">None</span></span>

## <span data-ttu-id="ffad7-136">출력</span><span class="sxs-lookup"><span data-stu-id="ffad7-136">OUTPUTS</span></span>

### <span data-ttu-id="ffad7-137">FrontDoor. PSRulesEngineRule/.</span><span class="sxs-lookup"><span data-stu-id="ffad7-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="ffad7-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ffad7-138">NOTES</span></span>

## <span data-ttu-id="ffad7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffad7-139">RELATED LINKS</span></span>
