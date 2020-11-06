---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 6ea379b1ad1629dc0ba3e7d747256c86153c651d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537068"
---
# <span data-ttu-id="9c732-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="9c732-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="9c732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c732-102">SYNOPSIS</span></span>
<span data-ttu-id="9c732-103">사용할 수 없도록 설정 된 새 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c732-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c732-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c732-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c732-105">DESCRIPTION</span></span>
<span data-ttu-id="9c732-106">**AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet은 사용 하지 않도록 설정 된 새 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="9c732-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c732-107">EXAMPLES</span></span>

### <span data-ttu-id="9c732-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c732-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="9c732-109">명령이 규칙 942130 및 규칙 942140을 사용 하지 않도록 설정 된 규칙 그룹에 대 한 새 규칙 그룹 구성 ("REQUEST-942-SQLI")을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="9c732-110">사용 하지 않도록 설정 된 새 규칙 그룹 구성은 $disabledRuleGroup 1에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="9c732-111">변수</span><span class="sxs-lookup"><span data-stu-id="9c732-111">PARAMETERS</span></span>

### <span data-ttu-id="9c732-112">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="9c732-112">-RuleGroupName</span></span>
<span data-ttu-id="9c732-113">사용할 수 없게 되는 규칙 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-113">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="9c732-114">-규칙</span><span class="sxs-lookup"><span data-stu-id="9c732-114">-Rules</span></span>
<span data-ttu-id="9c732-115">사용할 수 없게 되는 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-115">The list of rules that will be disabled.</span></span>
<span data-ttu-id="9c732-116">Null 인 경우 규칙 그룹의 모든 규칙이 사용 되지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-116">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c732-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c732-117">-DefaultProfile</span></span>
<span data-ttu-id="9c732-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c732-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c732-119">CommonParameters</span></span>
<span data-ttu-id="9c732-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c732-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c732-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c732-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c732-122">입력</span><span class="sxs-lookup"><span data-stu-id="9c732-122">INPUTS</span></span>

### <span data-ttu-id="9c732-123">않아야</span><span class="sxs-lookup"><span data-stu-id="9c732-123">None</span></span>

## <span data-ttu-id="9c732-124">출력</span><span class="sxs-lookup"><span data-stu-id="9c732-124">OUTPUTS</span></span>

### <span data-ttu-id="9c732-125">PSApplicationGatewayFirewallDisabledRuleGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9c732-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="9c732-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9c732-126">NOTES</span></span>

## <span data-ttu-id="9c732-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c732-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c732-128">새로운 AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c732-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="9c732-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c732-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

