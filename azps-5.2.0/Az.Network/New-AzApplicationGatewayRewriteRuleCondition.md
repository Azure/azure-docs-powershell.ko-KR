---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358198"
---
# <span data-ttu-id="4540a-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4540a-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="4540a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4540a-102">SYNOPSIS</span></span>
<span data-ttu-id="4540a-103">애플리케이션 게이트웨이에 대한 RewriteRule에 조건을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4540a-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="4540a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4540a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4540a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4540a-105">DESCRIPTION</span></span>
<span data-ttu-id="4540a-106">**AzApplicationGatewayRewriteRuleCondition cmdlet은** Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4540a-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="4540a-107">예제</span><span class="sxs-lookup"><span data-stu-id="4540a-107">EXAMPLES</span></span>

### <span data-ttu-id="4540a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4540a-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="4540a-109">이 명령은 다시 작성 규칙에 조건을 만들고 결과를 $condition.</span><span class="sxs-lookup"><span data-stu-id="4540a-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="4540a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4540a-110">PARAMETERS</span></span>

### <span data-ttu-id="4540a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4540a-111">-DefaultProfile</span></span>
<span data-ttu-id="4540a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4540a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4540a-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="4540a-113">-IgnoreCase</span></span>
<span data-ttu-id="4540a-114">패턴에서 대소문자 무시 플래그 설정</span><span class="sxs-lookup"><span data-stu-id="4540a-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4540a-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="4540a-115">-Negate</span></span>
<span data-ttu-id="4540a-116">조건 유효성 검사를 부인하기 위해 이 플래그 설정</span><span class="sxs-lookup"><span data-stu-id="4540a-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4540a-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="4540a-117">-Pattern</span></span>
<span data-ttu-id="4540a-118">변수 헤더에서 찾아야 하는 패턴</span><span class="sxs-lookup"><span data-stu-id="4540a-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4540a-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="4540a-119">-Variable</span></span>
<span data-ttu-id="4540a-120">조건을 설정할 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4540a-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4540a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4540a-121">CommonParameters</span></span>
<span data-ttu-id="4540a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4540a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4540a-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4540a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4540a-124">입력</span><span class="sxs-lookup"><span data-stu-id="4540a-124">INPUTS</span></span>

### <span data-ttu-id="4540a-125">없음</span><span class="sxs-lookup"><span data-stu-id="4540a-125">None</span></span>

## <span data-ttu-id="4540a-126">출력</span><span class="sxs-lookup"><span data-stu-id="4540a-126">OUTPUTS</span></span>

### <span data-ttu-id="4540a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4540a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="4540a-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4540a-128">NOTES</span></span>

## <span data-ttu-id="4540a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4540a-129">RELATED LINKS</span></span>
[<span data-ttu-id="4540a-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4540a-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4540a-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4540a-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4540a-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4540a-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4540a-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4540a-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4540a-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4540a-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4540a-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4540a-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="4540a-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4540a-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
