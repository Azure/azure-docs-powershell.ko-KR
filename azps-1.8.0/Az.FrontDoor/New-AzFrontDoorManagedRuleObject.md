---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: c72573f467377a4ea16fd487a8cee5f0055a5cee
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401456"
---
# <span data-ttu-id="fb08f-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="fb08f-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="fb08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb08f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb08f-103">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fb08f-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="fb08f-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb08f-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb08f-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb08f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb08f-106">WAF 정책 만들기를 위한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fb08f-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="fb08f-107">예제</span><span class="sxs-lookup"><span data-stu-id="fb08f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb08f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb08f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="fb08f-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="fb08f-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="fb08f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb08f-110">PARAMETERS</span></span>

### <span data-ttu-id="fb08f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb08f-111">-DefaultProfile</span></span>
<span data-ttu-id="fb08f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb08f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb08f-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="fb08f-113">-RuleGroupOverride</span></span>
<span data-ttu-id="fb08f-114">Azure 관리되는 공급자 오버라이드 구성 목록</span><span class="sxs-lookup"><span data-stu-id="fb08f-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="fb08f-115">-Type</span><span class="sxs-lookup"><span data-stu-id="fb08f-115">-Type</span></span>
<span data-ttu-id="fb08f-116">규칙시트의 유형</span><span class="sxs-lookup"><span data-stu-id="fb08f-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="fb08f-117">-Version</span><span class="sxs-lookup"><span data-stu-id="fb08f-117">-Version</span></span>
<span data-ttu-id="fb08f-118">규칙시트의 버전</span><span class="sxs-lookup"><span data-stu-id="fb08f-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="fb08f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb08f-119">CommonParameters</span></span>
<span data-ttu-id="fb08f-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb08f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb08f-121">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb08f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb08f-122">입력</span><span class="sxs-lookup"><span data-stu-id="fb08f-122">INPUTS</span></span>

### <span data-ttu-id="fb08f-123">없음</span><span class="sxs-lookup"><span data-stu-id="fb08f-123">None</span></span>

## <span data-ttu-id="fb08f-124">출력</span><span class="sxs-lookup"><span data-stu-id="fb08f-124">OUTPUTS</span></span>

### <span data-ttu-id="fb08f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="fb08f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="fb08f-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb08f-126">NOTES</span></span>

## <span data-ttu-id="fb08f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb08f-127">RELATED LINKS</span></span>

<span data-ttu-id="fb08f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="fb08f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
