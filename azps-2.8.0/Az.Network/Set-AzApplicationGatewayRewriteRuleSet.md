---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869597"
---
# <span data-ttu-id="6c2c3-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="6c2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2c3-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 집합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="6c2c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c2c3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c2c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6c2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2c3-106">**Set-AzApplicationGatewayRewriteRuleSet** cmdlet은 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6c2c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6c2c3-107">EXAMPLES</span></span>

### <span data-ttu-id="6c2c3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c2c3-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="6c2c3-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6c2c3-110">두 번째 명령은 $rule 변수에 지정 된 다시 쓰기 규칙을 사용 하도록 응용 프로그램 게이트웨이에 대 한 다시 작성 규칙 집합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="6c2c3-111">변수</span><span class="sxs-lookup"><span data-stu-id="6c2c3-111">PARAMETERS</span></span>

### <span data-ttu-id="6c2c3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c2c3-112">-ApplicationGateway</span></span>
<span data-ttu-id="6c2c3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c2c3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6c2c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2c3-114">-DefaultProfile</span></span>
<span data-ttu-id="6c2c3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2c3-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6c2c3-116">-Name</span></span>
<span data-ttu-id="6c2c3-117">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="6c2c3-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="6c2c3-118">-RewriteRule</span></span>
<span data-ttu-id="6c2c3-119">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="6c2c3-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="6c2c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2c3-120">CommonParameters</span></span>
<span data-ttu-id="6c2c3-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2c3-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c2c3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2c3-123">입력</span><span class="sxs-lookup"><span data-stu-id="6c2c3-123">INPUTS</span></span>

### <span data-ttu-id="6c2c3-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c2c3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c2c3-125">출력</span><span class="sxs-lookup"><span data-stu-id="6c2c3-125">OUTPUTS</span></span>

### <span data-ttu-id="6c2c3-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c2c3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c2c3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="6c2c3-127">NOTES</span></span>

## <span data-ttu-id="6c2c3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c2c3-128">RELATED LINKS</span></span>

[<span data-ttu-id="6c2c3-129">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6c2c3-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6c2c3-131">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6c2c3-132">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6c2c3-133">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6c2c3-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="6c2c3-134">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6c2c3-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="6c2c3-135">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c2c3-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
