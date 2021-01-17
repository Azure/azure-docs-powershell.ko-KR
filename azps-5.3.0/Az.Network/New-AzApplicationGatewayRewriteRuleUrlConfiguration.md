---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379317"
---
# <span data-ttu-id="24a0c-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="24a0c-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="24a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="24a0c-103">애플리케이션 게이트웨이에 대한 다시 작성 규칙 URL 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="24a0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="24a0c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a0c-105">설명</span><span class="sxs-lookup"><span data-stu-id="24a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="24a0c-106">**AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 URL 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="24a0c-107">예제</span><span class="sxs-lookup"><span data-stu-id="24a0c-107">EXAMPLES</span></span>

### <span data-ttu-id="24a0c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="24a0c-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="24a0c-109">이 명령은 다시 작성 규칙 URL 구성을 만들고 결과를 $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="24a0c-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="24a0c-110">기존 UrlConfiguration을 업데이트하려는 경우 새 UrlConfiguration을 만들고 규칙 작업 집합 다시 작성의 UrlConfiguration 속성에 새 UrlConfiguration을 할당하여 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="24a0c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24a0c-111">PARAMETERS</span></span>

### <span data-ttu-id="24a0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a0c-112">-DefaultProfile</span></span>
<span data-ttu-id="24a0c-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a0c-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="24a0c-114">-ModifiedPath</span></span>
<span data-ttu-id="24a0c-115">URL 경로 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-115">Url path value.</span></span>

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

### <span data-ttu-id="24a0c-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="24a0c-116">-ModifiedQueryString</span></span>
<span data-ttu-id="24a0c-117">URL 쿼리 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-117">Url query string value.</span></span>

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

### <span data-ttu-id="24a0c-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="24a0c-118">-Reroute</span></span>
<span data-ttu-id="24a0c-119">수정된 경로를 사용하여 경로 기반 요청 라우팅 규칙에 제공된 URL 경로 맵을 다시 평가하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="24a0c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a0c-120">CommonParameters</span></span>
<span data-ttu-id="24a0c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24a0c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a0c-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24a0c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a0c-123">입력</span><span class="sxs-lookup"><span data-stu-id="24a0c-123">INPUTS</span></span>

### <span data-ttu-id="24a0c-124">없음</span><span class="sxs-lookup"><span data-stu-id="24a0c-124">None</span></span>

## <span data-ttu-id="24a0c-125">출력</span><span class="sxs-lookup"><span data-stu-id="24a0c-125">OUTPUTS</span></span>

### <span data-ttu-id="24a0c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="24a0c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="24a0c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24a0c-127">NOTES</span></span>

## <span data-ttu-id="24a0c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24a0c-128">RELATED LINKS</span></span>

[<span data-ttu-id="24a0c-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24a0c-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24a0c-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24a0c-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24a0c-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24a0c-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="24a0c-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="24a0c-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="24a0c-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)