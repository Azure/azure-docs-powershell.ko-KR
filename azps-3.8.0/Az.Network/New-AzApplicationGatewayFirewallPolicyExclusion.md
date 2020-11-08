---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044817"
---
# <span data-ttu-id="e8ec4-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e8ec4-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="e8ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ec4-103">방화벽 정책에서 제외를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="e8ec4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8ec4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ec4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ec4-106">**AzApplicationGatewayFirewallPolicyExclusion** cmdlet은 방화벽 정책의 새 제외 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="e8ec4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e8ec4-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ec4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8ec4-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="e8ec4-109">이 명령은 xyz 라는 RequestHeaderNames 및 선택기 라는 StartsWith 라는 변수에 대해 새 제외 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="e8ec4-110">제외 항목이 $exclusionEntry에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="e8ec4-111">변수</span><span class="sxs-lookup"><span data-stu-id="e8ec4-111">PARAMETERS</span></span>

### <span data-ttu-id="e8ec4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec4-112">-DefaultProfile</span></span>
<span data-ttu-id="e8ec4-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ec4-114">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e8ec4-114">-MatchVariable</span></span>
<span data-ttu-id="e8ec4-115">제외할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="e8ec4-116">-선택기</span><span class="sxs-lookup"><span data-stu-id="e8ec4-116">-Selector</span></span>
<span data-ttu-id="e8ec4-117">Variable 변수는 collection이 고이 제외를 적용할 컬렉션의 요소를 지정 하는 데 사용 되는 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e8ec4-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="e8ec4-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="e8ec4-119">변수가 컬렉션인 경우 선택기에 대해 작업을 수행 하 여이 제외를 적용할 컬렉션의 요소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e8ec4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ec4-120">CommonParameters</span></span>
<span data-ttu-id="e8ec4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ec4-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ec4-123">입력</span><span class="sxs-lookup"><span data-stu-id="e8ec4-123">INPUTS</span></span>

### <span data-ttu-id="e8ec4-124">않아야</span><span class="sxs-lookup"><span data-stu-id="e8ec4-124">None</span></span>

## <span data-ttu-id="e8ec4-125">출력</span><span class="sxs-lookup"><span data-stu-id="e8ec4-125">OUTPUTS</span></span>

### <span data-ttu-id="e8ec4-126">PSApplicationGatewayFirewallPolicyExclusion에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e8ec4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="e8ec4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e8ec4-127">NOTES</span></span>

## <span data-ttu-id="e8ec4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ec4-128">RELATED LINKS</span></span>
