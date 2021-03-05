---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015280"
---
# <span data-ttu-id="c6c72-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="c6c72-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="c6c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c72-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c72-103">WAF 정책 만들기에 대한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="c6c72-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c6c72-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6c72-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c72-105">설명</span><span class="sxs-lookup"><span data-stu-id="c6c72-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c72-106">WAF 정책 만들기에 대한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="c6c72-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c6c72-107">예제</span><span class="sxs-lookup"><span data-stu-id="c6c72-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c72-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6c72-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="c6c72-109">RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="c6c72-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="c6c72-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6c72-110">PARAMETERS</span></span>

### <span data-ttu-id="c6c72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c72-111">-DefaultProfile</span></span>
<span data-ttu-id="c6c72-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c72-113">-제외</span><span class="sxs-lookup"><span data-stu-id="c6c72-113">-Exclusion</span></span>
<span data-ttu-id="c6c72-114">제외</span><span class="sxs-lookup"><span data-stu-id="c6c72-114">Exclusion</span></span>

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

### <span data-ttu-id="c6c72-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c6c72-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="c6c72-116">규칙재정 목록</span><span class="sxs-lookup"><span data-stu-id="c6c72-116">Rule override list</span></span>

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

### <span data-ttu-id="c6c72-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c72-117">-RuleGroupName</span></span>
<span data-ttu-id="c6c72-118">이러한 오버라이드가 적용되는 규칙 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c6c72-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="c6c72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c72-119">CommonParameters</span></span>
<span data-ttu-id="c6c72-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c72-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6c72-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c72-122">입력</span><span class="sxs-lookup"><span data-stu-id="c6c72-122">INPUTS</span></span>

### <span data-ttu-id="c6c72-123">없음</span><span class="sxs-lookup"><span data-stu-id="c6c72-123">None</span></span>

## <span data-ttu-id="c6c72-124">출력</span><span class="sxs-lookup"><span data-stu-id="c6c72-124">OUTPUTS</span></span>

### <span data-ttu-id="c6c72-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c6c72-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="c6c72-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6c72-126">NOTES</span></span>

## <span data-ttu-id="c6c72-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6c72-127">RELATED LINKS</span></span>

[<span data-ttu-id="c6c72-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6c72-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
