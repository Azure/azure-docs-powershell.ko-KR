---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213021"
---
# <span data-ttu-id="15d73-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="15d73-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="15d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d73-102">SYNOPSIS</span></span>
<span data-ttu-id="15d73-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 헤더 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="15d73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15d73-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d73-105">설명은</span><span class="sxs-lookup"><span data-stu-id="15d73-105">DESCRIPTION</span></span>
<span data-ttu-id="15d73-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration Cmdlet은** Azure application gateway에 대해 설정 된 재작성 규칙 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="15d73-107">예제의</span><span class="sxs-lookup"><span data-stu-id="15d73-107">EXAMPLES</span></span>

### <span data-ttu-id="15d73-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="15d73-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="15d73-109">이 명령은 재작성 규칙 헤더 구성을 만들고, 결과를 $hc 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="15d73-110">변수</span><span class="sxs-lookup"><span data-stu-id="15d73-110">PARAMETERS</span></span>

### <span data-ttu-id="15d73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d73-111">-DefaultProfile</span></span>
<span data-ttu-id="15d73-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d73-113">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="15d73-113">-HeaderName</span></span>
<span data-ttu-id="15d73-114">다시 쓸 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="15d73-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="15d73-115">-HeaderValue</span></span>
<span data-ttu-id="15d73-116">지정 된 헤더 이름에 대 한 집합에 대 한 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="15d73-117">이를 생략 하면 헤더가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="15d73-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d73-118">CommonParameters</span></span>
<span data-ttu-id="15d73-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d73-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d73-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d73-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d73-121">입력</span><span class="sxs-lookup"><span data-stu-id="15d73-121">INPUTS</span></span>

### <span data-ttu-id="15d73-122">않아야</span><span class="sxs-lookup"><span data-stu-id="15d73-122">None</span></span>

## <span data-ttu-id="15d73-123">출력</span><span class="sxs-lookup"><span data-stu-id="15d73-123">OUTPUTS</span></span>

### <span data-ttu-id="15d73-124">Microsoft. 네트워크. Psapplication의 Header구성</span><span class="sxs-lookup"><span data-stu-id="15d73-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="15d73-125">상속자</span><span class="sxs-lookup"><span data-stu-id="15d73-125">NOTES</span></span>

## <span data-ttu-id="15d73-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15d73-126">RELATED LINKS</span></span>

[<span data-ttu-id="15d73-127">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15d73-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="15d73-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15d73-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="15d73-129">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15d73-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="15d73-130">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15d73-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="15d73-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15d73-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="15d73-132">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="15d73-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="15d73-133">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="15d73-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
