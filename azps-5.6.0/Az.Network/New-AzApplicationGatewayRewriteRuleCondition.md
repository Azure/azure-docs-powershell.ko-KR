---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001147"
---
# <span data-ttu-id="d453b-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d453b-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d453b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d453b-102">SYNOPSIS</span></span>
<span data-ttu-id="d453b-103">애플리케이션 게이트웨이에 대한 RewriteRule에 조건을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="d453b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d453b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d453b-105">설명</span><span class="sxs-lookup"><span data-stu-id="d453b-105">DESCRIPTION</span></span>
<span data-ttu-id="d453b-106">**AzApplicationGatewayRewriteRuleCondition** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 다시 작성 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="d453b-107">예제</span><span class="sxs-lookup"><span data-stu-id="d453b-107">EXAMPLES</span></span>

### <span data-ttu-id="d453b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d453b-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="d453b-109">이 명령은 다시 작성 규칙에서 조건을 만들고 결과를 변수에 $condition.</span><span class="sxs-lookup"><span data-stu-id="d453b-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="d453b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d453b-110">PARAMETERS</span></span>

### <span data-ttu-id="d453b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d453b-111">-DefaultProfile</span></span>
<span data-ttu-id="d453b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d453b-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="d453b-113">-IgnoreCase</span></span>
<span data-ttu-id="d453b-114">패턴에서 대소문자 무시를 위해 이 플래그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d453b-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="d453b-115">-Negate</span></span>
<span data-ttu-id="d453b-116">조건 유효성 검사를 부인하기 위해 이 플래그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d453b-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="d453b-117">-Pattern</span></span>
<span data-ttu-id="d453b-118">변수 헤더에서 찾아야 하는 패턴</span><span class="sxs-lookup"><span data-stu-id="d453b-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d453b-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="d453b-119">-Variable</span></span>
<span data-ttu-id="d453b-120">조건을 설정할 헤더의 이름</span><span class="sxs-lookup"><span data-stu-id="d453b-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d453b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d453b-121">CommonParameters</span></span>
<span data-ttu-id="d453b-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d453b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d453b-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d453b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d453b-124">입력</span><span class="sxs-lookup"><span data-stu-id="d453b-124">INPUTS</span></span>

### <span data-ttu-id="d453b-125">없음</span><span class="sxs-lookup"><span data-stu-id="d453b-125">None</span></span>

## <span data-ttu-id="d453b-126">출력</span><span class="sxs-lookup"><span data-stu-id="d453b-126">OUTPUTS</span></span>

### <span data-ttu-id="d453b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d453b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d453b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d453b-128">NOTES</span></span>

## <span data-ttu-id="d453b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d453b-129">RELATED LINKS</span></span>
[<span data-ttu-id="d453b-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d453b-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d453b-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d453b-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d453b-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d453b-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d453b-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d453b-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d453b-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d453b-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d453b-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d453b-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d453b-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d453b-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
