---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 7d7403fff78d04153f1c088cbdf41f61677e2e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871265"
---
# <span data-ttu-id="ec04a-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="ec04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec04a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec04a-103">응용 프로그램 게이트웨이에서 재작성 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="ec04a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec04a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec04a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec04a-105">DESCRIPTION</span></span>
<span data-ttu-id="ec04a-106">**AzApplicationGatewayRewriteRuleSet** Cmdlet은 Azure application gateway에서 재작성 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="ec04a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec04a-107">EXAMPLES</span></span>

### <span data-ttu-id="ec04a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec04a-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="ec04a-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec04a-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 RuleSet02 이라는 재작성 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ec04a-111">변수</span><span class="sxs-lookup"><span data-stu-id="ec04a-111">PARAMETERS</span></span>

### <span data-ttu-id="ec04a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec04a-112">-ApplicationGateway</span></span>
<span data-ttu-id="ec04a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec04a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ec04a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec04a-114">-DefaultProfile</span></span>
<span data-ttu-id="ec04a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec04a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ec04a-116">-Name</span></span>
<span data-ttu-id="ec04a-117">Application gateway RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="ec04a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec04a-118">CommonParameters</span></span>
<span data-ttu-id="ec04a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec04a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec04a-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec04a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec04a-121">입력</span><span class="sxs-lookup"><span data-stu-id="ec04a-121">INPUTS</span></span>

### <span data-ttu-id="ec04a-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec04a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec04a-123">출력</span><span class="sxs-lookup"><span data-stu-id="ec04a-123">OUTPUTS</span></span>

### <span data-ttu-id="ec04a-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec04a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec04a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ec04a-125">NOTES</span></span>

## <span data-ttu-id="ec04a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec04a-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec04a-127">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ec04a-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ec04a-129">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ec04a-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ec04a-131">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ec04a-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="ec04a-132">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ec04a-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="ec04a-133">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec04a-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
