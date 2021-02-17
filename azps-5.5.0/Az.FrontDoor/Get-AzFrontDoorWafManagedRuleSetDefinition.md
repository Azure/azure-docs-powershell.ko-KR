---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209512"
---
# <span data-ttu-id="e0984-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e0984-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e0984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0984-102">SYNOPSIS</span></span>
<span data-ttu-id="e0984-103">WAF 관리 규칙 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0984-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="e0984-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0984-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0984-105">설명</span><span class="sxs-lookup"><span data-stu-id="e0984-105">DESCRIPTION</span></span>
<span data-ttu-id="e0984-106">참조로 사용할 WAF 관리 규칙 집합 정의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0984-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="e0984-107">예제</span><span class="sxs-lookup"><span data-stu-id="e0984-107">EXAMPLES</span></span>

### <span data-ttu-id="e0984-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0984-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="e0984-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="e0984-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e0984-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0984-110">PARAMETERS</span></span>

### <span data-ttu-id="e0984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0984-111">-DefaultProfile</span></span>
<span data-ttu-id="e0984-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0984-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0984-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0984-113">CommonParameters</span></span>
<span data-ttu-id="e0984-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0984-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0984-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0984-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0984-116">입력</span><span class="sxs-lookup"><span data-stu-id="e0984-116">INPUTS</span></span>

### <span data-ttu-id="e0984-117">없음</span><span class="sxs-lookup"><span data-stu-id="e0984-117">None</span></span>

## <span data-ttu-id="e0984-118">출력</span><span class="sxs-lookup"><span data-stu-id="e0984-118">OUTPUTS</span></span>

### <span data-ttu-id="e0984-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e0984-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e0984-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0984-120">NOTES</span></span>

## <span data-ttu-id="e0984-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0984-121">RELATED LINKS</span></span>

<span data-ttu-id="e0984-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="e0984-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
