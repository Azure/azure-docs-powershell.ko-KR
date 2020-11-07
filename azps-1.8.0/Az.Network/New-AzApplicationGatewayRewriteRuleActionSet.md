---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700388"
---
# <span data-ttu-id="45f5c-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="45f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="45f5c-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 actionset을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45f5c-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="45f5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45f5c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45f5c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="45f5c-106">**AzApplicationGatewayRewriteRuleActionSet Cmdlet은** Azure application gateway에 대 한 재작성 규칙 actionset을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45f5c-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="45f5c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="45f5c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="45f5c-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="45f5c-109">이 명령은 재작성 규칙 actionset을 만들고 그 결과를 $action 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f5c-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="45f5c-110">변수</span><span class="sxs-lookup"><span data-stu-id="45f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="45f5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f5c-111">-DefaultProfile</span></span>
<span data-ttu-id="45f5c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45f5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45f5c-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="45f5c-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="45f5c-114">요청 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="45f5c-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45f5c-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="45f5c-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="45f5c-116">응답 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="45f5c-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45f5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f5c-117">CommonParameters</span></span>
<span data-ttu-id="45f5c-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f5c-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45f5c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f5c-120">입력</span><span class="sxs-lookup"><span data-stu-id="45f5c-120">INPUTS</span></span>

### <span data-ttu-id="45f5c-121">않아야</span><span class="sxs-lookup"><span data-stu-id="45f5c-121">None</span></span>

## <span data-ttu-id="45f5c-122">출력</span><span class="sxs-lookup"><span data-stu-id="45f5c-122">OUTPUTS</span></span>

### <span data-ttu-id="45f5c-123">PSApplicationGatewayRewriteRuleActionSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="45f5c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="45f5c-124">상속자</span><span class="sxs-lookup"><span data-stu-id="45f5c-124">NOTES</span></span>

## <span data-ttu-id="45f5c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45f5c-125">RELATED LINKS</span></span>

[<span data-ttu-id="45f5c-126">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="45f5c-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="45f5c-128">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="45f5c-129">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="45f5c-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45f5c-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="45f5c-131">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="45f5c-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="45f5c-132">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="45f5c-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
