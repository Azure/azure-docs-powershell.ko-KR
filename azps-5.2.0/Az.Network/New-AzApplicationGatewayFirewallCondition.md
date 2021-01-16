---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340317"
---
# <span data-ttu-id="20581-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="20581-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="20581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20581-102">SYNOPSIS</span></span>
<span data-ttu-id="20581-103">사용자 지정 규칙에 대한 일치 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20581-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="20581-104">구문</span><span class="sxs-lookup"><span data-stu-id="20581-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20581-105">설명</span><span class="sxs-lookup"><span data-stu-id="20581-105">DESCRIPTION</span></span>
<span data-ttu-id="20581-106">**New-AzApplicationGatewayFirewallCondition은** 방화벽 사용자 지정 규칙에 대한 일치 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20581-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="20581-107">예제</span><span class="sxs-lookup"><span data-stu-id="20581-107">EXAMPLES</span></span>

### <span data-ttu-id="20581-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="20581-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="20581-109">이 명령은 $variable 정의된 일치 변수를 사용하여 새 일치 조건을 만들고, 연산자가 포함되고, negation 조건은 false, 소문자 및 자르기 등의 Transfroms, 일치 값은 abc 및 cde입니다.</span><span class="sxs-lookup"><span data-stu-id="20581-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="20581-110">새 일치 조건은 새 $condition.</span><span class="sxs-lookup"><span data-stu-id="20581-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="20581-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20581-111">PARAMETERS</span></span>

### <span data-ttu-id="20581-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20581-112">-DefaultProfile</span></span>
<span data-ttu-id="20581-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20581-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20581-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="20581-114">-MatchValue</span></span>
<span data-ttu-id="20581-115">일치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="20581-115">Match value.</span></span>

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

### <span data-ttu-id="20581-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="20581-116">-MatchVariable</span></span>
<span data-ttu-id="20581-117">일치 변수 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20581-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20581-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="20581-118">-NegationCondition</span></span>
<span data-ttu-id="20581-119">이 조건이 negate 조건인 경우를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20581-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="20581-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="20581-120">-Operator</span></span>
<span data-ttu-id="20581-121">일치할 연산자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20581-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20581-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="20581-122">-Transform</span></span>
<span data-ttu-id="20581-123">변환 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20581-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20581-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20581-124">CommonParameters</span></span>
<span data-ttu-id="20581-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20581-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20581-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20581-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20581-127">입력</span><span class="sxs-lookup"><span data-stu-id="20581-127">INPUTS</span></span>

### <span data-ttu-id="20581-128">없음</span><span class="sxs-lookup"><span data-stu-id="20581-128">None</span></span>

## <span data-ttu-id="20581-129">출력</span><span class="sxs-lookup"><span data-stu-id="20581-129">OUTPUTS</span></span>

### <span data-ttu-id="20581-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="20581-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="20581-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20581-131">NOTES</span></span>

## <span data-ttu-id="20581-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20581-132">RELATED LINKS</span></span>
