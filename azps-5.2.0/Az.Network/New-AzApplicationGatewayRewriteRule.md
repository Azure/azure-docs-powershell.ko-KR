---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358233"
---
# <span data-ttu-id="2f93b-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2f93b-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="2f93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f93b-103">애플리케이션 게이트웨이에 대한 다시 작성 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f93b-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="2f93b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f93b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f93b-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f93b-105">DESCRIPTION</span></span>
<span data-ttu-id="2f93b-106">**New-AzApplicationGatewayRewriteRule** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f93b-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="2f93b-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f93b-107">EXAMPLES</span></span>

### <span data-ttu-id="2f93b-108">예제 1: 애플리케이션 게이트웨이에 대한 다시 작성 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2f93b-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="2f93b-109">이 명령은 rule1이라는 다시 작성 규칙을 만들고 결과를 $rule.</span><span class="sxs-lookup"><span data-stu-id="2f93b-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="2f93b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f93b-110">PARAMETERS</span></span>

### <span data-ttu-id="2f93b-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-111">-ActionSet</span></span>
<span data-ttu-id="2f93b-112">다시 덮기 규칙의 ActionSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f93b-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="2f93b-113">-Condition</span></span>
<span data-ttu-id="2f93b-114">다시 필기 규칙을 실행할 조건</span><span class="sxs-lookup"><span data-stu-id="2f93b-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f93b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f93b-115">-DefaultProfile</span></span>
<span data-ttu-id="2f93b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f93b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f93b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f93b-117">-Name</span></span>
<span data-ttu-id="2f93b-118">RewriteRule의 이름</span><span class="sxs-lookup"><span data-stu-id="2f93b-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="2f93b-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="2f93b-119">-RuleSequence</span></span>
<span data-ttu-id="2f93b-120">다시 사용 규칙 집합에서 이 다시 필기 규칙의 규칙 순서</span><span class="sxs-lookup"><span data-stu-id="2f93b-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f93b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f93b-121">CommonParameters</span></span>
<span data-ttu-id="2f93b-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f93b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f93b-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f93b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f93b-124">입력</span><span class="sxs-lookup"><span data-stu-id="2f93b-124">INPUTS</span></span>

### <span data-ttu-id="2f93b-125">없음</span><span class="sxs-lookup"><span data-stu-id="2f93b-125">None</span></span>

## <span data-ttu-id="2f93b-126">출력</span><span class="sxs-lookup"><span data-stu-id="2f93b-126">OUTPUTS</span></span>

### <span data-ttu-id="2f93b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2f93b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="2f93b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f93b-128">NOTES</span></span>

## <span data-ttu-id="2f93b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f93b-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f93b-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f93b-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f93b-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f93b-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f93b-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f93b-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2f93b-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2f93b-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f93b-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
