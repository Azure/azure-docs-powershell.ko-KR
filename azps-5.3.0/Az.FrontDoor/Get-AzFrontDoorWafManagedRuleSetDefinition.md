---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489747"
---
# <span data-ttu-id="8bf80-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="8bf80-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="8bf80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bf80-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf80-103">WAF 관리 규칙 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf80-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="8bf80-104">구문</span><span class="sxs-lookup"><span data-stu-id="8bf80-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bf80-105">설명</span><span class="sxs-lookup"><span data-stu-id="8bf80-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf80-106">참조로 사용할 WAF 관리 규칙 집합 정의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf80-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="8bf80-107">예제</span><span class="sxs-lookup"><span data-stu-id="8bf80-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf80-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8bf80-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="8bf80-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="8bf80-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8bf80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bf80-110">PARAMETERS</span></span>

### <span data-ttu-id="8bf80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf80-111">-DefaultProfile</span></span>
<span data-ttu-id="8bf80-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf80-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf80-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf80-113">CommonParameters</span></span>
<span data-ttu-id="8bf80-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf80-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf80-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8bf80-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf80-116">입력</span><span class="sxs-lookup"><span data-stu-id="8bf80-116">INPUTS</span></span>

### <span data-ttu-id="8bf80-117">없음</span><span class="sxs-lookup"><span data-stu-id="8bf80-117">None</span></span>

## <span data-ttu-id="8bf80-118">출력</span><span class="sxs-lookup"><span data-stu-id="8bf80-118">OUTPUTS</span></span>

### <span data-ttu-id="8bf80-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="8bf80-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="8bf80-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8bf80-120">NOTES</span></span>

## <span data-ttu-id="8bf80-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bf80-121">RELATED LINKS</span></span>

<span data-ttu-id="8bf80-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="8bf80-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
