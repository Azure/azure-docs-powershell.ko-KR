---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868365"
---
# <span data-ttu-id="39b90-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="39b90-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="39b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b90-102">SYNOPSIS</span></span>
<span data-ttu-id="39b90-103">WAF 정책 만들기에 대 한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="39b90-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="39b90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39b90-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39b90-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39b90-105">DESCRIPTION</span></span>
<span data-ttu-id="39b90-106">WAF 정책 만들기에 대 한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="39b90-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="39b90-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39b90-107">EXAMPLES</span></span>

### <span data-ttu-id="39b90-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="39b90-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="39b90-109">RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="39b90-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="39b90-110">변수</span><span class="sxs-lookup"><span data-stu-id="39b90-110">PARAMETERS</span></span>

### <span data-ttu-id="39b90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b90-111">-DefaultProfile</span></span>
<span data-ttu-id="39b90-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39b90-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b90-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="39b90-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="39b90-114">규칙 무시 목록</span><span class="sxs-lookup"><span data-stu-id="39b90-114">Rule override list</span></span>

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

### <span data-ttu-id="39b90-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="39b90-115">-RuleGroupName</span></span>
<span data-ttu-id="39b90-116">이러한 재정의가 적용 되는 규칙 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="39b90-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="39b90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b90-117">CommonParameters</span></span>
<span data-ttu-id="39b90-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b90-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39b90-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b90-120">입력</span><span class="sxs-lookup"><span data-stu-id="39b90-120">INPUTS</span></span>

### <span data-ttu-id="39b90-121">않아야</span><span class="sxs-lookup"><span data-stu-id="39b90-121">None</span></span>

## <span data-ttu-id="39b90-122">출력</span><span class="sxs-lookup"><span data-stu-id="39b90-122">OUTPUTS</span></span>

### <span data-ttu-id="39b90-123">FrontDoor. PSAzureRuleGroupOverride/.</span><span class="sxs-lookup"><span data-stu-id="39b90-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="39b90-124">상속자</span><span class="sxs-lookup"><span data-stu-id="39b90-124">NOTES</span></span>

## <span data-ttu-id="39b90-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39b90-125">RELATED LINKS</span></span>

[<span data-ttu-id="39b90-126">새로운 AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="39b90-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
