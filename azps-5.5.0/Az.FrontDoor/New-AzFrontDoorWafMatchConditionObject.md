---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188417"
---
# <span data-ttu-id="0057d-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0057d-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="0057d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0057d-102">SYNOPSIS</span></span>
<span data-ttu-id="0057d-103">WAF 정책 만들기를 위한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0057d-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0057d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0057d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0057d-105">설명</span><span class="sxs-lookup"><span data-stu-id="0057d-105">DESCRIPTION</span></span>
<span data-ttu-id="0057d-106">WAF 정책 만들기를 위한 MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0057d-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0057d-107">예제</span><span class="sxs-lookup"><span data-stu-id="0057d-107">EXAMPLES</span></span>

### <span data-ttu-id="0057d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0057d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="0057d-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="0057d-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="0057d-110">MatchCondition 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0057d-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="0057d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0057d-111">PARAMETERS</span></span>

### <span data-ttu-id="0057d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0057d-112">-DefaultProfile</span></span>
<span data-ttu-id="0057d-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0057d-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="0057d-114">-MatchValue</span></span>
<span data-ttu-id="0057d-115">일치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-115">Match value.</span></span>

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

### <span data-ttu-id="0057d-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="0057d-116">-MatchVariable</span></span>
<span data-ttu-id="0057d-117">변수 일치.</span><span class="sxs-lookup"><span data-stu-id="0057d-117">Match Variable.</span></span>
<span data-ttu-id="0057d-118">가능한 값은 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs', 'RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="0057d-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="0057d-119">-NegateCondition</span></span>
<span data-ttu-id="0057d-120">이 조건이 negate 조건이지 기본값이 false가 아닌지 설명</span><span class="sxs-lookup"><span data-stu-id="0057d-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="0057d-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="0057d-121">-OperatorProperty</span></span>
<span data-ttu-id="0057d-122">일치할 연산자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-122">Describes operator to be matched.</span></span>
<span data-ttu-id="0057d-123">가능한 값은 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="0057d-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="0057d-124">-Selector</span></span>
<span data-ttu-id="0057d-125">일치하는 RequestHeader 또는 RequestBody의 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="0057d-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="0057d-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="0057d-126">-Transform</span></span>
<span data-ttu-id="0057d-127">적용할 변환입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-127">Transforms to apply.</span></span> <span data-ttu-id="0057d-128">가능한 값은 '소문자', '대문자', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'입니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="0057d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0057d-129">CommonParameters</span></span>
<span data-ttu-id="0057d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0057d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0057d-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0057d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0057d-132">입력</span><span class="sxs-lookup"><span data-stu-id="0057d-132">INPUTS</span></span>

### <span data-ttu-id="0057d-133">없음</span><span class="sxs-lookup"><span data-stu-id="0057d-133">None</span></span>

## <span data-ttu-id="0057d-134">출력</span><span class="sxs-lookup"><span data-stu-id="0057d-134">OUTPUTS</span></span>

### <span data-ttu-id="0057d-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="0057d-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="0057d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0057d-136">NOTES</span></span>

## <span data-ttu-id="0057d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0057d-137">RELATED LINKS</span></span>

[<span data-ttu-id="0057d-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0057d-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
