---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524412"
---
# <span data-ttu-id="470c7-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="470c7-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="470c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470c7-102">SYNOPSIS</span></span>
<span data-ttu-id="470c7-103">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="470c7-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="470c7-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="470c7-105">DESCRIPTION</span></span>
<span data-ttu-id="470c7-106">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="470c7-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="470c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="470c7-107">EXAMPLES</span></span>

### <span data-ttu-id="470c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="470c7-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="470c7-109">CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="470c7-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="470c7-110">변수</span><span class="sxs-lookup"><span data-stu-id="470c7-110">PARAMETERS</span></span>

### <span data-ttu-id="470c7-111">-작업</span><span class="sxs-lookup"><span data-stu-id="470c7-111">-Action</span></span>
<span data-ttu-id="470c7-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-112">Type of Actions.</span></span>
<span data-ttu-id="470c7-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 차단 ', ' 로그 '</span><span class="sxs-lookup"><span data-stu-id="470c7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470c7-114">-DefaultProfile</span></span>
<span data-ttu-id="470c7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470c7-116">MatchCondition</span><span class="sxs-lookup"><span data-stu-id="470c7-116">-MatchCondition</span></span>
<span data-ttu-id="470c7-117">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-117">List of match conditions.</span></span>

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

### <span data-ttu-id="470c7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="470c7-118">-Name</span></span>
<span data-ttu-id="470c7-119">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="470c7-119">Name of the rule</span></span>

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

### <span data-ttu-id="470c7-120">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="470c7-120">-Priority</span></span>
<span data-ttu-id="470c7-121">규칙의 우선 순위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="470c7-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="470c7-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="470c7-123">속도 제한 기간</span><span class="sxs-lookup"><span data-stu-id="470c7-123">Rate limit duration.</span></span> <span data-ttu-id="470c7-124">기본값-1 분</span><span class="sxs-lookup"><span data-stu-id="470c7-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="470c7-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="470c7-125">-RateLimitThreshold</span></span>
<span data-ttu-id="470c7-126">속도 제한 thresold</span><span class="sxs-lookup"><span data-stu-id="470c7-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="470c7-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="470c7-127">-RuleType</span></span>
<span data-ttu-id="470c7-128">규칙의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-128">Type of the rule.</span></span>
<span data-ttu-id="470c7-129">사용할 수 있는 값은 다음과 같습니다. ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="470c7-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="470c7-130">-변환</span><span class="sxs-lookup"><span data-stu-id="470c7-130">-Transform</span></span>
<span data-ttu-id="470c7-131">변형 목록</span><span class="sxs-lookup"><span data-stu-id="470c7-131">List of transforms</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470c7-132">CommonParameters</span></span>
<span data-ttu-id="470c7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="470c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470c7-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470c7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470c7-135">입력</span><span class="sxs-lookup"><span data-stu-id="470c7-135">INPUTS</span></span>

### <span data-ttu-id="470c7-136">않아야</span><span class="sxs-lookup"><span data-stu-id="470c7-136">None</span></span>

## <span data-ttu-id="470c7-137">출력</span><span class="sxs-lookup"><span data-stu-id="470c7-137">OUTPUTS</span></span>

### <span data-ttu-id="470c7-138">FrontDoor. PSCustomRule/.</span><span class="sxs-lookup"><span data-stu-id="470c7-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="470c7-139">상속자</span><span class="sxs-lookup"><span data-stu-id="470c7-139">NOTES</span></span>

## <span data-ttu-id="470c7-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="470c7-140">RELATED LINKS</span></span>

<span data-ttu-id="470c7-141">[새로운 AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="470c7-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
