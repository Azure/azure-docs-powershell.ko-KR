---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 8bd540c30551451bd729126c35c4d778c700591f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001120"
---
# <span data-ttu-id="cb22a-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="cb22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb22a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb22a-103">애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb22a-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="cb22a-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb22a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb22a-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb22a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb22a-106">**New-AzApplicationGatewayRewriteRuleSet** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb22a-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="cb22a-107">예제</span><span class="sxs-lookup"><span data-stu-id="cb22a-107">EXAMPLES</span></span>

### <span data-ttu-id="cb22a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb22a-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="cb22a-109">이 명령은 ruleet1이라는 다시 작성 규칙 집합을 만들고 결과를 $ruleset.</span><span class="sxs-lookup"><span data-stu-id="cb22a-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="cb22a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb22a-110">PARAMETERS</span></span>

### <span data-ttu-id="cb22a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb22a-111">-DefaultProfile</span></span>
<span data-ttu-id="cb22a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb22a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb22a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cb22a-113">-Name</span></span>
<span data-ttu-id="cb22a-114">RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="cb22a-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="cb22a-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb22a-115">-RewriteRule</span></span>
<span data-ttu-id="cb22a-116">다시 를 다시 던지기 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="cb22a-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="cb22a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb22a-117">CommonParameters</span></span>
<span data-ttu-id="cb22a-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb22a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb22a-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb22a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb22a-120">입력</span><span class="sxs-lookup"><span data-stu-id="cb22a-120">INPUTS</span></span>

### <span data-ttu-id="cb22a-121">없음</span><span class="sxs-lookup"><span data-stu-id="cb22a-121">None</span></span>

## <span data-ttu-id="cb22a-122">출력</span><span class="sxs-lookup"><span data-stu-id="cb22a-122">OUTPUTS</span></span>

### <span data-ttu-id="cb22a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="cb22a-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb22a-124">NOTES</span></span>

## <span data-ttu-id="cb22a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb22a-125">RELATED LINKS</span></span>

[<span data-ttu-id="cb22a-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cb22a-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cb22a-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cb22a-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cb22a-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb22a-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="cb22a-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb22a-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="cb22a-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb22a-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
