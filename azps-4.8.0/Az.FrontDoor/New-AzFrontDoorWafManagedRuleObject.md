---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213572"
---
# <span data-ttu-id="ab726-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab726-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="ab726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab726-102">SYNOPSIS</span></span>
<span data-ttu-id="ab726-103">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ab726-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ab726-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab726-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab726-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab726-105">DESCRIPTION</span></span>
<span data-ttu-id="ab726-106">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ab726-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ab726-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab726-107">EXAMPLES</span></span>

### <span data-ttu-id="ab726-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab726-108">Example 1</span></span>
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

<span data-ttu-id="ab726-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ab726-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="ab726-110">변수</span><span class="sxs-lookup"><span data-stu-id="ab726-110">PARAMETERS</span></span>

### <span data-ttu-id="ab726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab726-111">-DefaultProfile</span></span>
<span data-ttu-id="ab726-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab726-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab726-113">-제외</span><span class="sxs-lookup"><span data-stu-id="ab726-113">-Exclusion</span></span>
<span data-ttu-id="ab726-114">전용</span><span class="sxs-lookup"><span data-stu-id="ab726-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab726-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ab726-115">-RuleGroupOverride</span></span>
<span data-ttu-id="ab726-116">Azure 관리 공급자 재정의 구성 목록</span><span class="sxs-lookup"><span data-stu-id="ab726-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="ab726-117">-Type</span><span class="sxs-lookup"><span data-stu-id="ab726-117">-Type</span></span>
<span data-ttu-id="ab726-118">규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ab726-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="ab726-119">-버전</span><span class="sxs-lookup"><span data-stu-id="ab726-119">-Version</span></span>
<span data-ttu-id="ab726-120">버전 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="ab726-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="ab726-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab726-121">CommonParameters</span></span>
<span data-ttu-id="ab726-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab726-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab726-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab726-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab726-124">입력</span><span class="sxs-lookup"><span data-stu-id="ab726-124">INPUTS</span></span>

### <span data-ttu-id="ab726-125">않아야</span><span class="sxs-lookup"><span data-stu-id="ab726-125">None</span></span>

## <span data-ttu-id="ab726-126">출력</span><span class="sxs-lookup"><span data-stu-id="ab726-126">OUTPUTS</span></span>

### <span data-ttu-id="ab726-127">FrontDoor를 통해 PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="ab726-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="ab726-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ab726-128">NOTES</span></span>

## <span data-ttu-id="ab726-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab726-129">RELATED LINKS</span></span>

<span data-ttu-id="ab726-130">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [업데이트-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [새로운 AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="ab726-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
