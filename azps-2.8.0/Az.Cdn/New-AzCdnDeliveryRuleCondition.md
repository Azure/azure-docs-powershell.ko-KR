---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697582"
---
# <span data-ttu-id="75539-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="75539-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="75539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75539-102">SYNOPSIS</span></span>
<span data-ttu-id="75539-103">배달 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75539-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="75539-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75539-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75539-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75539-105">DESCRIPTION</span></span>
<span data-ttu-id="75539-106">**AzCdnDeliveryRule** CMDLET은 CDN 끝점 만들기에 대 한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75539-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="75539-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75539-107">EXAMPLES</span></span>

### <span data-ttu-id="75539-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="75539-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="75539-109">간단한 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75539-109">Create a simple condition.</span></span>

## <span data-ttu-id="75539-110">변수</span><span class="sxs-lookup"><span data-stu-id="75539-110">PARAMETERS</span></span>

### <span data-ttu-id="75539-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75539-111">-DefaultProfile</span></span>
<span data-ttu-id="75539-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75539-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75539-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="75539-113">-MatchValue</span></span>
<span data-ttu-id="75539-114">사용할 수 있는 일치 값 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="75539-114">List of possible match values.</span></span>

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

### <span data-ttu-id="75539-115">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="75539-115">-MatchVariable</span></span>
<span data-ttu-id="75539-116">조건의 짝이 되는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="75539-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="75539-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="75539-117">-NegateCondition</span></span>
<span data-ttu-id="75539-118">이 조건의 결과를 부정할 수 있는지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="75539-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="75539-119">-연산자</span><span class="sxs-lookup"><span data-stu-id="75539-119">-Operator</span></span>
<span data-ttu-id="75539-120">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="75539-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="75539-121">-변환</span><span class="sxs-lookup"><span data-stu-id="75539-121">-Transform</span></span>
<span data-ttu-id="75539-122">일치 하기 전에 적용할 변환</span><span class="sxs-lookup"><span data-stu-id="75539-122">Transform to apply before matching.</span></span>
<span data-ttu-id="75539-123">사용할 수 있는 값은 소문자와 대문자입니다.</span><span class="sxs-lookup"><span data-stu-id="75539-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="75539-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75539-124">CommonParameters</span></span>
<span data-ttu-id="75539-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75539-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75539-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75539-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75539-127">입력</span><span class="sxs-lookup"><span data-stu-id="75539-127">INPUTS</span></span>

### <span data-ttu-id="75539-128">않아야</span><span class="sxs-lookup"><span data-stu-id="75539-128">None</span></span>

## <span data-ttu-id="75539-129">출력</span><span class="sxs-lookup"><span data-stu-id="75539-129">OUTPUTS</span></span>

### <span data-ttu-id="75539-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="75539-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="75539-131">상속자</span><span class="sxs-lookup"><span data-stu-id="75539-131">NOTES</span></span>

## <span data-ttu-id="75539-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75539-132">RELATED LINKS</span></span>
