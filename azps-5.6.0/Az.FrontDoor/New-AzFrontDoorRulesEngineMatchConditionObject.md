---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 4f35b20b7c17a0cd809cb5964fbecfa429b581bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970955"
---
# <span data-ttu-id="dc7c2-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="dc7c2-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="dc7c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7c2-103">규칙 엔진 규칙을 만들기 위한 PSRulesEngineMatchCondition 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="dc7c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc7c2-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc7c2-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="dc7c2-106">규칙 엔진 규칙을 만들기 위한 PSRulesEngineMatchCondition 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="dc7c2-107">예제</span><span class="sxs-lookup"><span data-stu-id="dc7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="dc7c2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc7c2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="dc7c2-109">새 PSRulesEngineMatchCondition 개체를 그레이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="dc7c2-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc7c2-110">PARAMETERS</span></span>

### <span data-ttu-id="dc7c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7c2-111">-DefaultProfile</span></span>
<span data-ttu-id="dc7c2-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc7c2-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="dc7c2-113">-MatchValue</span></span>
<span data-ttu-id="dc7c2-114">일치하는 값과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-114">Match values to match against.</span></span>
<span data-ttu-id="dc7c2-115">연산자는 OR 시맨틱을 통해 여기에 있는 각 값에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="dc7c2-116">해당 연산자 중 한 개가 변수와 해당 연산자와 일치하는 경우 이 일치 조건은 일치로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="dc7c2-117">-MatchVariable</span></span>
<span data-ttu-id="dc7c2-118">변수 일치.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-118">Match Variable.</span></span>
<span data-ttu-id="dc7c2-119">가능한 값은 IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="dc7c2-120">-NegateCondition</span></span>
<span data-ttu-id="dc7c2-121">이 조건이 부적정한 상태인지 아닌지에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-122">-연산자</span><span class="sxs-lookup"><span data-stu-id="dc7c2-122">-Operator</span></span>
<span data-ttu-id="dc7c2-123">일치 조건에 적용할 연산자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="dc7c2-124">가능한 값은 Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="dc7c2-125">-Selector</span></span>
<span data-ttu-id="dc7c2-126">일치할 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="dc7c2-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="dc7c2-127">-Transform</span></span>
<span data-ttu-id="dc7c2-128">일치하기 전에 적용된 변환의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="dc7c2-129">가능한 개별 변환 값은 소문자, 대문자, 트리밍, URLDecode, URLEncode, RemoveNulls입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7c2-130">CommonParameters</span></span>
<span data-ttu-id="dc7c2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7c2-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc7c2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7c2-133">입력</span><span class="sxs-lookup"><span data-stu-id="dc7c2-133">INPUTS</span></span>

### <span data-ttu-id="dc7c2-134">없음</span><span class="sxs-lookup"><span data-stu-id="dc7c2-134">None</span></span>

## <span data-ttu-id="dc7c2-135">출력</span><span class="sxs-lookup"><span data-stu-id="dc7c2-135">OUTPUTS</span></span>

### <span data-ttu-id="dc7c2-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="dc7c2-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="dc7c2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc7c2-137">NOTES</span></span>

## <span data-ttu-id="dc7c2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc7c2-138">RELATED LINKS</span></span>
