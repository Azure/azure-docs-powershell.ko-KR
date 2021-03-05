---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970848"
---
# <span data-ttu-id="8609c-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="8609c-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="8609c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8609c-102">SYNOPSIS</span></span>
<span data-ttu-id="8609c-103">관리되는 규칙 오버라이드 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8609c-103">Create managed rule override object</span></span>

## <span data-ttu-id="8609c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8609c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8609c-105">설명</span><span class="sxs-lookup"><span data-stu-id="8609c-105">DESCRIPTION</span></span>
<span data-ttu-id="8609c-106">관리되는 WAF 규칙 그룹에 대한 PSAzureManagedRuleOverride 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8609c-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="8609c-107">예제</span><span class="sxs-lookup"><span data-stu-id="8609c-107">EXAMPLES</span></span>

### <span data-ttu-id="8609c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8609c-108">Example 1</span></span>
<span data-ttu-id="8609c-109">규칙 942250(SQLI 그룹에 있는)에 대한 관리되는 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8609c-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="8609c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8609c-110">PARAMETERS</span></span>

### <span data-ttu-id="8609c-111">-Action</span><span class="sxs-lookup"><span data-stu-id="8609c-111">-Action</span></span>
<span data-ttu-id="8609c-112">작업재지정</span><span class="sxs-lookup"><span data-stu-id="8609c-112">Override Action</span></span>

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

### <span data-ttu-id="8609c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8609c-113">-DefaultProfile</span></span>
<span data-ttu-id="8609c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8609c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8609c-115">-사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="8609c-115">-Disabled</span></span>
<span data-ttu-id="8609c-116">사용하지 않도록 설정된 상태</span><span class="sxs-lookup"><span data-stu-id="8609c-116">Disabled state</span></span>

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

### <span data-ttu-id="8609c-117">-제외</span><span class="sxs-lookup"><span data-stu-id="8609c-117">-Exclusion</span></span>
<span data-ttu-id="8609c-118">제외</span><span class="sxs-lookup"><span data-stu-id="8609c-118">Exclusion</span></span>

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

### <span data-ttu-id="8609c-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="8609c-119">-RuleId</span></span>
<span data-ttu-id="8609c-120">규칙 ID</span><span class="sxs-lookup"><span data-stu-id="8609c-120">Rule ID</span></span>

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

### <span data-ttu-id="8609c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8609c-121">CommonParameters</span></span>
<span data-ttu-id="8609c-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8609c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8609c-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8609c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8609c-124">입력</span><span class="sxs-lookup"><span data-stu-id="8609c-124">INPUTS</span></span>

### <span data-ttu-id="8609c-125">없음</span><span class="sxs-lookup"><span data-stu-id="8609c-125">None</span></span>

## <span data-ttu-id="8609c-126">출력</span><span class="sxs-lookup"><span data-stu-id="8609c-126">OUTPUTS</span></span>

### <span data-ttu-id="8609c-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8609c-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="8609c-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8609c-128">NOTES</span></span>

## <span data-ttu-id="8609c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8609c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8609c-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="8609c-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)