---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 44fe7da11f3a06d7938f084b0edf6a6a39bb30f5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412761"
---
# <span data-ttu-id="4f930-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4f930-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="4f930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f930-102">SYNOPSIS</span></span>
<span data-ttu-id="4f930-103">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4f930-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4f930-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f930-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f930-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f930-105">DESCRIPTION</span></span>
<span data-ttu-id="4f930-106">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4f930-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4f930-107">예제</span><span class="sxs-lookup"><span data-stu-id="4f930-107">EXAMPLES</span></span>

### <span data-ttu-id="4f930-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f930-108">Example 1</span></span>
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

<span data-ttu-id="4f930-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4f930-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="4f930-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f930-110">PARAMETERS</span></span>

### <span data-ttu-id="4f930-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f930-111">-DefaultProfile</span></span>
<span data-ttu-id="4f930-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f930-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f930-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4f930-113">-RuleGroupOverride</span></span>
<span data-ttu-id="4f930-114">Azure 관리되는 공급자 오버라이드 구성 목록</span><span class="sxs-lookup"><span data-stu-id="4f930-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="4f930-115">-Type</span><span class="sxs-lookup"><span data-stu-id="4f930-115">-Type</span></span>
<span data-ttu-id="4f930-116">규칙시트의 유형</span><span class="sxs-lookup"><span data-stu-id="4f930-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="4f930-117">-Version</span><span class="sxs-lookup"><span data-stu-id="4f930-117">-Version</span></span>
<span data-ttu-id="4f930-118">규칙시트의 버전</span><span class="sxs-lookup"><span data-stu-id="4f930-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="4f930-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f930-119">CommonParameters</span></span>
<span data-ttu-id="4f930-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f930-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f930-121">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f930-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f930-122">입력</span><span class="sxs-lookup"><span data-stu-id="4f930-122">INPUTS</span></span>

### <span data-ttu-id="4f930-123">없음</span><span class="sxs-lookup"><span data-stu-id="4f930-123">None</span></span>

## <span data-ttu-id="4f930-124">출력</span><span class="sxs-lookup"><span data-stu-id="4f930-124">OUTPUTS</span></span>

### <span data-ttu-id="4f930-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="4f930-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="4f930-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f930-126">NOTES</span></span>

## <span data-ttu-id="4f930-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f930-127">RELATED LINKS</span></span>

<span data-ttu-id="4f930-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="4f930-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
