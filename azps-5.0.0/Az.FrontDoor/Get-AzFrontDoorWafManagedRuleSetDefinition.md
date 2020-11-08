---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219056"
---
# <span data-ttu-id="e0bd6-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e0bd6-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e0bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bd6-103">WAF 관리 규칙 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="e0bd6-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="e0bd6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0bd6-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0bd6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bd6-106">참조로 사용할 WAF 관리 규칙 집합 정의의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0bd6-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="e0bd6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e0bd6-107">EXAMPLES</span></span>

### <span data-ttu-id="e0bd6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0bd6-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="e0bd6-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="e0bd6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e0bd6-110">변수</span><span class="sxs-lookup"><span data-stu-id="e0bd6-110">PARAMETERS</span></span>

### <span data-ttu-id="e0bd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bd6-111">-DefaultProfile</span></span>
<span data-ttu-id="e0bd6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0bd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0bd6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bd6-113">CommonParameters</span></span>
<span data-ttu-id="e0bd6-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0bd6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bd6-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e0bd6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bd6-116">입력</span><span class="sxs-lookup"><span data-stu-id="e0bd6-116">INPUTS</span></span>

### <span data-ttu-id="e0bd6-117">않아야</span><span class="sxs-lookup"><span data-stu-id="e0bd6-117">None</span></span>

## <span data-ttu-id="e0bd6-118">출력</span><span class="sxs-lookup"><span data-stu-id="e0bd6-118">OUTPUTS</span></span>

### <span data-ttu-id="e0bd6-119">FrontDoor를 통해 PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e0bd6-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e0bd6-120">상속자</span><span class="sxs-lookup"><span data-stu-id="e0bd6-120">NOTES</span></span>

## <span data-ttu-id="e0bd6-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0bd6-121">RELATED LINKS</span></span>

<span data-ttu-id="e0bd6-122">[새로운 AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [새로운 AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [새로운 AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="e0bd6-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
