---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994070"
---
# <span data-ttu-id="f91df-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f91df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f91df-102">SYNOPSIS</span></span>
<span data-ttu-id="f91df-103">애플리케이션 게이트웨이의 다시 를 다시 던지기 규칙 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f91df-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="f91df-104">구문</span><span class="sxs-lookup"><span data-stu-id="f91df-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f91df-105">설명</span><span class="sxs-lookup"><span data-stu-id="f91df-105">DESCRIPTION</span></span>
<span data-ttu-id="f91df-106">애플리케이션 게이트웨이의 다시 를 다시 던지기 규칙 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f91df-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="f91df-107">예제</span><span class="sxs-lookup"><span data-stu-id="f91df-107">EXAMPLES</span></span>

### <span data-ttu-id="f91df-108">예제 1 : 특정 다시 기록 규칙 집합을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="f91df-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="f91df-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f91df-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f91df-110">두 번째 명령은 명령이라는 변수에 저장된 Application Gateway에서 RuleSet01이라는 다시 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f91df-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f91df-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f91df-111">PARAMETERS</span></span>

### <span data-ttu-id="f91df-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f91df-112">-ApplicationGateway</span></span>
<span data-ttu-id="f91df-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f91df-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f91df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91df-114">-DefaultProfile</span></span>
<span data-ttu-id="f91df-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f91df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91df-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f91df-116">-Name</span></span>
<span data-ttu-id="f91df-117">애플리케이션 게이트웨이 RewriteRuleSet의 이름</span><span class="sxs-lookup"><span data-stu-id="f91df-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f91df-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91df-118">CommonParameters</span></span>
<span data-ttu-id="f91df-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f91df-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91df-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f91df-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91df-121">입력</span><span class="sxs-lookup"><span data-stu-id="f91df-121">INPUTS</span></span>

### <span data-ttu-id="f91df-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f91df-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f91df-123">출력</span><span class="sxs-lookup"><span data-stu-id="f91df-123">OUTPUTS</span></span>

### <span data-ttu-id="f91df-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f91df-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f91df-125">NOTES</span></span>

## <span data-ttu-id="f91df-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f91df-126">RELATED LINKS</span></span>

[<span data-ttu-id="f91df-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f91df-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f91df-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f91df-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f91df-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f91df-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f91df-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f91df-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f91df-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f91df-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f91df-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
