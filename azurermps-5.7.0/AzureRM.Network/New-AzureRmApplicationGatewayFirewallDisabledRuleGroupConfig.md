---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 780e231f2ca512b5becf0ee068c004dd815cea89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530438"
---
# <span data-ttu-id="e5ea8-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="e5ea8-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="e5ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ea8-103">사용할 수 없도록 설정 된 새 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5ea8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5ea8-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5ea8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ea8-106">**AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet은 사용 하지 않도록 설정 된 새 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="e5ea8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5ea8-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ea8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5ea8-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="e5ea8-109">명령이 규칙 942130 및 규칙 942140을 사용 하지 않도록 설정 된 규칙 그룹에 대 한 새 규칙 그룹 구성 ("REQUEST-942-SQLI")을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="e5ea8-110">사용 하지 않도록 설정 된 새 규칙 그룹 구성은 $disabledRuleGroup 1에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="e5ea8-111">변수</span><span class="sxs-lookup"><span data-stu-id="e5ea8-111">PARAMETERS</span></span>

### <span data-ttu-id="e5ea8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ea8-112">-DefaultProfile</span></span>
<span data-ttu-id="e5ea8-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ea8-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ea8-114">-RuleGroupName</span></span>
<span data-ttu-id="e5ea8-115">사용할 수 없게 되는 규칙 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="e5ea8-116">-규칙</span><span class="sxs-lookup"><span data-stu-id="e5ea8-116">-Rules</span></span>
<span data-ttu-id="e5ea8-117">사용할 수 없게 되는 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="e5ea8-118">Null 인 경우 규칙 그룹의 모든 규칙이 사용 되지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="e5ea8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ea8-119">CommonParameters</span></span>
<span data-ttu-id="e5ea8-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ea8-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ea8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ea8-122">입력</span><span class="sxs-lookup"><span data-stu-id="e5ea8-122">INPUTS</span></span>

### <span data-ttu-id="e5ea8-123">않아야</span><span class="sxs-lookup"><span data-stu-id="e5ea8-123">None</span></span>

## <span data-ttu-id="e5ea8-124">출력</span><span class="sxs-lookup"><span data-stu-id="e5ea8-124">OUTPUTS</span></span>

### <span data-ttu-id="e5ea8-125">PSApplicationGatewayFirewallDisabledRuleGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="e5ea8-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e5ea8-126">NOTES</span></span>

## <span data-ttu-id="e5ea8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5ea8-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5ea8-128">새로운 AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5ea8-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e5ea8-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5ea8-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

