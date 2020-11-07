---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702929"
---
# <span data-ttu-id="6b549-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6b549-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="6b549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b549-102">SYNOPSIS</span></span>
<span data-ttu-id="6b549-103">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6b549-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b549-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b549-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b549-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6b549-105">DESCRIPTION</span></span>
<span data-ttu-id="6b549-106">WAF 정책 만들기에 대 한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6b549-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="6b549-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6b549-107">EXAMPLES</span></span>

### <span data-ttu-id="6b549-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b549-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="6b549-109">MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6b549-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="6b549-110">변수</span><span class="sxs-lookup"><span data-stu-id="6b549-110">PARAMETERS</span></span>

### <span data-ttu-id="6b549-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b549-111">-DefaultProfile</span></span>
<span data-ttu-id="6b549-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b549-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="6b549-113">-MatchValue</span></span>
<span data-ttu-id="6b549-114">값 일치</span><span class="sxs-lookup"><span data-stu-id="6b549-114">Match value.</span></span>

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

### <span data-ttu-id="6b549-115">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="6b549-115">-MatchVariable</span></span>
<span data-ttu-id="6b549-116">Match 변수</span><span class="sxs-lookup"><span data-stu-id="6b549-116">Match Variable.</span></span>
<span data-ttu-id="6b549-117">사용할 수 있는 값으로는 ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' Urirequesturi ', ' RequestHeader ', ' Requestmethod '가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="6b549-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="6b549-118">-NegateCondition</span></span>
<span data-ttu-id="6b549-119">이 값이 음수 조건이 고 기본값이 false 인지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="6b549-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="6b549-120">-OperatorProperty</span></span>
<span data-ttu-id="6b549-121">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-121">Describes operator to be matched.</span></span>
<span data-ttu-id="6b549-122">가능한 값은 ' Any ', ' IPMatch ', ' GeoMatch ', ' Equal ', ' Contains ', ' LessThan ', ' GreaterThan ', ' LessThanOrEqual ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ' ' 등입니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="6b549-123">-선택기</span><span class="sxs-lookup"><span data-stu-id="6b549-123">-Selector</span></span>
<span data-ttu-id="6b549-124">일치 시킬 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="6b549-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="6b549-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b549-125">CommonParameters</span></span>
<span data-ttu-id="6b549-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b549-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b549-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b549-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b549-128">입력</span><span class="sxs-lookup"><span data-stu-id="6b549-128">INPUTS</span></span>

### <span data-ttu-id="6b549-129">않아야</span><span class="sxs-lookup"><span data-stu-id="6b549-129">None</span></span>

## <span data-ttu-id="6b549-130">출력</span><span class="sxs-lookup"><span data-stu-id="6b549-130">OUTPUTS</span></span>

### <span data-ttu-id="6b549-131">FrontDoor. a i m Matchor</span><span class="sxs-lookup"><span data-stu-id="6b549-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="6b549-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6b549-132">NOTES</span></span>

## <span data-ttu-id="6b549-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b549-133">RELATED LINKS</span></span>

[<span data-ttu-id="6b549-134">새로운 AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="6b549-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
