---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868370"
---
# <span data-ttu-id="88353-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="88353-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="88353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88353-102">SYNOPSIS</span></span>
<span data-ttu-id="88353-103">관리 규칙 재정의 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="88353-103">Create managed rule override object</span></span>

## <span data-ttu-id="88353-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88353-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88353-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88353-105">DESCRIPTION</span></span>
<span data-ttu-id="88353-106">관리 WAF 규칙 그룹에 대해 PSAzureManagedRuleOverride 개체 만들기 개체 생성을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="88353-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="88353-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88353-107">EXAMPLES</span></span>

### <span data-ttu-id="88353-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="88353-108">Example 1</span></span>
<span data-ttu-id="88353-109">규칙 942250 (SQLI 그룹에 있음)에 대 한 관리 규칙 재정의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88353-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="88353-110">변수</span><span class="sxs-lookup"><span data-stu-id="88353-110">PARAMETERS</span></span>

### <span data-ttu-id="88353-111">-작업</span><span class="sxs-lookup"><span data-stu-id="88353-111">-Action</span></span>
<span data-ttu-id="88353-112">재정의 작업</span><span class="sxs-lookup"><span data-stu-id="88353-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88353-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88353-113">-DefaultProfile</span></span>
<span data-ttu-id="88353-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88353-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88353-115">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="88353-115">-Disabled</span></span>
<span data-ttu-id="88353-116">비활성 상태</span><span class="sxs-lookup"><span data-stu-id="88353-116">Disabled state</span></span>

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

### <span data-ttu-id="88353-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="88353-117">-RuleId</span></span>
<span data-ttu-id="88353-118">규칙 ID</span><span class="sxs-lookup"><span data-stu-id="88353-118">Rule ID</span></span>

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

### <span data-ttu-id="88353-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88353-119">CommonParameters</span></span>
<span data-ttu-id="88353-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88353-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88353-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88353-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88353-122">입력</span><span class="sxs-lookup"><span data-stu-id="88353-122">INPUTS</span></span>

### <span data-ttu-id="88353-123">않아야</span><span class="sxs-lookup"><span data-stu-id="88353-123">None</span></span>

## <span data-ttu-id="88353-124">출력</span><span class="sxs-lookup"><span data-stu-id="88353-124">OUTPUTS</span></span>

### <span data-ttu-id="88353-125">FrontDoor를 통해 PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="88353-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="88353-126">상속자</span><span class="sxs-lookup"><span data-stu-id="88353-126">NOTES</span></span>

## <span data-ttu-id="88353-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88353-127">RELATED LINKS</span></span>

[<span data-ttu-id="88353-128">새로운 AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="88353-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)