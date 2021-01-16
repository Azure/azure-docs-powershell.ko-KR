---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341649"
---
# <span data-ttu-id="b7199-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7199-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b7199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7199-102">SYNOPSIS</span></span>
<span data-ttu-id="b7199-103">애플리케이션 게이트웨이에서 다시 필기 규칙 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b7199-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="b7199-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7199-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7199-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7199-105">DESCRIPTION</span></span>
<span data-ttu-id="b7199-106">**Remove-AzApplicationGatewayRewriteRuleSet** cmdlet은 Azure 애플리케이션 게이트웨이에서 재작성 규칙 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b7199-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="b7199-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7199-107">EXAMPLES</span></span>

### <span data-ttu-id="b7199-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7199-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="b7199-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b7199-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b7199-110">두 번째 명령은 규칙 집합에 저장된 애플리케이션 게이트웨이에서 RuleSet02라는 다시 사용 규칙 집합을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b7199-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b7199-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7199-111">PARAMETERS</span></span>

### <span data-ttu-id="b7199-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7199-112">-ApplicationGateway</span></span>
<span data-ttu-id="b7199-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7199-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b7199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7199-114">-DefaultProfile</span></span>
<span data-ttu-id="b7199-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7199-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7199-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b7199-116">-Name</span></span>
<span data-ttu-id="b7199-117">Application Gateway RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="b7199-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b7199-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7199-118">CommonParameters</span></span>
<span data-ttu-id="b7199-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7199-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7199-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7199-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7199-121">입력</span><span class="sxs-lookup"><span data-stu-id="b7199-121">INPUTS</span></span>

### <span data-ttu-id="b7199-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7199-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7199-123">출력</span><span class="sxs-lookup"><span data-stu-id="b7199-123">OUTPUTS</span></span>

### <span data-ttu-id="b7199-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7199-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7199-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7199-125">NOTES</span></span>

## <span data-ttu-id="b7199-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7199-126">RELATED LINKS</span></span>

[<span data-ttu-id="b7199-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7199-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7199-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7199-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7199-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7199-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7199-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7199-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b7199-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b7199-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b7199-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b7199-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b7199-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7199-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
