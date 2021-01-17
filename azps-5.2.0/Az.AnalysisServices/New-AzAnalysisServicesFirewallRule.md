---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332810"
---
# <span data-ttu-id="b5062-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5062-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b5062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5062-102">SYNOPSIS</span></span>
<span data-ttu-id="b5062-103">새 Analysis Services 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5062-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="b5062-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5062-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5062-105">설명</span><span class="sxs-lookup"><span data-stu-id="b5062-105">DESCRIPTION</span></span>
<span data-ttu-id="b5062-106">이 New-AzAnalysisServicesFirewallRule 새 방화벽 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5062-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="b5062-107">예제</span><span class="sxs-lookup"><span data-stu-id="b5062-107">EXAMPLES</span></span>

### <span data-ttu-id="b5062-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5062-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="b5062-109">시작 범위 0.0.0.0 및 끝 범위 255.255.255.255를 통해 rule1이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5062-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="b5062-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5062-110">PARAMETERS</span></span>

### <span data-ttu-id="b5062-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5062-111">-DefaultProfile</span></span>
<span data-ttu-id="b5062-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5062-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5062-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b5062-113">-FirewallRuleName</span></span>
<span data-ttu-id="b5062-114">방화벽 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="b5062-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5062-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="b5062-115">-RangeEnd</span></span>
<span data-ttu-id="b5062-116">방화벽 규칙의 범위 끝</span><span class="sxs-lookup"><span data-stu-id="b5062-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5062-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="b5062-117">-RangeStart</span></span>
<span data-ttu-id="b5062-118">방화벽 규칙의 범위 시작</span><span class="sxs-lookup"><span data-stu-id="b5062-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5062-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5062-119">CommonParameters</span></span>
<span data-ttu-id="b5062-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5062-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5062-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b5062-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5062-122">입력</span><span class="sxs-lookup"><span data-stu-id="b5062-122">INPUTS</span></span>

### <span data-ttu-id="b5062-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b5062-123">System.String</span></span>

## <span data-ttu-id="b5062-124">출력</span><span class="sxs-lookup"><span data-stu-id="b5062-124">OUTPUTS</span></span>

### <span data-ttu-id="b5062-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5062-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b5062-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5062-126">NOTES</span></span>

## <span data-ttu-id="b5062-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5062-127">RELATED LINKS</span></span>

[<span data-ttu-id="b5062-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b5062-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)