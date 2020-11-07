---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: f192eb4bf88201f30f8648cba6468fb406401f43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689870"
---
# <span data-ttu-id="6d2fb-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6d2fb-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="6d2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2fb-103">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6d2fb-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="6d2fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d2fb-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d2fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6d2fb-106">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6d2fb-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="6d2fb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="6d2fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d2fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="6d2fb-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="6d2fb-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="6d2fb-110">MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6d2fb-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="6d2fb-111">변수</span><span class="sxs-lookup"><span data-stu-id="6d2fb-111">PARAMETERS</span></span>

### <span data-ttu-id="6d2fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2fb-112">-DefaultProfile</span></span>
<span data-ttu-id="6d2fb-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2fb-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="6d2fb-114">-MatchValue</span></span>
<span data-ttu-id="6d2fb-115">값 일치</span><span class="sxs-lookup"><span data-stu-id="6d2fb-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d2fb-116">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="6d2fb-116">-MatchVariable</span></span>
<span data-ttu-id="6d2fb-117">Match 변수</span><span class="sxs-lookup"><span data-stu-id="6d2fb-117">Match Variable.</span></span>
<span data-ttu-id="6d2fb-118">사용할 수 있는 값으로는 ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' Urirequesturi ', ' RequestHeader ', ' Requestmethod '가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="6d2fb-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="6d2fb-119">-NegateCondition</span></span>
<span data-ttu-id="6d2fb-120">이 값이 음수 조건이 고 기본값이 false 인지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="6d2fb-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="6d2fb-121">-OperatorProperty</span></span>
<span data-ttu-id="6d2fb-122">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-122">Describes operator to be matched.</span></span>
<span data-ttu-id="6d2fb-123">가능한 값에는 ' Any ', ' IPMatch ', ' GeoMatch ', ' Equal ', ' Contains ', ' LessThan ', ' GreaterThan ', ' LessThanOrEqual ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ', ' RegEx '가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="6d2fb-124">-선택기</span><span class="sxs-lookup"><span data-stu-id="6d2fb-124">-Selector</span></span>
<span data-ttu-id="6d2fb-125">일치 시킬 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="6d2fb-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="6d2fb-126">-변환</span><span class="sxs-lookup"><span data-stu-id="6d2fb-126">-Transform</span></span>
<span data-ttu-id="6d2fb-127">적용할 변형.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-127">Transforms to apply.</span></span> <span data-ttu-id="6d2fb-128">사용할 수 있는 값은 다음과 같습니다. ' 소문자 ', ' 대문자 ', ' Trim ', ' UrlDecode ', ' UrlEncode ', ' RemoveNulls '.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d2fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2fb-129">CommonParameters</span></span>
<span data-ttu-id="6d2fb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2fb-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d2fb-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2fb-132">입력</span><span class="sxs-lookup"><span data-stu-id="6d2fb-132">INPUTS</span></span>

### <span data-ttu-id="6d2fb-133">않아야</span><span class="sxs-lookup"><span data-stu-id="6d2fb-133">None</span></span>

## <span data-ttu-id="6d2fb-134">출력</span><span class="sxs-lookup"><span data-stu-id="6d2fb-134">OUTPUTS</span></span>

### <span data-ttu-id="6d2fb-135">FrontDoor. a i m Matchor</span><span class="sxs-lookup"><span data-stu-id="6d2fb-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="6d2fb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6d2fb-136">NOTES</span></span>

## <span data-ttu-id="6d2fb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d2fb-137">RELATED LINKS</span></span>

[<span data-ttu-id="6d2fb-138">새로운 AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="6d2fb-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
