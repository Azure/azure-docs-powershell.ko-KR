---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214867"
---
# <span data-ttu-id="2b016-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b016-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2b016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b016-102">SYNOPSIS</span></span>
<span data-ttu-id="2b016-103">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="2b016-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b016-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b016-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b016-105">DESCRIPTION</span></span>
<span data-ttu-id="2b016-106">**AzApplicationGatewayRewriteRuleSet Cmdlet은** Azure application gateway에 대 한 다시 쓰기 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="2b016-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b016-107">EXAMPLES</span></span>

### <span data-ttu-id="2b016-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b016-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="2b016-109">이 명령은 ruleset1 이라는 재작성 규칙 집합을 만들고 그 결과를 이름이 지정 된 변수 $ruleset에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="2b016-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b016-110">PARAMETERS</span></span>

### <span data-ttu-id="2b016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b016-111">-DefaultProfile</span></span>
<span data-ttu-id="2b016-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b016-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2b016-113">-Name</span></span>
<span data-ttu-id="2b016-114">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="2b016-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="2b016-115">-RewriteRule</span></span>
<span data-ttu-id="2b016-116">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="2b016-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b016-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b016-117">CommonParameters</span></span>
<span data-ttu-id="2b016-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b016-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b016-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b016-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b016-120">입력</span><span class="sxs-lookup"><span data-stu-id="2b016-120">INPUTS</span></span>

### <span data-ttu-id="2b016-121">않아야</span><span class="sxs-lookup"><span data-stu-id="2b016-121">None</span></span>

## <span data-ttu-id="2b016-122">출력</span><span class="sxs-lookup"><span data-stu-id="2b016-122">OUTPUTS</span></span>

### <span data-ttu-id="2b016-123">PSApplicationGatewayRewriteRuleSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2b016-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2b016-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2b016-124">NOTES</span></span>

## <span data-ttu-id="2b016-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b016-125">RELATED LINKS</span></span>

[<span data-ttu-id="2b016-126">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b016-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b016-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b016-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b016-128">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b016-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b016-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b016-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b016-130">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2b016-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2b016-131">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2b016-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2b016-132">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b016-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
