---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: d8e22f5eb0e504757bd94fa5235d07ad3e3db998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044830"
---
# <span data-ttu-id="1ae6e-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="1ae6e-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="1ae6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae6e-103">응용 프로그램 게이트웨이 방화벽 정책에 대 한 새 사용자 지정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="1ae6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ae6e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae6e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ae6e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae6e-106">**AzApplicationGatewayFirewallCustomRule** 는 방화벽 정책에 대 한 사용자 지정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="1ae6e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ae6e-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae6e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ae6e-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="1ae6e-109">이 명령은 사용자 지정 규칙 (예: 우선 순위 1)과 규칙 유형이 조건 변수에 정의 된 조건에 일치 하는 규칙을 만들고,이 작업에서 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="1ae6e-110">새 일치 사용자 지정 규칙이 $customRule에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="1ae6e-111">변수</span><span class="sxs-lookup"><span data-stu-id="1ae6e-111">PARAMETERS</span></span>

### <span data-ttu-id="1ae6e-112">-작업</span><span class="sxs-lookup"><span data-stu-id="1ae6e-112">-Action</span></span>
<span data-ttu-id="1ae6e-113">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-113">Type of Actions.</span></span>

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

### <span data-ttu-id="1ae6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae6e-114">-DefaultProfile</span></span>
<span data-ttu-id="1ae6e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae6e-116">MatchCondition</span><span class="sxs-lookup"><span data-stu-id="1ae6e-116">-MatchCondition</span></span>
<span data-ttu-id="1ae6e-117">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-117">List of match conditions.</span></span>

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

### <span data-ttu-id="1ae6e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="1ae6e-118">-Name</span></span>
<span data-ttu-id="1ae6e-119">규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="1ae6e-120">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="1ae6e-120">-Priority</span></span>
<span data-ttu-id="1ae6e-121">규칙의 우선 순위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-121">Describes priority of the rule.</span></span>
<span data-ttu-id="1ae6e-122">값이 낮은 규칙이 높은 값을 갖는 규칙 보다 먼저 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="1ae6e-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="1ae6e-123">-RuleType</span></span>
<span data-ttu-id="1ae6e-124">규칙 유형에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="1ae6e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae6e-125">CommonParameters</span></span>
<span data-ttu-id="1ae6e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae6e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae6e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae6e-128">입력</span><span class="sxs-lookup"><span data-stu-id="1ae6e-128">INPUTS</span></span>

### <span data-ttu-id="1ae6e-129">않아야</span><span class="sxs-lookup"><span data-stu-id="1ae6e-129">None</span></span>

## <span data-ttu-id="1ae6e-130">출력</span><span class="sxs-lookup"><span data-stu-id="1ae6e-130">OUTPUTS</span></span>

### <span data-ttu-id="1ae6e-131">PSApplicationGatewayFirewallCustomRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="1ae6e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1ae6e-132">NOTES</span></span>

## <span data-ttu-id="1ae6e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ae6e-133">RELATED LINKS</span></span>
