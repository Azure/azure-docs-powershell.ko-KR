---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970928"
---
# <span data-ttu-id="4fe29-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="4fe29-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="4fe29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe29-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe29-103">WAF 정책 만들기에 대한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4fe29-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4fe29-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fe29-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe29-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fe29-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe29-106">WAF 정책 만들기에 대한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4fe29-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4fe29-107">예제</span><span class="sxs-lookup"><span data-stu-id="4fe29-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe29-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fe29-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="4fe29-109">CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4fe29-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="4fe29-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4fe29-110">PARAMETERS</span></span>

### <span data-ttu-id="4fe29-111">-Action</span><span class="sxs-lookup"><span data-stu-id="4fe29-111">-Action</span></span>
<span data-ttu-id="4fe29-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-112">Type of Actions.</span></span>
<span data-ttu-id="4fe29-113">가능한 값에는 '허용', '블록', 'Log'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="4fe29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe29-114">-DefaultProfile</span></span>
<span data-ttu-id="4fe29-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe29-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4fe29-116">-EnabledState</span></span>
<span data-ttu-id="4fe29-117">사용 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-117">Enabled State.</span></span> <span data-ttu-id="4fe29-118">가능한 값은 '사용', '사용 안 하세요'를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="4fe29-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="4fe29-119">-MatchCondition</span></span>
<span data-ttu-id="4fe29-120">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-120">List of match conditions.</span></span>

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

### <span data-ttu-id="4fe29-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe29-121">-Name</span></span>
<span data-ttu-id="4fe29-122">규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="4fe29-122">Name of the rule</span></span>

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

### <span data-ttu-id="4fe29-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="4fe29-123">-Priority</span></span>
<span data-ttu-id="4fe29-124">규칙의 우선 순위를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="4fe29-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="4fe29-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="4fe29-126">속도 제한 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-126">Rate limit duration.</span></span> <span data-ttu-id="4fe29-127">기본값 - 1분</span><span class="sxs-lookup"><span data-stu-id="4fe29-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="4fe29-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="4fe29-128">-RateLimitThreshold</span></span>
<span data-ttu-id="4fe29-129">속도 제한 임계값</span><span class="sxs-lookup"><span data-stu-id="4fe29-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="4fe29-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="4fe29-130">-RuleType</span></span>
<span data-ttu-id="4fe29-131">규칙의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-131">Type of the rule.</span></span>
<span data-ttu-id="4fe29-132">가능한 값은 다음과 같습니다. 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="4fe29-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="4fe29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe29-133">CommonParameters</span></span>
<span data-ttu-id="4fe29-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe29-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fe29-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe29-136">입력</span><span class="sxs-lookup"><span data-stu-id="4fe29-136">INPUTS</span></span>

### <span data-ttu-id="4fe29-137">없음</span><span class="sxs-lookup"><span data-stu-id="4fe29-137">None</span></span>

## <span data-ttu-id="4fe29-138">출력</span><span class="sxs-lookup"><span data-stu-id="4fe29-138">OUTPUTS</span></span>

### <span data-ttu-id="4fe29-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="4fe29-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="4fe29-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fe29-140">NOTES</span></span>

## <span data-ttu-id="4fe29-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fe29-141">RELATED LINKS</span></span>

<span data-ttu-id="4fe29-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="4fe29-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
