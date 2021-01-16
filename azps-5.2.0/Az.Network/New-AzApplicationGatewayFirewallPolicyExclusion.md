---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340245"
---
# <span data-ttu-id="18564-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="18564-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="18564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18564-102">SYNOPSIS</span></span>
<span data-ttu-id="18564-103">방화벽 정책에 대한 제외를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18564-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="18564-104">구문</span><span class="sxs-lookup"><span data-stu-id="18564-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18564-105">설명</span><span class="sxs-lookup"><span data-stu-id="18564-105">DESCRIPTION</span></span>
<span data-ttu-id="18564-106">**New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet은 방화벽 정책에 대한 새 제외 규칙 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="18564-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="18564-107">예제</span><span class="sxs-lookup"><span data-stu-id="18564-107">EXAMPLES</span></span>

### <span data-ttu-id="18564-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="18564-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="18564-109">이 명령은 RequestHeaderNames라는 변수와 xyz라는 StartsWith 및 Selector라는 연산자에 대한 새 제외 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18564-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="18564-110">제외 항목은 $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="18564-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="18564-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18564-111">PARAMETERS</span></span>

### <span data-ttu-id="18564-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18564-112">-DefaultProfile</span></span>
<span data-ttu-id="18564-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18564-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18564-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="18564-114">-MatchVariable</span></span>
<span data-ttu-id="18564-115">제외할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="18564-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18564-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="18564-116">-Selector</span></span>
<span data-ttu-id="18564-117">변수가 컬렉션인 경우 연산자는 이 제외가 적용되는 컬렉션의 요소를 지정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="18564-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="18564-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="18564-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="18564-119">변수가 컬렉션인 경우 선택기에서 작동하여 이 제외가 적용되는 컬렉션의 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18564-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18564-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18564-120">CommonParameters</span></span>
<span data-ttu-id="18564-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18564-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18564-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18564-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18564-123">입력</span><span class="sxs-lookup"><span data-stu-id="18564-123">INPUTS</span></span>

### <span data-ttu-id="18564-124">없음</span><span class="sxs-lookup"><span data-stu-id="18564-124">None</span></span>

## <span data-ttu-id="18564-125">출력</span><span class="sxs-lookup"><span data-stu-id="18564-125">OUTPUTS</span></span>

### <span data-ttu-id="18564-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="18564-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="18564-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18564-127">NOTES</span></span>

## <span data-ttu-id="18564-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18564-128">RELATED LINKS</span></span>
