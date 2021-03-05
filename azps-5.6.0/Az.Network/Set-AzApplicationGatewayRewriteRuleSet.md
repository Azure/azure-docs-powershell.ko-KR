---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 934c69071e90ebb1a38bf4e1fda5e631364ab87b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003467"
---
# <span data-ttu-id="fad62-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fad62-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="fad62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fad62-102">SYNOPSIS</span></span>
<span data-ttu-id="fad62-103">애플리케이션 게이트웨이에 대한 다시 덮기 규칙 집합을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="fad62-104">구문</span><span class="sxs-lookup"><span data-stu-id="fad62-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fad62-105">설명</span><span class="sxs-lookup"><span data-stu-id="fad62-105">DESCRIPTION</span></span>
<span data-ttu-id="fad62-106">**Set-AzApplicationGatewayRewriteRuleSet** cmdlet은 요청 라우팅 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="fad62-107">예제</span><span class="sxs-lookup"><span data-stu-id="fad62-107">EXAMPLES</span></span>

### <span data-ttu-id="fad62-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fad62-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="fad62-109">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fad62-110">두 번째 명령은 애플리케이션 게이트웨이에 대한 다시 기록 규칙 집합을 수정하여 $rule 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="fad62-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fad62-111">PARAMETERS</span></span>

### <span data-ttu-id="fad62-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad62-112">-ApplicationGateway</span></span>
<span data-ttu-id="fad62-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad62-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fad62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad62-114">-DefaultProfile</span></span>
<span data-ttu-id="fad62-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fad62-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fad62-116">-Name</span></span>
<span data-ttu-id="fad62-117">RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="fad62-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="fad62-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="fad62-118">-RewriteRule</span></span>
<span data-ttu-id="fad62-119">다시 를 다시 던지기 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="fad62-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="fad62-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad62-120">CommonParameters</span></span>
<span data-ttu-id="fad62-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fad62-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad62-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fad62-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad62-123">입력</span><span class="sxs-lookup"><span data-stu-id="fad62-123">INPUTS</span></span>

### <span data-ttu-id="fad62-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad62-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fad62-125">출력</span><span class="sxs-lookup"><span data-stu-id="fad62-125">OUTPUTS</span></span>

### <span data-ttu-id="fad62-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad62-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fad62-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fad62-127">NOTES</span></span>

## <span data-ttu-id="fad62-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fad62-128">RELATED LINKS</span></span>

[<span data-ttu-id="fad62-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fad62-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fad62-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fad62-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fad62-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fad62-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fad62-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fad62-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fad62-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fad62-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="fad62-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fad62-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="fad62-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fad62-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
