---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878429"
---
# <span data-ttu-id="93301-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93301-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="93301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93301-102">SYNOPSIS</span></span>
<span data-ttu-id="93301-103">응용 프로그램 게이트웨이의 다시 작성 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93301-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="93301-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93301-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93301-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93301-105">DESCRIPTION</span></span>
<span data-ttu-id="93301-106">응용 프로그램 게이트웨이의 다시 작성 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93301-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="93301-107">예제의</span><span class="sxs-lookup"><span data-stu-id="93301-107">EXAMPLES</span></span>

### <span data-ttu-id="93301-108">예제 1: 특정 재작성 규칙 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="93301-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="93301-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="93301-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="93301-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 RuleSet01 이라는 재작성 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93301-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="93301-111">변수</span><span class="sxs-lookup"><span data-stu-id="93301-111">PARAMETERS</span></span>

### <span data-ttu-id="93301-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93301-112">-ApplicationGateway</span></span>
<span data-ttu-id="93301-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93301-113">The applicationGateway</span></span>

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

### <span data-ttu-id="93301-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93301-114">-DefaultProfile</span></span>
<span data-ttu-id="93301-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93301-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93301-116">-이름</span><span class="sxs-lookup"><span data-stu-id="93301-116">-Name</span></span>
<span data-ttu-id="93301-117">Application gateway RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93301-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="93301-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93301-118">CommonParameters</span></span>
<span data-ttu-id="93301-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93301-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93301-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93301-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93301-121">입력</span><span class="sxs-lookup"><span data-stu-id="93301-121">INPUTS</span></span>

### <span data-ttu-id="93301-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93301-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93301-123">출력</span><span class="sxs-lookup"><span data-stu-id="93301-123">OUTPUTS</span></span>

### <span data-ttu-id="93301-124">PSApplicationGatewayRewriteRuleSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="93301-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="93301-125">상속자</span><span class="sxs-lookup"><span data-stu-id="93301-125">NOTES</span></span>

## <span data-ttu-id="93301-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93301-126">RELATED LINKS</span></span>

[<span data-ttu-id="93301-127">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93301-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93301-128">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93301-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93301-129">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93301-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93301-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="93301-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="93301-131">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="93301-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="93301-132">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="93301-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="93301-133">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="93301-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
