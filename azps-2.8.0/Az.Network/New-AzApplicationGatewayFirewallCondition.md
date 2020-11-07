---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: aec627fdc8889d6bcfc4fb8e7762eb3be7bf0432
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870018"
---
# <span data-ttu-id="66017-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="66017-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="66017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66017-102">SYNOPSIS</span></span>
<span data-ttu-id="66017-103">사용자 지정 규칙에 대 한 일치 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66017-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="66017-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66017-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66017-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66017-105">DESCRIPTION</span></span>
<span data-ttu-id="66017-106">**AzApplicationGatewayFirewallCondition** 는 방화벽 사용자 지정 규칙에 대 한 일치 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66017-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="66017-107">예제의</span><span class="sxs-lookup"><span data-stu-id="66017-107">EXAMPLES</span></span>

### <span data-ttu-id="66017-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="66017-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="66017-109">명령에서 $variable에 정의 된 match 변수를 사용 하 여 새 일치 조건을 만들고, 연산자가 Contains이 고 음수 조건이 false 이면, Transfroms를 포함 하 여 일치 값이 abc 및 cde입니다.</span><span class="sxs-lookup"><span data-stu-id="66017-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="66017-110">새 일치 조건이 $condition에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66017-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="66017-111">변수</span><span class="sxs-lookup"><span data-stu-id="66017-111">PARAMETERS</span></span>

### <span data-ttu-id="66017-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66017-112">-DefaultProfile</span></span>
<span data-ttu-id="66017-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66017-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66017-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="66017-114">-MatchValue</span></span>
<span data-ttu-id="66017-115">값 일치</span><span class="sxs-lookup"><span data-stu-id="66017-115">Match value.</span></span>

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

### <span data-ttu-id="66017-116">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="66017-116">-MatchVariable</span></span>
<span data-ttu-id="66017-117">일치 변수 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="66017-117">List of match variables.</span></span>

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

### <span data-ttu-id="66017-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="66017-118">-NegationCondition</span></span>
<span data-ttu-id="66017-119">이 조건이 음수 인지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="66017-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="66017-120">-연산자</span><span class="sxs-lookup"><span data-stu-id="66017-120">-Operator</span></span>
<span data-ttu-id="66017-121">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="66017-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="66017-122">-변환</span><span class="sxs-lookup"><span data-stu-id="66017-122">-Transform</span></span>
<span data-ttu-id="66017-123">변형 목록.</span><span class="sxs-lookup"><span data-stu-id="66017-123">List of transforms.</span></span>

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

### <span data-ttu-id="66017-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66017-124">CommonParameters</span></span>
<span data-ttu-id="66017-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66017-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66017-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66017-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66017-127">입력</span><span class="sxs-lookup"><span data-stu-id="66017-127">INPUTS</span></span>

### <span data-ttu-id="66017-128">않아야</span><span class="sxs-lookup"><span data-stu-id="66017-128">None</span></span>

## <span data-ttu-id="66017-129">출력</span><span class="sxs-lookup"><span data-stu-id="66017-129">OUTPUTS</span></span>

### <span data-ttu-id="66017-130">PSApplicationGatewayFirewallCondition에 대 한.</span><span class="sxs-lookup"><span data-stu-id="66017-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="66017-131">상속자</span><span class="sxs-lookup"><span data-stu-id="66017-131">NOTES</span></span>

## <span data-ttu-id="66017-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66017-132">RELATED LINKS</span></span>
