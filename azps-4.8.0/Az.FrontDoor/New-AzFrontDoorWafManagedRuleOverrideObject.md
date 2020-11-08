---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213574"
---
# <span data-ttu-id="25cf3-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="25cf3-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="25cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="25cf3-103">관리 규칙 재정의 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="25cf3-103">Create managed rule override object</span></span>

## <span data-ttu-id="25cf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25cf3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25cf3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="25cf3-106">관리 WAF 규칙 그룹에 대해 PSAzureManagedRuleOverride 개체 만들기 개체 생성을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cf3-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="25cf3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="25cf3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="25cf3-108">Example 1</span></span>
<span data-ttu-id="25cf3-109">규칙 942250 (SQLI 그룹에 있음)에 대 한 관리 규칙 재정의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25cf3-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="25cf3-110">변수</span><span class="sxs-lookup"><span data-stu-id="25cf3-110">PARAMETERS</span></span>

### <span data-ttu-id="25cf3-111">-작업</span><span class="sxs-lookup"><span data-stu-id="25cf3-111">-Action</span></span>
<span data-ttu-id="25cf3-112">재정의 작업</span><span class="sxs-lookup"><span data-stu-id="25cf3-112">Override Action</span></span>

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

### <span data-ttu-id="25cf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cf3-113">-DefaultProfile</span></span>
<span data-ttu-id="25cf3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25cf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cf3-115">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="25cf3-115">-Disabled</span></span>
<span data-ttu-id="25cf3-116">비활성 상태</span><span class="sxs-lookup"><span data-stu-id="25cf3-116">Disabled state</span></span>

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

### <span data-ttu-id="25cf3-117">-제외</span><span class="sxs-lookup"><span data-stu-id="25cf3-117">-Exclusion</span></span>
<span data-ttu-id="25cf3-118">전용</span><span class="sxs-lookup"><span data-stu-id="25cf3-118">Exclusion</span></span>

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

### <span data-ttu-id="25cf3-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="25cf3-119">-RuleId</span></span>
<span data-ttu-id="25cf3-120">규칙 ID</span><span class="sxs-lookup"><span data-stu-id="25cf3-120">Rule ID</span></span>

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

### <span data-ttu-id="25cf3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cf3-121">CommonParameters</span></span>
<span data-ttu-id="25cf3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cf3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cf3-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25cf3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cf3-124">입력</span><span class="sxs-lookup"><span data-stu-id="25cf3-124">INPUTS</span></span>

### <span data-ttu-id="25cf3-125">않아야</span><span class="sxs-lookup"><span data-stu-id="25cf3-125">None</span></span>

## <span data-ttu-id="25cf3-126">출력</span><span class="sxs-lookup"><span data-stu-id="25cf3-126">OUTPUTS</span></span>

### <span data-ttu-id="25cf3-127">FrontDoor를 통해 PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="25cf3-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="25cf3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="25cf3-128">NOTES</span></span>

## <span data-ttu-id="25cf3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25cf3-129">RELATED LINKS</span></span>

[<span data-ttu-id="25cf3-130">새로운 AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="25cf3-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)