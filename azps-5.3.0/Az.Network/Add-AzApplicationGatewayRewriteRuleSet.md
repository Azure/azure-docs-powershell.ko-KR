---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492771"
---
# <span data-ttu-id="9f62b-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9f62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f62b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f62b-103">애플리케이션 게이트웨이에 다시 사용 규칙 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9f62b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f62b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f62b-105">설명</span><span class="sxs-lookup"><span data-stu-id="9f62b-105">DESCRIPTION</span></span>
<span data-ttu-id="9f62b-106">**Add-AzApplicationGatewayRewriteRuleSet** cmdlet은 애플리케이션 게이트웨이에 설정된 다시작성 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9f62b-107">예제</span><span class="sxs-lookup"><span data-stu-id="9f62b-107">EXAMPLES</span></span>

### <span data-ttu-id="9f62b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f62b-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="9f62b-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9f62b-110">두 번째 명령은 애플리케이션 게이트웨이에 설정된 다시 기록 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="9f62b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f62b-111">PARAMETERS</span></span>

### <span data-ttu-id="9f62b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f62b-112">-ApplicationGateway</span></span>
<span data-ttu-id="9f62b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f62b-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f62b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f62b-114">-DefaultProfile</span></span>
<span data-ttu-id="9f62b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f62b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9f62b-116">-Name</span></span>
<span data-ttu-id="9f62b-117">RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="9f62b-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="9f62b-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="9f62b-118">-RewriteRule</span></span>
<span data-ttu-id="9f62b-119">다시 사용 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="9f62b-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="9f62b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f62b-120">CommonParameters</span></span>
<span data-ttu-id="9f62b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f62b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f62b-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f62b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f62b-123">입력</span><span class="sxs-lookup"><span data-stu-id="9f62b-123">INPUTS</span></span>

### <span data-ttu-id="9f62b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f62b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f62b-125">출력</span><span class="sxs-lookup"><span data-stu-id="9f62b-125">OUTPUTS</span></span>

### <span data-ttu-id="9f62b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f62b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f62b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f62b-127">NOTES</span></span>

## <span data-ttu-id="9f62b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f62b-128">RELATED LINKS</span></span>

[<span data-ttu-id="9f62b-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9f62b-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9f62b-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9f62b-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9f62b-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9f62b-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9f62b-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9f62b-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9f62b-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f62b-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
