---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211584"
---
# <span data-ttu-id="a5a00-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5a00-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="a5a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a00-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a00-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 url 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="a5a00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5a00-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5a00-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a00-106">**AzApplicationGatewayRewriteRuleUrlConfiguration Cmdlet은** Azure application gateway에 대 한 재작성 규칙 url 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a5a00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5a00-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a00-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5a00-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="a5a00-109">이 명령은 재작성 규칙 url 구성을 만들고 결과를 $urlConfiguration 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="a5a00-110">기존 UrlConfiguration을 업데이트 하려는 경우 새 UrlConfiguration을 만들고 새 UrlConfiguration을 다시 작성 규칙 동작 집합의 UrlConfiguration 속성에 할당 하 여이 구성을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="a5a00-111">변수</span><span class="sxs-lookup"><span data-stu-id="a5a00-111">PARAMETERS</span></span>

### <span data-ttu-id="a5a00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a00-112">-DefaultProfile</span></span>
<span data-ttu-id="a5a00-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a00-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="a5a00-114">-ModifiedPath</span></span>
<span data-ttu-id="a5a00-115">Url 경로 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-115">Url path value.</span></span>

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

### <span data-ttu-id="a5a00-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="a5a00-116">-ModifiedQueryString</span></span>
<span data-ttu-id="a5a00-117">Url 쿼리 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-117">Url query string value.</span></span>

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

### <span data-ttu-id="a5a00-118">-경로 조정</span><span class="sxs-lookup"><span data-stu-id="a5a00-118">-Reroute</span></span>
<span data-ttu-id="a5a00-119">경로 기반 요청 라우팅 규칙에서 수정 된 경로를 사용 하 여 제공 되는 url 경로 맵을 다시 평가 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a00-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a00-120">CommonParameters</span></span>
<span data-ttu-id="a5a00-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a00-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a00-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5a00-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a00-123">입력</span><span class="sxs-lookup"><span data-stu-id="a5a00-123">INPUTS</span></span>

### <span data-ttu-id="a5a00-124">않아야</span><span class="sxs-lookup"><span data-stu-id="a5a00-124">None</span></span>

## <span data-ttu-id="a5a00-125">출력</span><span class="sxs-lookup"><span data-stu-id="a5a00-125">OUTPUTS</span></span>

### <span data-ttu-id="a5a00-126">Microsoft. 네트워크. Psapplication게이트웨이 Urlconfiguration</span><span class="sxs-lookup"><span data-stu-id="a5a00-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="a5a00-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a5a00-127">NOTES</span></span>

## <span data-ttu-id="a5a00-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5a00-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5a00-129">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5a00-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5a00-131">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5a00-132">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5a00-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5a00-134">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a5a00-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a5a00-135">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a5a00-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)