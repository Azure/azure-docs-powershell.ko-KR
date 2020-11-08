---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044908"
---
# <span data-ttu-id="b5b05-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="b5b05-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="b5b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b05-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b05-103">배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="b5b05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5b05-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b05-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5b05-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b05-106">**AzCdnDeliveryRule** CMDLET은 CDN 끝점 만들기에 대 한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="b5b05-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5b05-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b05-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5b05-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="b5b05-109">간단한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-109">Create a simple rule.</span></span>

## <span data-ttu-id="b5b05-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5b05-110">PARAMETERS</span></span>

### <span data-ttu-id="b5b05-111">-작업</span><span class="sxs-lookup"><span data-stu-id="b5b05-111">-Action</span></span>
<span data-ttu-id="b5b05-112">규칙의 모든 조건이 충족 될 때 실행 되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b05-113">-조건</span><span class="sxs-lookup"><span data-stu-id="b5b05-113">-Condition</span></span>
<span data-ttu-id="b5b05-114">실행할 작업과 일치 해야 하는 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b05-115">-DefaultProfile</span></span>
<span data-ttu-id="b5b05-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b05-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b5b05-117">-Name</span></span>
<span data-ttu-id="b5b05-118">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="b5b05-118">Name of the rule</span></span>

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

### <span data-ttu-id="b5b05-119">-주문</span><span class="sxs-lookup"><span data-stu-id="b5b05-119">-Order</span></span>
<span data-ttu-id="b5b05-120">규칙의 순서</span><span class="sxs-lookup"><span data-stu-id="b5b05-120">Order of the rule</span></span>

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

### <span data-ttu-id="b5b05-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b05-121">CommonParameters</span></span>
<span data-ttu-id="b5b05-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b05-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b05-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5b05-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b05-124">입력</span><span class="sxs-lookup"><span data-stu-id="b5b05-124">INPUTS</span></span>

### <span data-ttu-id="b5b05-125">않아야</span><span class="sxs-lookup"><span data-stu-id="b5b05-125">None</span></span>

## <span data-ttu-id="b5b05-126">출력</span><span class="sxs-lookup"><span data-stu-id="b5b05-126">OUTPUTS</span></span>

### <span data-ttu-id="b5b05-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="b5b05-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="b5b05-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b5b05-128">NOTES</span></span>

## <span data-ttu-id="b5b05-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5b05-129">RELATED LINKS</span></span>
