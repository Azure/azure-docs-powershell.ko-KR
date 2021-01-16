---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493976"
---
# <span data-ttu-id="12b75-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="12b75-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="12b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12b75-102">SYNOPSIS</span></span>
<span data-ttu-id="12b75-103">배달 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="12b75-104">구문</span><span class="sxs-lookup"><span data-stu-id="12b75-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12b75-105">설명</span><span class="sxs-lookup"><span data-stu-id="12b75-105">DESCRIPTION</span></span>
<span data-ttu-id="12b75-106">**New-AzCdnDeliveryRule** cmdlet은 CDN 엔드포인트를 만들기 위한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="12b75-107">예제</span><span class="sxs-lookup"><span data-stu-id="12b75-107">EXAMPLES</span></span>

### <span data-ttu-id="12b75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="12b75-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="12b75-109">간단한 조건을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-109">Create a simple condition.</span></span>

## <span data-ttu-id="12b75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12b75-110">PARAMETERS</span></span>

### <span data-ttu-id="12b75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b75-111">-DefaultProfile</span></span>
<span data-ttu-id="12b75-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b75-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="12b75-113">-MatchValue</span></span>
<span data-ttu-id="12b75-114">가능한 일치 값 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b75-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="12b75-115">-MatchVariable</span></span>
<span data-ttu-id="12b75-116">조건의 일치 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="12b75-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="12b75-117">-NegateCondition</span></span>
<span data-ttu-id="12b75-118">이 조건의 결과가 부호가 될지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="12b75-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="12b75-119">-Operator</span></span>
<span data-ttu-id="12b75-120">일치할 연산자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="12b75-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="12b75-121">-Selector</span></span>
<span data-ttu-id="12b75-122">일치할 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="12b75-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="12b75-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="12b75-123">-Transform</span></span>
<span data-ttu-id="12b75-124">일치하기 전에 적용할 변환입니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-124">Transform to apply before matching.</span></span>
<span data-ttu-id="12b75-125">가능한 값은 소문자 및 대문자입니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="12b75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b75-126">CommonParameters</span></span>
<span data-ttu-id="12b75-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12b75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b75-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12b75-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b75-129">입력</span><span class="sxs-lookup"><span data-stu-id="12b75-129">INPUTS</span></span>

### <span data-ttu-id="12b75-130">없음</span><span class="sxs-lookup"><span data-stu-id="12b75-130">None</span></span>

## <span data-ttu-id="12b75-131">출력</span><span class="sxs-lookup"><span data-stu-id="12b75-131">OUTPUTS</span></span>

### <span data-ttu-id="12b75-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="12b75-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="12b75-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12b75-133">NOTES</span></span>

## <span data-ttu-id="12b75-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12b75-134">RELATED LINKS</span></span>
