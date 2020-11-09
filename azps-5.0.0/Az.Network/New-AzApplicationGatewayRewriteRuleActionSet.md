---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310271"
---
# <span data-ttu-id="1d471-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1d471-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="1d471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d471-102">SYNOPSIS</span></span>
<span data-ttu-id="1d471-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 동작 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d471-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="1d471-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d471-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d471-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d471-105">DESCRIPTION</span></span>
<span data-ttu-id="1d471-106">**AzApplicationGatewayRewriteRuleActionSet Cmdlet은** Azure application gateway에 대해 설정 된 재작성 규칙 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d471-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="1d471-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d471-107">EXAMPLES</span></span>

### <span data-ttu-id="1d471-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d471-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="1d471-109">이 명령은 재작성 규칙 작업 집합을 만들고 그 결과를 $action 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d471-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="1d471-110">변수</span><span class="sxs-lookup"><span data-stu-id="1d471-110">PARAMETERS</span></span>

### <span data-ttu-id="1d471-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d471-111">-DefaultProfile</span></span>
<span data-ttu-id="1d471-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d471-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d471-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d471-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="1d471-114">요청 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="1d471-114">List of request header configurations</span></span>

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

### <span data-ttu-id="1d471-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d471-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="1d471-116">응답 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="1d471-116">List of response header configurations</span></span>

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

### <span data-ttu-id="1d471-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d471-117">-UrlConfiguration</span></span>
<span data-ttu-id="1d471-118">Action set의 Url 구성</span><span class="sxs-lookup"><span data-stu-id="1d471-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="1d471-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d471-119">CommonParameters</span></span>
<span data-ttu-id="1d471-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d471-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d471-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d471-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d471-122">입력</span><span class="sxs-lookup"><span data-stu-id="1d471-122">INPUTS</span></span>

### <span data-ttu-id="1d471-123">않아야</span><span class="sxs-lookup"><span data-stu-id="1d471-123">None</span></span>

## <span data-ttu-id="1d471-124">출력</span><span class="sxs-lookup"><span data-stu-id="1d471-124">OUTPUTS</span></span>

### <span data-ttu-id="1d471-125">PSApplicationGatewayRewriteRuleActionSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1d471-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="1d471-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1d471-126">NOTES</span></span>

## <span data-ttu-id="1d471-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d471-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d471-128">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d471-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1d471-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d471-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1d471-130">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d471-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1d471-131">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d471-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1d471-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d471-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="1d471-133">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1d471-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="1d471-134">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d471-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="1d471-135">새로운 AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d471-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)