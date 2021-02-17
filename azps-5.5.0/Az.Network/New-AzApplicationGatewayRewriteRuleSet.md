---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206813"
---
# <span data-ttu-id="93f1a-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="93f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="93f1a-103">애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93f1a-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="93f1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="93f1a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f1a-105">설명</span><span class="sxs-lookup"><span data-stu-id="93f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="93f1a-106">**New-AzApplicationGatewayRewriteRuleSet** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93f1a-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="93f1a-107">예제</span><span class="sxs-lookup"><span data-stu-id="93f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="93f1a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="93f1a-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="93f1a-109">이 명령은 ruleset1이라는 다시 작성 규칙 집합을 만들고 결과를 $ruleset.</span><span class="sxs-lookup"><span data-stu-id="93f1a-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="93f1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="93f1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f1a-111">-DefaultProfile</span></span>
<span data-ttu-id="93f1a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93f1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f1a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="93f1a-113">-Name</span></span>
<span data-ttu-id="93f1a-114">RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="93f1a-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="93f1a-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="93f1a-115">-RewriteRule</span></span>
<span data-ttu-id="93f1a-116">다시 사용 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="93f1a-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="93f1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f1a-117">CommonParameters</span></span>
<span data-ttu-id="93f1a-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93f1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f1a-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93f1a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f1a-120">입력</span><span class="sxs-lookup"><span data-stu-id="93f1a-120">INPUTS</span></span>

### <span data-ttu-id="93f1a-121">없음</span><span class="sxs-lookup"><span data-stu-id="93f1a-121">None</span></span>

## <span data-ttu-id="93f1a-122">출력</span><span class="sxs-lookup"><span data-stu-id="93f1a-122">OUTPUTS</span></span>

### <span data-ttu-id="93f1a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="93f1a-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93f1a-124">NOTES</span></span>

## <span data-ttu-id="93f1a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93f1a-125">RELATED LINKS</span></span>

[<span data-ttu-id="93f1a-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93f1a-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93f1a-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93f1a-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93f1a-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="93f1a-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="93f1a-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="93f1a-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="93f1a-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f1a-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
