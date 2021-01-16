---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 266d553f70cb5c128df1d266f95ee93cb1eb013c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337070"
---
# <span data-ttu-id="3106a-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3106a-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="3106a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3106a-102">SYNOPSIS</span></span>
<span data-ttu-id="3106a-103">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3106a-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3106a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3106a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3106a-105">설명</span><span class="sxs-lookup"><span data-stu-id="3106a-105">DESCRIPTION</span></span>
<span data-ttu-id="3106a-106">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3106a-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3106a-107">예제</span><span class="sxs-lookup"><span data-stu-id="3106a-107">EXAMPLES</span></span>

### <span data-ttu-id="3106a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3106a-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="3106a-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3106a-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="3106a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3106a-110">PARAMETERS</span></span>

### <span data-ttu-id="3106a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3106a-111">-DefaultProfile</span></span>
<span data-ttu-id="3106a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3106a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3106a-113">-제외</span><span class="sxs-lookup"><span data-stu-id="3106a-113">-Exclusion</span></span>
<span data-ttu-id="3106a-114">제외</span><span class="sxs-lookup"><span data-stu-id="3106a-114">Exclusion</span></span>

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

### <span data-ttu-id="3106a-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3106a-115">-RuleGroupOverride</span></span>
<span data-ttu-id="3106a-116">Azure 관리 공급자 오버라이드 구성 목록</span><span class="sxs-lookup"><span data-stu-id="3106a-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="3106a-117">-Type</span><span class="sxs-lookup"><span data-stu-id="3106a-117">-Type</span></span>
<span data-ttu-id="3106a-118">규칙시트의 유형</span><span class="sxs-lookup"><span data-stu-id="3106a-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="3106a-119">-Version</span><span class="sxs-lookup"><span data-stu-id="3106a-119">-Version</span></span>
<span data-ttu-id="3106a-120">규칙시트의 버전</span><span class="sxs-lookup"><span data-stu-id="3106a-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="3106a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3106a-121">CommonParameters</span></span>
<span data-ttu-id="3106a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3106a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3106a-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3106a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3106a-124">입력</span><span class="sxs-lookup"><span data-stu-id="3106a-124">INPUTS</span></span>

### <span data-ttu-id="3106a-125">없음</span><span class="sxs-lookup"><span data-stu-id="3106a-125">None</span></span>

## <span data-ttu-id="3106a-126">출력</span><span class="sxs-lookup"><span data-stu-id="3106a-126">OUTPUTS</span></span>

### <span data-ttu-id="3106a-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="3106a-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="3106a-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3106a-128">NOTES</span></span>

## <span data-ttu-id="3106a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3106a-129">RELATED LINKS</span></span>

<span data-ttu-id="3106a-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="3106a-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
