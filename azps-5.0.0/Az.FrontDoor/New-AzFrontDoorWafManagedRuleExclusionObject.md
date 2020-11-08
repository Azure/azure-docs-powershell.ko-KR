---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217404"
---
# <span data-ttu-id="fa2ec-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="fa2ec-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="fa2ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2ec-103">WAF 관리 규칙 집합, 그룹 또는 규칙에 대 한 관리 규칙 제외 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fa2ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa2ec-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa2ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa2ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2ec-106">WAF 관리 규칙 집합, 그룹 또는 규칙에 대 한 관리 규칙 제외 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="fa2ec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa2ec-107">EXAMPLES</span></span>

### <span data-ttu-id="fa2ec-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa2ec-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="fa2ec-109">변수</span><span class="sxs-lookup"><span data-stu-id="fa2ec-109">PARAMETERS</span></span>

### <span data-ttu-id="fa2ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2ec-110">-DefaultProfile</span></span>
<span data-ttu-id="fa2ec-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2ec-112">-연산자</span><span class="sxs-lookup"><span data-stu-id="fa2ec-112">-Operator</span></span>
<span data-ttu-id="fa2ec-113">선택기를 찾을 때 사용 하는 EqualsAny는 선택기를 의미 하지 않습니다 (지정 된 형식의 모든 일치 변수).</span><span class="sxs-lookup"><span data-stu-id="fa2ec-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="fa2ec-114">-선택기</span><span class="sxs-lookup"><span data-stu-id="fa2ec-114">-Selector</span></span>
<span data-ttu-id="fa2ec-115">연산자를 사용 하 여 일치 시킬 선택기 패턴 (연산자가 EqualsAny이 아닌 경우)</span><span class="sxs-lookup"><span data-stu-id="fa2ec-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="fa2ec-116">-변수</span><span class="sxs-lookup"><span data-stu-id="fa2ec-116">-Variable</span></span>
<span data-ttu-id="fa2ec-117">Match 변수</span><span class="sxs-lookup"><span data-stu-id="fa2ec-117">Match variable.</span></span> <span data-ttu-id="fa2ec-118">사용할 수 있는 값은 RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames입니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="fa2ec-119">예를 들어 QueryStringArgNames은 지정 된 연산자를 사용 하 여 선택기와 일치 하는 GET 매개 변수를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="fa2ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2ec-120">CommonParameters</span></span>
<span data-ttu-id="fa2ec-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2ec-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa2ec-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2ec-123">입력</span><span class="sxs-lookup"><span data-stu-id="fa2ec-123">INPUTS</span></span>

### <span data-ttu-id="fa2ec-124">않아야</span><span class="sxs-lookup"><span data-stu-id="fa2ec-124">None</span></span>

## <span data-ttu-id="fa2ec-125">출력</span><span class="sxs-lookup"><span data-stu-id="fa2ec-125">OUTPUTS</span></span>

### <span data-ttu-id="fa2ec-126">FrontDoor를 통해 PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="fa2ec-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="fa2ec-127">상속자</span><span class="sxs-lookup"><span data-stu-id="fa2ec-127">NOTES</span></span>

## <span data-ttu-id="fa2ec-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa2ec-128">RELATED LINKS</span></span>

<span data-ttu-id="fa2ec-129">[새로운 AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [새로운 AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [새로운 AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="fa2ec-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
