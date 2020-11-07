---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700383"
---
# <span data-ttu-id="31169-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31169-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="31169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31169-102">SYNOPSIS</span></span>
<span data-ttu-id="31169-103">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31169-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="31169-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31169-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31169-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31169-105">DESCRIPTION</span></span>
<span data-ttu-id="31169-106">**AzApplicationGatewayRewriteRuleSet Cmdlet은** Azure application gateway에 대 한 다시 쓰기 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31169-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="31169-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31169-107">EXAMPLES</span></span>

### <span data-ttu-id="31169-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="31169-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="31169-109">이 명령은 ruleset1 이라는 재작성 규칙 집합을 만들고 그 결과를 이름이 지정 된 변수 $ruleset에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="31169-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="31169-110">변수</span><span class="sxs-lookup"><span data-stu-id="31169-110">PARAMETERS</span></span>

### <span data-ttu-id="31169-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31169-111">-DefaultProfile</span></span>
<span data-ttu-id="31169-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31169-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31169-113">-이름</span><span class="sxs-lookup"><span data-stu-id="31169-113">-Name</span></span>
<span data-ttu-id="31169-114">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31169-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="31169-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="31169-115">-RewriteRule</span></span>
<span data-ttu-id="31169-116">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="31169-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="31169-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31169-117">CommonParameters</span></span>
<span data-ttu-id="31169-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31169-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31169-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31169-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31169-120">입력</span><span class="sxs-lookup"><span data-stu-id="31169-120">INPUTS</span></span>

### <span data-ttu-id="31169-121">않아야</span><span class="sxs-lookup"><span data-stu-id="31169-121">None</span></span>

## <span data-ttu-id="31169-122">출력</span><span class="sxs-lookup"><span data-stu-id="31169-122">OUTPUTS</span></span>

### <span data-ttu-id="31169-123">PSApplicationGatewayRewriteRuleSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="31169-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="31169-124">상속자</span><span class="sxs-lookup"><span data-stu-id="31169-124">NOTES</span></span>

## <span data-ttu-id="31169-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31169-125">RELATED LINKS</span></span>

[<span data-ttu-id="31169-126">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31169-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31169-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31169-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31169-128">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31169-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31169-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31169-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="31169-130">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31169-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="31169-131">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31169-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="31169-132">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="31169-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
