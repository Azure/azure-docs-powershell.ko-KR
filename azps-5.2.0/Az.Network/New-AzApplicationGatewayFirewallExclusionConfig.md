---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340286"
---
# <span data-ttu-id="ac37a-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="ac37a-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="ac37a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac37a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac37a-103">애플리케이션 게이트웨이 waf에 대한 새 제외 규칙 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="ac37a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac37a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac37a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ac37a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac37a-106">**New-AzApplicationGatewayFirewallExclusionConfig** cmdlet은 애플리케이션 게이트웨이 waf에 대한 새 제외 규칙 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="ac37a-107">예제</span><span class="sxs-lookup"><span data-stu-id="ac37a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac37a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac37a-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="ac37a-109">이 명령은 RequestHeaderNames라는 변수와 xyz라는 StartsWith 및 Selector라는 연산자에 대한 새 제외 규칙 목록 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="ac37a-110">제외 목록 구성은 $exclusion 1에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="ac37a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac37a-111">PARAMETERS</span></span>

### <span data-ttu-id="ac37a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac37a-112">-DefaultProfile</span></span>
<span data-ttu-id="ac37a-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac37a-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="ac37a-114">-Operator</span></span>
<span data-ttu-id="ac37a-115">변수가 컬렉션인 경우 선택기에서 작동하여 이 제외가 적용되는 컬렉션의 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="ac37a-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="ac37a-116">-Selector</span></span>
<span data-ttu-id="ac37a-117">변수가 컬렉션인 경우 연산자는 이 제외가 적용되는 컬렉션의 요소를 지정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="ac37a-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="ac37a-118">-Variable</span></span>
<span data-ttu-id="ac37a-119">제외할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="ac37a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac37a-120">CommonParameters</span></span>
<span data-ttu-id="ac37a-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac37a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac37a-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ac37a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac37a-123">입력</span><span class="sxs-lookup"><span data-stu-id="ac37a-123">INPUTS</span></span>

### <span data-ttu-id="ac37a-124">없음</span><span class="sxs-lookup"><span data-stu-id="ac37a-124">None</span></span>

## <span data-ttu-id="ac37a-125">출력</span><span class="sxs-lookup"><span data-stu-id="ac37a-125">OUTPUTS</span></span>

### <span data-ttu-id="ac37a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="ac37a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="ac37a-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac37a-127">NOTES</span></span>

## <span data-ttu-id="ac37a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac37a-128">RELATED LINKS</span></span>
