---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492167"
---
# <span data-ttu-id="a516a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="a516a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="a516a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a516a-102">SYNOPSIS</span></span>
<span data-ttu-id="a516a-103">비활성화된 새 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="a516a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a516a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a516a-105">설명</span><span class="sxs-lookup"><span data-stu-id="a516a-105">DESCRIPTION</span></span>
<span data-ttu-id="a516a-106">**New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet은 새로운 비활성화된 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="a516a-107">예제</span><span class="sxs-lookup"><span data-stu-id="a516a-107">EXAMPLES</span></span>

### <span data-ttu-id="a516a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a516a-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="a516a-109">이 명령은 규칙 942130 및 규칙 942140이 비활성화된 "REQUEST-942-APPLICATION-ATTACK-SQLI"라는 규칙 그룹에 대해 사용하지 않도록 설정된 규칙 그룹 구성을 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="a516a-110">사용하지 않도록 설정한 새 규칙 그룹 구성은 $disabledRuleGroup 1에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="a516a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a516a-111">PARAMETERS</span></span>

### <span data-ttu-id="a516a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a516a-112">-DefaultProfile</span></span>
<span data-ttu-id="a516a-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a516a-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="a516a-114">-RuleGroupName</span></span>
<span data-ttu-id="a516a-115">비활성화할 규칙 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="a516a-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="a516a-116">-Rules</span></span>
<span data-ttu-id="a516a-117">비활성화할 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="a516a-118">null이면 규칙 그룹의 모든 규칙이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a516a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a516a-119">CommonParameters</span></span>
<span data-ttu-id="a516a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a516a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a516a-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a516a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a516a-122">입력</span><span class="sxs-lookup"><span data-stu-id="a516a-122">INPUTS</span></span>

### <span data-ttu-id="a516a-123">없음</span><span class="sxs-lookup"><span data-stu-id="a516a-123">None</span></span>

## <span data-ttu-id="a516a-124">출력</span><span class="sxs-lookup"><span data-stu-id="a516a-124">OUTPUTS</span></span>

### <span data-ttu-id="a516a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="a516a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="a516a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a516a-126">NOTES</span></span>

## <span data-ttu-id="a516a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a516a-127">RELATED LINKS</span></span>

[<span data-ttu-id="a516a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a516a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a516a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a516a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

