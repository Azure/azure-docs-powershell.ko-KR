---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400674"
---
# <span data-ttu-id="500a1-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="500a1-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="500a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500a1-102">SYNOPSIS</span></span>
<span data-ttu-id="500a1-103">WAF 정책 만들기를 위한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="500a1-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="500a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="500a1-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="500a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="500a1-105">DESCRIPTION</span></span>
<span data-ttu-id="500a1-106">WAF 정책 만들기를 위한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="500a1-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="500a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="500a1-107">EXAMPLES</span></span>

### <span data-ttu-id="500a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="500a1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="500a1-109">CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="500a1-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="500a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500a1-110">PARAMETERS</span></span>

### <span data-ttu-id="500a1-111">-Action</span><span class="sxs-lookup"><span data-stu-id="500a1-111">-Action</span></span>
<span data-ttu-id="500a1-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-112">Type of Actions.</span></span>
<span data-ttu-id="500a1-113">가능한 값은 'Allow', 'Block', 'Log'입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="500a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500a1-114">-DefaultProfile</span></span>
<span data-ttu-id="500a1-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500a1-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="500a1-116">-MatchCondition</span></span>
<span data-ttu-id="500a1-117">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-117">List of match conditions.</span></span>

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

### <span data-ttu-id="500a1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="500a1-118">-Name</span></span>
<span data-ttu-id="500a1-119">규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="500a1-119">Name of the rule</span></span>

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

### <span data-ttu-id="500a1-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="500a1-120">-Priority</span></span>
<span data-ttu-id="500a1-121">규칙의 우선 순위를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="500a1-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="500a1-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="500a1-123">속도 제한 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-123">Rate limit duration.</span></span> <span data-ttu-id="500a1-124">기본값 - 1분</span><span class="sxs-lookup"><span data-stu-id="500a1-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="500a1-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="500a1-125">-RateLimitThreshold</span></span>
<span data-ttu-id="500a1-126">속도 제한 제한</span><span class="sxs-lookup"><span data-stu-id="500a1-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="500a1-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="500a1-127">-RuleType</span></span>
<span data-ttu-id="500a1-128">규칙의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-128">Type of the rule.</span></span>
<span data-ttu-id="500a1-129">가능한 값은 'MatchRule', 'RateLimitRule'입니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="500a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500a1-130">CommonParameters</span></span>
<span data-ttu-id="500a1-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="500a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500a1-132">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="500a1-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500a1-133">입력</span><span class="sxs-lookup"><span data-stu-id="500a1-133">INPUTS</span></span>

### <span data-ttu-id="500a1-134">없음</span><span class="sxs-lookup"><span data-stu-id="500a1-134">None</span></span>

## <span data-ttu-id="500a1-135">출력</span><span class="sxs-lookup"><span data-stu-id="500a1-135">OUTPUTS</span></span>

### <span data-ttu-id="500a1-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="500a1-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="500a1-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="500a1-137">NOTES</span></span>

## <span data-ttu-id="500a1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="500a1-138">RELATED LINKS</span></span>

<span data-ttu-id="500a1-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="500a1-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
