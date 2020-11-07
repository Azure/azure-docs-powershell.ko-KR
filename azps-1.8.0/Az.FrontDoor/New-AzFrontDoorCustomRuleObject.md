---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868402"
---
# <span data-ttu-id="921b4-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="921b4-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="921b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="921b4-102">SYNOPSIS</span></span>
<span data-ttu-id="921b4-103">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="921b4-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="921b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="921b4-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="921b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="921b4-105">DESCRIPTION</span></span>
<span data-ttu-id="921b4-106">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="921b4-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="921b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="921b4-107">EXAMPLES</span></span>

### <span data-ttu-id="921b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="921b4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="921b4-109">CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="921b4-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="921b4-110">변수</span><span class="sxs-lookup"><span data-stu-id="921b4-110">PARAMETERS</span></span>

### <span data-ttu-id="921b4-111">-작업</span><span class="sxs-lookup"><span data-stu-id="921b4-111">-Action</span></span>
<span data-ttu-id="921b4-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-112">Type of Actions.</span></span>
<span data-ttu-id="921b4-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 차단 ', ' 로그 '</span><span class="sxs-lookup"><span data-stu-id="921b4-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921b4-114">-DefaultProfile</span></span>
<span data-ttu-id="921b4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="921b4-116">MatchCondition</span><span class="sxs-lookup"><span data-stu-id="921b4-116">-MatchCondition</span></span>
<span data-ttu-id="921b4-117">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="921b4-118">-Name</span></span>
<span data-ttu-id="921b4-119">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="921b4-119">Name of the rule</span></span>

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

### <span data-ttu-id="921b4-120">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="921b4-120">-Priority</span></span>
<span data-ttu-id="921b4-121">규칙의 우선 순위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-121">Describes priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="921b4-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="921b4-123">속도 제한 기간</span><span class="sxs-lookup"><span data-stu-id="921b4-123">Rate limit duration.</span></span> <span data-ttu-id="921b4-124">기본값-1 분</span><span class="sxs-lookup"><span data-stu-id="921b4-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="921b4-125">-RateLimitThreshold</span></span>
<span data-ttu-id="921b4-126">속도 제한 thresold</span><span class="sxs-lookup"><span data-stu-id="921b4-126">Rate limit thresold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="921b4-127">-RuleType</span></span>
<span data-ttu-id="921b4-128">규칙의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-128">Type of the rule.</span></span>
<span data-ttu-id="921b4-129">사용할 수 있는 값은 다음과 같습니다. ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="921b4-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921b4-130">CommonParameters</span></span>
<span data-ttu-id="921b4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="921b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921b4-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921b4-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921b4-133">입력</span><span class="sxs-lookup"><span data-stu-id="921b4-133">INPUTS</span></span>

### <span data-ttu-id="921b4-134">않아야</span><span class="sxs-lookup"><span data-stu-id="921b4-134">None</span></span>

## <span data-ttu-id="921b4-135">출력</span><span class="sxs-lookup"><span data-stu-id="921b4-135">OUTPUTS</span></span>

### <span data-ttu-id="921b4-136">FrontDoor. PSCustomRule/.</span><span class="sxs-lookup"><span data-stu-id="921b4-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="921b4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="921b4-137">NOTES</span></span>

## <span data-ttu-id="921b4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="921b4-138">RELATED LINKS</span></span>

<span data-ttu-id="921b4-139">[새로운 AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="921b4-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
