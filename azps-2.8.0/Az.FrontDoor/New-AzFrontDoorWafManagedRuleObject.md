---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689873"
---
# <span data-ttu-id="26772-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="26772-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="26772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26772-102">SYNOPSIS</span></span>
<span data-ttu-id="26772-103">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="26772-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="26772-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26772-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26772-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26772-105">DESCRIPTION</span></span>
<span data-ttu-id="26772-106">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="26772-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="26772-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26772-107">EXAMPLES</span></span>

### <span data-ttu-id="26772-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="26772-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="26772-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="26772-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="26772-110">변수</span><span class="sxs-lookup"><span data-stu-id="26772-110">PARAMETERS</span></span>

### <span data-ttu-id="26772-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26772-111">-DefaultProfile</span></span>
<span data-ttu-id="26772-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26772-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26772-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="26772-113">-RuleGroupOverride</span></span>
<span data-ttu-id="26772-114">Azure 관리 공급자 재정의 구성 목록</span><span class="sxs-lookup"><span data-stu-id="26772-114">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26772-115">-Type</span><span class="sxs-lookup"><span data-stu-id="26772-115">-Type</span></span>
<span data-ttu-id="26772-116">규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="26772-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="26772-117">-버전</span><span class="sxs-lookup"><span data-stu-id="26772-117">-Version</span></span>
<span data-ttu-id="26772-118">버전 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="26772-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="26772-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26772-119">CommonParameters</span></span>
<span data-ttu-id="26772-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26772-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26772-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26772-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26772-122">입력</span><span class="sxs-lookup"><span data-stu-id="26772-122">INPUTS</span></span>

### <span data-ttu-id="26772-123">않아야</span><span class="sxs-lookup"><span data-stu-id="26772-123">None</span></span>

## <span data-ttu-id="26772-124">출력</span><span class="sxs-lookup"><span data-stu-id="26772-124">OUTPUTS</span></span>

### <span data-ttu-id="26772-125">FrontDoor를 통해 PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="26772-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="26772-126">상속자</span><span class="sxs-lookup"><span data-stu-id="26772-126">NOTES</span></span>

## <span data-ttu-id="26772-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26772-127">RELATED LINKS</span></span>

<span data-ttu-id="26772-128">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [새로운 AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="26772-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>