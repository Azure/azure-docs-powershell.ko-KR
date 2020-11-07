---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 7fb766bfa65d37fd8491e93593b3ea423938fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689193"
---
# <span data-ttu-id="ed86e-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ed86e-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="ed86e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed86e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed86e-103">새 Analysis Services 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed86e-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="ed86e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed86e-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed86e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed86e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed86e-106">New-AzAnalysisServicesFirewallRule에서 새 방화벽 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed86e-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="ed86e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ed86e-107">EXAMPLES</span></span>

### <span data-ttu-id="ed86e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed86e-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="ed86e-109">시작 범위가 0.0.0.0이 고 끝 범위가 255.255.255.255 인 rule1 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed86e-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="ed86e-110">변수</span><span class="sxs-lookup"><span data-stu-id="ed86e-110">PARAMETERS</span></span>

### <span data-ttu-id="ed86e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed86e-111">-DefaultProfile</span></span>
<span data-ttu-id="ed86e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed86e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed86e-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ed86e-113">-FirewallRuleName</span></span>
<span data-ttu-id="ed86e-114">방화벽 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="ed86e-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="ed86e-115">-규격 종료</span><span class="sxs-lookup"><span data-stu-id="ed86e-115">-RangeEnd</span></span>
<span data-ttu-id="ed86e-116">방화벽 규칙의 범위 종료</span><span class="sxs-lookup"><span data-stu-id="ed86e-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="ed86e-117">-차원 시작</span><span class="sxs-lookup"><span data-stu-id="ed86e-117">-RangeStart</span></span>
<span data-ttu-id="ed86e-118">방화벽 규칙 시작 범위</span><span class="sxs-lookup"><span data-stu-id="ed86e-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="ed86e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed86e-119">CommonParameters</span></span>
<span data-ttu-id="ed86e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed86e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed86e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed86e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed86e-122">입력</span><span class="sxs-lookup"><span data-stu-id="ed86e-122">INPUTS</span></span>

### <span data-ttu-id="ed86e-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed86e-123">System.String</span></span>

## <span data-ttu-id="ed86e-124">출력</span><span class="sxs-lookup"><span data-stu-id="ed86e-124">OUTPUTS</span></span>

### <span data-ttu-id="ed86e-125">AnalysisServices. PsAzureAnalysisServicesFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="ed86e-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="ed86e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ed86e-126">NOTES</span></span>

## <span data-ttu-id="ed86e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed86e-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed86e-128">새로운 AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ed86e-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)