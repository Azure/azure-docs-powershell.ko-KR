---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870502"
---
# <span data-ttu-id="8e990-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="8e990-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="8e990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e990-102">SYNOPSIS</span></span>
<span data-ttu-id="8e990-103">응용 프로그램 게이트웨이의 RewriteRule에 조건을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="8e990-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e990-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e990-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e990-105">DESCRIPTION</span></span>
<span data-ttu-id="8e990-106">**AzApplicationGatewayRewriteRuleCondition Cmdlet은** Azure application gateway에 대 한 재작성 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="8e990-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e990-107">EXAMPLES</span></span>

### <span data-ttu-id="8e990-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e990-108">Example 1</span></span>
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
<span data-ttu-id="8e990-109">이 명령은 재작성 규칙에 조건을 만들고 결과를 $condition 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="8e990-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e990-110">PARAMETERS</span></span>

### <span data-ttu-id="8e990-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e990-111">-DefaultProfile</span></span>
<span data-ttu-id="8e990-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e990-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="8e990-113">-IgnoreCase</span></span>
<span data-ttu-id="8e990-114">이 플래그를 설정 하 여 패턴의 대/소문자를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="8e990-115">-음수</span><span class="sxs-lookup"><span data-stu-id="8e990-115">-Negate</span></span>
<span data-ttu-id="8e990-116">조건 유효성 검사를 무효화 하도록이 플래그 설정</span><span class="sxs-lookup"><span data-stu-id="8e990-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="8e990-117">-패턴</span><span class="sxs-lookup"><span data-stu-id="8e990-117">-Pattern</span></span>
<span data-ttu-id="8e990-118">변수 머리글에서 찾을 패턴</span><span class="sxs-lookup"><span data-stu-id="8e990-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="8e990-119">-변수</span><span class="sxs-lookup"><span data-stu-id="8e990-119">-Variable</span></span>
<span data-ttu-id="8e990-120">조건을 설정할 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="8e990-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e990-121">CommonParameters</span></span>
<span data-ttu-id="8e990-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e990-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8e990-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e990-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e990-124">입력</span><span class="sxs-lookup"><span data-stu-id="8e990-124">INPUTS</span></span>

### <span data-ttu-id="8e990-125">않아야</span><span class="sxs-lookup"><span data-stu-id="8e990-125">None</span></span>

## <span data-ttu-id="8e990-126">출력</span><span class="sxs-lookup"><span data-stu-id="8e990-126">OUTPUTS</span></span>

### <span data-ttu-id="8e990-127">PSApplicationGatewayRewriteRuleCondition에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8e990-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="8e990-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8e990-128">NOTES</span></span>

## <span data-ttu-id="8e990-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e990-129">RELATED LINKS</span></span>
[<span data-ttu-id="8e990-130">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e990-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e990-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e990-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e990-132">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e990-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e990-133">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e990-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e990-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e990-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e990-135">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8e990-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8e990-136">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8e990-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
