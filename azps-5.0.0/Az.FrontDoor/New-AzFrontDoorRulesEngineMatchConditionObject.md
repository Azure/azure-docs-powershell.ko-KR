---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217411"
---
# <span data-ttu-id="d8a85-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d8a85-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="d8a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a85-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a85-103">규칙 엔진 규칙을 만들기 위한 PSRulesEngineMatchCondition 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="d8a85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8a85-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8a85-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a85-106">규칙 엔진 규칙을 만들기 위한 PSRulesEngineMatchCondition 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="d8a85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8a85-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a85-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8a85-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="d8a85-109">Greate 새 PSRulesEngineMatchCondition 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="d8a85-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8a85-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a85-111">-DefaultProfile</span></span>
<span data-ttu-id="d8a85-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a85-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d8a85-113">-MatchValue</span></span>
<span data-ttu-id="d8a85-114">일치 하는 값을 일치 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-114">Match values to match against.</span></span>
<span data-ttu-id="d8a85-115">연산자는 여기에 나와 있는 각 값에 또는 의미 체계에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="d8a85-116">지정 된 연산자를 사용 하 여 변수와 일치 하는 항목이 있으면 일치 조건이 일치 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="d8a85-117">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d8a85-117">-MatchVariable</span></span>
<span data-ttu-id="d8a85-118">Match 변수</span><span class="sxs-lookup"><span data-stu-id="d8a85-118">Match Variable.</span></span>
<span data-ttu-id="d8a85-119">사용할 수 있는 값은 IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, Urirequesturi, Requestmethod, Requestmethod, RequestfilenameExtension, RequestHeader, Requestmethod, Requestmethod입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="d8a85-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="d8a85-120">-NegateCondition</span></span>
<span data-ttu-id="d8a85-121">이 조건이 음수 인지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="d8a85-122">-연산자</span><span class="sxs-lookup"><span data-stu-id="d8a85-122">-Operator</span></span>
<span data-ttu-id="d8a85-123">일치 조건에 적용할 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="d8a85-124">가능한 값은 Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="d8a85-125">-선택기</span><span class="sxs-lookup"><span data-stu-id="d8a85-125">-Selector</span></span>
<span data-ttu-id="d8a85-126">일치 시킬 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="d8a85-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="d8a85-127">-변환</span><span class="sxs-lookup"><span data-stu-id="d8a85-127">-Transform</span></span>
<span data-ttu-id="d8a85-128">일치 하기 전에 적용 되는 변환의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="d8a85-129">사용할 수 있는 개별 변환 값은 소문자, 대문자, Trim, UrlDecode, UrlEncode, RemoveNulls입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="d8a85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a85-130">CommonParameters</span></span>
<span data-ttu-id="d8a85-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a85-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8a85-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a85-133">입력</span><span class="sxs-lookup"><span data-stu-id="d8a85-133">INPUTS</span></span>

### <span data-ttu-id="d8a85-134">않아야</span><span class="sxs-lookup"><span data-stu-id="d8a85-134">None</span></span>

## <span data-ttu-id="d8a85-135">출력</span><span class="sxs-lookup"><span data-stu-id="d8a85-135">OUTPUTS</span></span>

### <span data-ttu-id="d8a85-136">FrontDoor. PSRulesEngineMatchCondition/.</span><span class="sxs-lookup"><span data-stu-id="d8a85-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="d8a85-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d8a85-137">NOTES</span></span>

## <span data-ttu-id="d8a85-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8a85-138">RELATED LINKS</span></span>
