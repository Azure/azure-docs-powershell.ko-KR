---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: f3cd7edf0def90f4245e20c540332d08e045865f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955808"
---
# <span data-ttu-id="93b78-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="93b78-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="93b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93b78-102">SYNOPSIS</span></span>
<span data-ttu-id="93b78-103">애플리케이션 게이트웨이 방화벽 정책에 대한 새 사용자 지정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="93b78-104">구문</span><span class="sxs-lookup"><span data-stu-id="93b78-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b78-105">설명</span><span class="sxs-lookup"><span data-stu-id="93b78-105">DESCRIPTION</span></span>
<span data-ttu-id="93b78-106">**New-AzApplicationGatewayFirewallCustomRule은** 방화벽 정책에 대한 사용자 지정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="93b78-107">예제</span><span class="sxs-lookup"><span data-stu-id="93b78-107">EXAMPLES</span></span>

### <span data-ttu-id="93b78-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="93b78-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="93b78-109">명령은 예제 규칙, 우선 순위 1의 이름을 사용하여 새 사용자 지정 규칙을 만들고 규칙 형식은 조건 변수에 정의된 조건을 사용하여 MatchRule이 되고 작업이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="93b78-110">새 일치 사용자 지정 규칙은 $customRule.</span><span class="sxs-lookup"><span data-stu-id="93b78-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="93b78-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93b78-111">PARAMETERS</span></span>

### <span data-ttu-id="93b78-112">-Action</span><span class="sxs-lookup"><span data-stu-id="93b78-112">-Action</span></span>
<span data-ttu-id="93b78-113">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b78-114">-DefaultProfile</span></span>
<span data-ttu-id="93b78-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93b78-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="93b78-116">-MatchCondition</span></span>
<span data-ttu-id="93b78-117">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b78-118">-Name</span><span class="sxs-lookup"><span data-stu-id="93b78-118">-Name</span></span>
<span data-ttu-id="93b78-119">규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="93b78-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="93b78-120">-Priority</span></span>
<span data-ttu-id="93b78-121">규칙의 우선 순위를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-121">Describes priority of the rule.</span></span>
<span data-ttu-id="93b78-122">값이 더 낮은 규칙은 더 높은 값을 가지는 규칙 앞에 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b78-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="93b78-123">-RuleType</span></span>
<span data-ttu-id="93b78-124">규칙 유형을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b78-125">CommonParameters</span></span>
<span data-ttu-id="93b78-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93b78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b78-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93b78-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b78-128">입력</span><span class="sxs-lookup"><span data-stu-id="93b78-128">INPUTS</span></span>

### <span data-ttu-id="93b78-129">없음</span><span class="sxs-lookup"><span data-stu-id="93b78-129">None</span></span>

## <span data-ttu-id="93b78-130">출력</span><span class="sxs-lookup"><span data-stu-id="93b78-130">OUTPUTS</span></span>

### <span data-ttu-id="93b78-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="93b78-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="93b78-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93b78-132">NOTES</span></span>

## <span data-ttu-id="93b78-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93b78-133">RELATED LINKS</span></span>
