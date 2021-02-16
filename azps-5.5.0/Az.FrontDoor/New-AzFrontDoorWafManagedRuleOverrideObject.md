---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204064"
---
# <span data-ttu-id="96dc8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="96dc8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="96dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="96dc8-103">관리되는 규칙 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="96dc8-103">Create managed rule override object</span></span>

## <span data-ttu-id="96dc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="96dc8-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96dc8-105">설명</span><span class="sxs-lookup"><span data-stu-id="96dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="96dc8-106">관리되는 WAF 규칙 그룹에 대한 PSAzureManagedRuleOverride 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96dc8-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="96dc8-107">예제</span><span class="sxs-lookup"><span data-stu-id="96dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="96dc8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="96dc8-108">Example 1</span></span>
<span data-ttu-id="96dc8-109">SQLI 그룹에 있는 규칙 942250에 대한 관리되는 규칙의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96dc8-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="96dc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96dc8-110">PARAMETERS</span></span>

### <span data-ttu-id="96dc8-111">-Action</span><span class="sxs-lookup"><span data-stu-id="96dc8-111">-Action</span></span>
<span data-ttu-id="96dc8-112">작업 오버라이드</span><span class="sxs-lookup"><span data-stu-id="96dc8-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dc8-113">-DefaultProfile</span></span>
<span data-ttu-id="96dc8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96dc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96dc8-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="96dc8-115">-Disabled</span></span>
<span data-ttu-id="96dc8-116">사용 안 상태</span><span class="sxs-lookup"><span data-stu-id="96dc8-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dc8-117">-제외</span><span class="sxs-lookup"><span data-stu-id="96dc8-117">-Exclusion</span></span>
<span data-ttu-id="96dc8-118">제외</span><span class="sxs-lookup"><span data-stu-id="96dc8-118">Exclusion</span></span>

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

### <span data-ttu-id="96dc8-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="96dc8-119">-RuleId</span></span>
<span data-ttu-id="96dc8-120">규칙 ID</span><span class="sxs-lookup"><span data-stu-id="96dc8-120">Rule ID</span></span>

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

### <span data-ttu-id="96dc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dc8-121">CommonParameters</span></span>
<span data-ttu-id="96dc8-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96dc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dc8-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96dc8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dc8-124">입력</span><span class="sxs-lookup"><span data-stu-id="96dc8-124">INPUTS</span></span>

### <span data-ttu-id="96dc8-125">없음</span><span class="sxs-lookup"><span data-stu-id="96dc8-125">None</span></span>

## <span data-ttu-id="96dc8-126">출력</span><span class="sxs-lookup"><span data-stu-id="96dc8-126">OUTPUTS</span></span>

### <span data-ttu-id="96dc8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="96dc8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="96dc8-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96dc8-128">NOTES</span></span>

## <span data-ttu-id="96dc8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96dc8-129">RELATED LINKS</span></span>

[<span data-ttu-id="96dc8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="96dc8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)