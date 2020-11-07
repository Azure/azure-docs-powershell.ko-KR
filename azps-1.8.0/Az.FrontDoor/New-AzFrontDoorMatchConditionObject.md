---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868369"
---
# <span data-ttu-id="750cd-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="750cd-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="750cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="750cd-102">SYNOPSIS</span></span>
<span data-ttu-id="750cd-103">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="750cd-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="750cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="750cd-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="750cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="750cd-105">DESCRIPTION</span></span>
<span data-ttu-id="750cd-106">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="750cd-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="750cd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="750cd-107">EXAMPLES</span></span>

### <span data-ttu-id="750cd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="750cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="750cd-109">MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="750cd-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="750cd-110">변수</span><span class="sxs-lookup"><span data-stu-id="750cd-110">PARAMETERS</span></span>

### <span data-ttu-id="750cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750cd-111">-DefaultProfile</span></span>
<span data-ttu-id="750cd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750cd-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="750cd-113">-MatchValue</span></span>
<span data-ttu-id="750cd-114">값 일치</span><span class="sxs-lookup"><span data-stu-id="750cd-114">Match value.</span></span>

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

### <span data-ttu-id="750cd-115">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="750cd-115">-MatchVariable</span></span>
<span data-ttu-id="750cd-116">Match 변수</span><span class="sxs-lookup"><span data-stu-id="750cd-116">Match Variable.</span></span>
<span data-ttu-id="750cd-117">사용할 수 있는 값으로는 ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' Urirequesturi ', ' RequestHeader ', ' Requestmethod '가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750cd-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="750cd-118">-NegateCondition</span></span>
<span data-ttu-id="750cd-119">이 값이 음수 조건이 고 기본값이 false 인지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="750cd-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="750cd-120">-OperatorProperty</span></span>
<span data-ttu-id="750cd-121">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-121">Describes operator to be matched.</span></span>
<span data-ttu-id="750cd-122">가능한 값은 ' Any ', ' IPMatch ', ' GeoMatch ', ' Equal ', ' Contains ', ' LessThan ', ' GreaterThan ', ' LessThanOrEqual ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ' ' 등입니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750cd-123">-선택기</span><span class="sxs-lookup"><span data-stu-id="750cd-123">-Selector</span></span>
<span data-ttu-id="750cd-124">일치 시킬 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="750cd-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="750cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750cd-125">CommonParameters</span></span>
<span data-ttu-id="750cd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="750cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750cd-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="750cd-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750cd-128">입력</span><span class="sxs-lookup"><span data-stu-id="750cd-128">INPUTS</span></span>

### <span data-ttu-id="750cd-129">않아야</span><span class="sxs-lookup"><span data-stu-id="750cd-129">None</span></span>

## <span data-ttu-id="750cd-130">출력</span><span class="sxs-lookup"><span data-stu-id="750cd-130">OUTPUTS</span></span>

### <span data-ttu-id="750cd-131">FrontDoor. a i m Matchor</span><span class="sxs-lookup"><span data-stu-id="750cd-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="750cd-132">상속자</span><span class="sxs-lookup"><span data-stu-id="750cd-132">NOTES</span></span>

## <span data-ttu-id="750cd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="750cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="750cd-134">새로운 AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="750cd-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
