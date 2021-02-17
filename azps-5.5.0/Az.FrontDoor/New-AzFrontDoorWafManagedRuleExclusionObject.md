---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180636"
---
# <span data-ttu-id="fa5e1-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="fa5e1-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="fa5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5e1-103">WAF 관리 규칙 집합, 그룹 또는 규칙에 대한 관리되는 규칙 제외 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fa5e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa5e1-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa5e1-105">설명</span><span class="sxs-lookup"><span data-stu-id="fa5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5e1-106">WAF 관리 규칙 집합, 그룹 또는 규칙에 대한 관리되는 규칙 제외 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fa5e1-107">예제</span><span class="sxs-lookup"><span data-stu-id="fa5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="fa5e1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa5e1-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="fa5e1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa5e1-109">PARAMETERS</span></span>

### <span data-ttu-id="fa5e1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5e1-110">-DefaultProfile</span></span>
<span data-ttu-id="fa5e1-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa5e1-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="fa5e1-112">-Operator</span></span>
<span data-ttu-id="fa5e1-113">선택기와 일치할 때 사용할 연산자입니다. EqualsAny는 선택기 없음(지정된 형식의 모든 일치 변수)을 의미하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="fa5e1-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="fa5e1-114">-Selector</span></span>
<span data-ttu-id="fa5e1-115">연산자를 사용하여 일치하는 선택기 패턴(연산자가 EqualsAny가 아닌 경우)</span><span class="sxs-lookup"><span data-stu-id="fa5e1-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="fa5e1-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="fa5e1-116">-Variable</span></span>
<span data-ttu-id="fa5e1-117">일치 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-117">Match variable.</span></span> <span data-ttu-id="fa5e1-118">가능한 값은 RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="fa5e1-119">예를 들어 QueryStringArgNames는 선택기와 주어진 연산자와 일치하는 GET 매개 변수를 제외한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="fa5e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5e1-120">CommonParameters</span></span>
<span data-ttu-id="fa5e1-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5e1-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa5e1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5e1-123">입력</span><span class="sxs-lookup"><span data-stu-id="fa5e1-123">INPUTS</span></span>

### <span data-ttu-id="fa5e1-124">없음</span><span class="sxs-lookup"><span data-stu-id="fa5e1-124">None</span></span>

## <span data-ttu-id="fa5e1-125">출력</span><span class="sxs-lookup"><span data-stu-id="fa5e1-125">OUTPUTS</span></span>

### <span data-ttu-id="fa5e1-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="fa5e1-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="fa5e1-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa5e1-127">NOTES</span></span>

## <span data-ttu-id="fa5e1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa5e1-128">RELATED LINKS</span></span>

<span data-ttu-id="fa5e1-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="fa5e1-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
