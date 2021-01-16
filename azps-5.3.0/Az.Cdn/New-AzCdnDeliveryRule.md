---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493978"
---
# <span data-ttu-id="3e6ef-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="3e6ef-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="3e6ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6ef-103">배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="3e6ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e6ef-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6ef-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e6ef-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6ef-106">**New-AzCdnDeliveryRule** cmdlet은 CDN 엔드포인트를 만들기 위한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="3e6ef-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e6ef-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6ef-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e6ef-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="3e6ef-109">간단한 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-109">Create a simple rule.</span></span>

## <span data-ttu-id="3e6ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e6ef-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6ef-111">-Action</span><span class="sxs-lookup"><span data-stu-id="3e6ef-111">-Action</span></span>
<span data-ttu-id="3e6ef-112">규칙의 모든 조건이 충족될 때 실행되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="3e6ef-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="3e6ef-113">-Condition</span></span>
<span data-ttu-id="3e6ef-114">실행할 작업에 대해 일치해야 하는 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="3e6ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6ef-115">-DefaultProfile</span></span>
<span data-ttu-id="3e6ef-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6ef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3e6ef-117">-Name</span></span>
<span data-ttu-id="3e6ef-118">규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="3e6ef-118">Name of the rule</span></span>

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

### <span data-ttu-id="3e6ef-119">-Order</span><span class="sxs-lookup"><span data-stu-id="3e6ef-119">-Order</span></span>
<span data-ttu-id="3e6ef-120">규칙 순서</span><span class="sxs-lookup"><span data-stu-id="3e6ef-120">Order of the rule</span></span>

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

### <span data-ttu-id="3e6ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6ef-121">CommonParameters</span></span>
<span data-ttu-id="3e6ef-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6ef-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e6ef-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6ef-124">입력</span><span class="sxs-lookup"><span data-stu-id="3e6ef-124">INPUTS</span></span>

### <span data-ttu-id="3e6ef-125">없음</span><span class="sxs-lookup"><span data-stu-id="3e6ef-125">None</span></span>

## <span data-ttu-id="3e6ef-126">출력</span><span class="sxs-lookup"><span data-stu-id="3e6ef-126">OUTPUTS</span></span>

### <span data-ttu-id="3e6ef-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="3e6ef-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="3e6ef-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e6ef-128">NOTES</span></span>

## <span data-ttu-id="3e6ef-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e6ef-129">RELATED LINKS</span></span>
