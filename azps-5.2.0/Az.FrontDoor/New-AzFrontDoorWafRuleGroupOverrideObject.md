---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332246"
---
# <span data-ttu-id="61fc2-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="61fc2-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="61fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="61fc2-103">WAF 정책 만들기에 대한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="61fc2-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="61fc2-104">구문</span><span class="sxs-lookup"><span data-stu-id="61fc2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61fc2-105">설명</span><span class="sxs-lookup"><span data-stu-id="61fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="61fc2-106">WAF 정책 만들기에 대한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="61fc2-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="61fc2-107">예제</span><span class="sxs-lookup"><span data-stu-id="61fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="61fc2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="61fc2-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="61fc2-109">RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="61fc2-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="61fc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="61fc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fc2-111">-DefaultProfile</span></span>
<span data-ttu-id="61fc2-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61fc2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61fc2-113">-제외</span><span class="sxs-lookup"><span data-stu-id="61fc2-113">-Exclusion</span></span>
<span data-ttu-id="61fc2-114">제외</span><span class="sxs-lookup"><span data-stu-id="61fc2-114">Exclusion</span></span>

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

### <span data-ttu-id="61fc2-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="61fc2-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="61fc2-116">규칙재지 목록</span><span class="sxs-lookup"><span data-stu-id="61fc2-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61fc2-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="61fc2-117">-RuleGroupName</span></span>
<span data-ttu-id="61fc2-118">이러한 overrides가 적용되는 규칙 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="61fc2-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="61fc2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fc2-119">CommonParameters</span></span>
<span data-ttu-id="61fc2-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61fc2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fc2-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61fc2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fc2-122">입력</span><span class="sxs-lookup"><span data-stu-id="61fc2-122">INPUTS</span></span>

### <span data-ttu-id="61fc2-123">없음</span><span class="sxs-lookup"><span data-stu-id="61fc2-123">None</span></span>

## <span data-ttu-id="61fc2-124">출력</span><span class="sxs-lookup"><span data-stu-id="61fc2-124">OUTPUTS</span></span>

### <span data-ttu-id="61fc2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="61fc2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="61fc2-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61fc2-126">NOTES</span></span>

## <span data-ttu-id="61fc2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61fc2-127">RELATED LINKS</span></span>

[<span data-ttu-id="61fc2-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="61fc2-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
