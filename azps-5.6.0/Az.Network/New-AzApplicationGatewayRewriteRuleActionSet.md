---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 2c5fa5f4c12a44d1efc12e75dfa3901dce061f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008768"
---
# <span data-ttu-id="7280d-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7280d-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="7280d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7280d-102">SYNOPSIS</span></span>
<span data-ttu-id="7280d-103">애플리케이션 게이트웨이에 대한 다시 작성 규칙 작업 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7280d-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="7280d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7280d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7280d-105">설명</span><span class="sxs-lookup"><span data-stu-id="7280d-105">DESCRIPTION</span></span>
<span data-ttu-id="7280d-106">**New-AzApplicationGatewayRewriteRuleActionSet** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 작업 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7280d-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="7280d-107">예제</span><span class="sxs-lookup"><span data-stu-id="7280d-107">EXAMPLES</span></span>

### <span data-ttu-id="7280d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7280d-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="7280d-109">이 명령은 다시 작성 규칙 작업 집합을 만들고 결과를 $action.</span><span class="sxs-lookup"><span data-stu-id="7280d-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="7280d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7280d-110">PARAMETERS</span></span>

### <span data-ttu-id="7280d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7280d-111">-DefaultProfile</span></span>
<span data-ttu-id="7280d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7280d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7280d-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7280d-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="7280d-114">요청 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="7280d-114">List of request header configurations</span></span>

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

### <span data-ttu-id="7280d-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7280d-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="7280d-116">응답 헤더 구성 목록</span><span class="sxs-lookup"><span data-stu-id="7280d-116">List of response header configurations</span></span>

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

### <span data-ttu-id="7280d-117">-URLConfiguration</span><span class="sxs-lookup"><span data-stu-id="7280d-117">-UrlConfiguration</span></span>
<span data-ttu-id="7280d-118">작업 집합에 대한 URL 구성</span><span class="sxs-lookup"><span data-stu-id="7280d-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="7280d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7280d-119">CommonParameters</span></span>
<span data-ttu-id="7280d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7280d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7280d-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7280d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7280d-122">입력</span><span class="sxs-lookup"><span data-stu-id="7280d-122">INPUTS</span></span>

### <span data-ttu-id="7280d-123">없음</span><span class="sxs-lookup"><span data-stu-id="7280d-123">None</span></span>

## <span data-ttu-id="7280d-124">출력</span><span class="sxs-lookup"><span data-stu-id="7280d-124">OUTPUTS</span></span>

### <span data-ttu-id="7280d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7280d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="7280d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7280d-126">NOTES</span></span>

## <span data-ttu-id="7280d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7280d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7280d-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7280d-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7280d-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7280d-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7280d-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7280d-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7280d-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7280d-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7280d-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7280d-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7280d-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7280d-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7280d-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7280d-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="7280d-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7280d-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)