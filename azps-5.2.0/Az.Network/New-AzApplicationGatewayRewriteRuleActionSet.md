---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358226"
---
# <span data-ttu-id="af964-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af964-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="af964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af964-102">SYNOPSIS</span></span>
<span data-ttu-id="af964-103">애플리케이션 게이트웨이에 대한 다시 작성 규칙 작업 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af964-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="af964-104">구문</span><span class="sxs-lookup"><span data-stu-id="af964-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af964-105">설명</span><span class="sxs-lookup"><span data-stu-id="af964-105">DESCRIPTION</span></span>
<span data-ttu-id="af964-106">**New-AzApplicationGatewayRewriteRuleActionSet** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 작업 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af964-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="af964-107">예제</span><span class="sxs-lookup"><span data-stu-id="af964-107">EXAMPLES</span></span>

### <span data-ttu-id="af964-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="af964-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="af964-109">이 명령은 다시 작성 규칙 작업 집합을 만들고 결과를 $action.</span><span class="sxs-lookup"><span data-stu-id="af964-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="af964-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af964-110">PARAMETERS</span></span>

### <span data-ttu-id="af964-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af964-111">-DefaultProfile</span></span>
<span data-ttu-id="af964-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af964-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af964-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af964-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="af964-114">요청 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="af964-114">List of request header configurations</span></span>

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

### <span data-ttu-id="af964-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af964-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="af964-116">응답 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="af964-116">List of response header configurations</span></span>

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

### <span data-ttu-id="af964-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="af964-117">-UrlConfiguration</span></span>
<span data-ttu-id="af964-118">작업 집합에 대한 URL 구성</span><span class="sxs-lookup"><span data-stu-id="af964-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af964-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af964-119">CommonParameters</span></span>
<span data-ttu-id="af964-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af964-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af964-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af964-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af964-122">입력</span><span class="sxs-lookup"><span data-stu-id="af964-122">INPUTS</span></span>

### <span data-ttu-id="af964-123">없음</span><span class="sxs-lookup"><span data-stu-id="af964-123">None</span></span>

## <span data-ttu-id="af964-124">출력</span><span class="sxs-lookup"><span data-stu-id="af964-124">OUTPUTS</span></span>

### <span data-ttu-id="af964-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af964-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="af964-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af964-126">NOTES</span></span>

## <span data-ttu-id="af964-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af964-127">RELATED LINKS</span></span>

[<span data-ttu-id="af964-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af964-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af964-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af964-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af964-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af964-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af964-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af964-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af964-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af964-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af964-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="af964-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="af964-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af964-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="af964-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="af964-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)