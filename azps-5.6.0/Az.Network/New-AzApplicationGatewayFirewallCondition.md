---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007744"
---
# <span data-ttu-id="68687-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="68687-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="68687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68687-102">SYNOPSIS</span></span>
<span data-ttu-id="68687-103">사용자 지정 규칙에 대한 일치 조건 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68687-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="68687-104">구문</span><span class="sxs-lookup"><span data-stu-id="68687-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68687-105">설명</span><span class="sxs-lookup"><span data-stu-id="68687-105">DESCRIPTION</span></span>
<span data-ttu-id="68687-106">**New-AzApplicationGatewayFirewallCondition은** 방화벽 사용자 지정 규칙에 대한 일치 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68687-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="68687-107">예제</span><span class="sxs-lookup"><span data-stu-id="68687-107">EXAMPLES</span></span>

### <span data-ttu-id="68687-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="68687-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="68687-109">명령은 $variable 일치 변수를 사용하여 새 일치 조건을 만듭니다. 연산자가 포함되고 대/소변 조건은 false, 소문자 및 트리밍을 포함한 Transfroms, 일치 값은 abc 및 cde입니다.</span><span class="sxs-lookup"><span data-stu-id="68687-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="68687-110">새 일치 조건은 $condition.</span><span class="sxs-lookup"><span data-stu-id="68687-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="68687-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68687-111">PARAMETERS</span></span>

### <span data-ttu-id="68687-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68687-112">-DefaultProfile</span></span>
<span data-ttu-id="68687-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68687-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68687-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="68687-114">-MatchValue</span></span>
<span data-ttu-id="68687-115">일치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="68687-115">Match value.</span></span>

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

### <span data-ttu-id="68687-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="68687-116">-MatchVariable</span></span>
<span data-ttu-id="68687-117">일치 변수 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="68687-117">List of match variables.</span></span>

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

### <span data-ttu-id="68687-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="68687-118">-NegationCondition</span></span>
<span data-ttu-id="68687-119">이 조건이 부적정한 상태인지 아닌지에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="68687-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="68687-120">-연산자</span><span class="sxs-lookup"><span data-stu-id="68687-120">-Operator</span></span>
<span data-ttu-id="68687-121">일치할 연산자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="68687-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="68687-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="68687-122">-Transform</span></span>
<span data-ttu-id="68687-123">변환 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="68687-123">List of transforms.</span></span>

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

### <span data-ttu-id="68687-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68687-124">CommonParameters</span></span>
<span data-ttu-id="68687-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68687-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68687-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68687-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68687-127">입력</span><span class="sxs-lookup"><span data-stu-id="68687-127">INPUTS</span></span>

### <span data-ttu-id="68687-128">없음</span><span class="sxs-lookup"><span data-stu-id="68687-128">None</span></span>

## <span data-ttu-id="68687-129">출력</span><span class="sxs-lookup"><span data-stu-id="68687-129">OUTPUTS</span></span>

### <span data-ttu-id="68687-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="68687-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="68687-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68687-131">NOTES</span></span>

## <span data-ttu-id="68687-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68687-132">RELATED LINKS</span></span>
