---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042850"
---
# <span data-ttu-id="358fa-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="358fa-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="358fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358fa-102">SYNOPSIS</span></span>
<span data-ttu-id="358fa-103">배달 규칙 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="358fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="358fa-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="358fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="358fa-105">DESCRIPTION</span></span>
<span data-ttu-id="358fa-106">**AzCdnDeliveryRule** CMDLET은 CDN 끝점 만들기에 대 한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="358fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="358fa-107">EXAMPLES</span></span>

### <span data-ttu-id="358fa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="358fa-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="358fa-109">간단한 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-109">Create a simple condition.</span></span>

## <span data-ttu-id="358fa-110">변수</span><span class="sxs-lookup"><span data-stu-id="358fa-110">PARAMETERS</span></span>

### <span data-ttu-id="358fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358fa-111">-DefaultProfile</span></span>
<span data-ttu-id="358fa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358fa-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="358fa-113">-MatchValue</span></span>
<span data-ttu-id="358fa-114">사용할 수 있는 일치 값 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-114">List of possible match values.</span></span>

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

### <span data-ttu-id="358fa-115">MatchVariable</span><span class="sxs-lookup"><span data-stu-id="358fa-115">-MatchVariable</span></span>
<span data-ttu-id="358fa-116">조건의 짝이 되는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="358fa-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="358fa-117">-NegateCondition</span></span>
<span data-ttu-id="358fa-118">이 조건의 결과를 부정할 수 있는지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="358fa-119">-연산자</span><span class="sxs-lookup"><span data-stu-id="358fa-119">-Operator</span></span>
<span data-ttu-id="358fa-120">일치 시킬 연산자에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="358fa-121">-선택기</span><span class="sxs-lookup"><span data-stu-id="358fa-121">-Selector</span></span>
<span data-ttu-id="358fa-122">일치 시킬 선택기 이름</span><span class="sxs-lookup"><span data-stu-id="358fa-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="358fa-123">-변환</span><span class="sxs-lookup"><span data-stu-id="358fa-123">-Transform</span></span>
<span data-ttu-id="358fa-124">일치 하기 전에 적용할 변환</span><span class="sxs-lookup"><span data-stu-id="358fa-124">Transform to apply before matching.</span></span>
<span data-ttu-id="358fa-125">사용할 수 있는 값은 소문자와 대문자입니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="358fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358fa-126">CommonParameters</span></span>
<span data-ttu-id="358fa-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="358fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358fa-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="358fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358fa-129">입력</span><span class="sxs-lookup"><span data-stu-id="358fa-129">INPUTS</span></span>

### <span data-ttu-id="358fa-130">않아야</span><span class="sxs-lookup"><span data-stu-id="358fa-130">None</span></span>

## <span data-ttu-id="358fa-131">출력</span><span class="sxs-lookup"><span data-stu-id="358fa-131">OUTPUTS</span></span>

### <span data-ttu-id="358fa-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="358fa-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="358fa-133">상속자</span><span class="sxs-lookup"><span data-stu-id="358fa-133">NOTES</span></span>

## <span data-ttu-id="358fa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="358fa-134">RELATED LINKS</span></span>
