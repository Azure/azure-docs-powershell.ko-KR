---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358884"
---
# <span data-ttu-id="701a8-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="701a8-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="701a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="701a8-102">SYNOPSIS</span></span>
<span data-ttu-id="701a8-103">애플리케이션 게이트웨이에 대한 다시 작성 규칙 헤더 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="701a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="701a8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="701a8-105">설명</span><span class="sxs-lookup"><span data-stu-id="701a8-105">DESCRIPTION</span></span>
<span data-ttu-id="701a8-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 작업 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="701a8-107">예제</span><span class="sxs-lookup"><span data-stu-id="701a8-107">EXAMPLES</span></span>

### <span data-ttu-id="701a8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="701a8-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="701a8-109">이 명령은 다시 작성 규칙 헤더 구성을 만들고 결과를 $hc.</span><span class="sxs-lookup"><span data-stu-id="701a8-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="701a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="701a8-110">PARAMETERS</span></span>

### <span data-ttu-id="701a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="701a8-111">-DefaultProfile</span></span>
<span data-ttu-id="701a8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="701a8-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="701a8-113">-HeaderName</span></span>
<span data-ttu-id="701a8-114">다시 입력할 헤더의 이름</span><span class="sxs-lookup"><span data-stu-id="701a8-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="701a8-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="701a8-115">-HeaderValue</span></span>
<span data-ttu-id="701a8-116">지정한 헤더 이름에 대한 집합에 대한 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="701a8-117">이 헤더를 생략하면 헤더가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="701a8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701a8-118">CommonParameters</span></span>
<span data-ttu-id="701a8-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="701a8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701a8-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="701a8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701a8-121">입력</span><span class="sxs-lookup"><span data-stu-id="701a8-121">INPUTS</span></span>

### <span data-ttu-id="701a8-122">없음</span><span class="sxs-lookup"><span data-stu-id="701a8-122">None</span></span>

## <span data-ttu-id="701a8-123">출력</span><span class="sxs-lookup"><span data-stu-id="701a8-123">OUTPUTS</span></span>

### <span data-ttu-id="701a8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="701a8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="701a8-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="701a8-125">NOTES</span></span>

## <span data-ttu-id="701a8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="701a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="701a8-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="701a8-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="701a8-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="701a8-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="701a8-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="701a8-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="701a8-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="701a8-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="701a8-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="701a8-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="701a8-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="701a8-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="701a8-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="701a8-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
