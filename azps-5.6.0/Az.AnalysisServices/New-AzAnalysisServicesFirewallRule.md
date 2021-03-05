---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 4936571126a00d34fc91d2f7cbd85b232f18b4fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999026"
---
# <span data-ttu-id="78864-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78864-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="78864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78864-102">SYNOPSIS</span></span>
<span data-ttu-id="78864-103">새 Analysis Services 방화벽 규칙 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78864-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="78864-104">구문</span><span class="sxs-lookup"><span data-stu-id="78864-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78864-105">설명</span><span class="sxs-lookup"><span data-stu-id="78864-105">DESCRIPTION</span></span>
<span data-ttu-id="78864-106">New-AzAnalysisServicesFirewallRule 새 방화벽 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78864-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="78864-107">예제</span><span class="sxs-lookup"><span data-stu-id="78864-107">EXAMPLES</span></span>

### <span data-ttu-id="78864-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="78864-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="78864-109">시작 범위 0.0.0.0.0 및 종료 범위 255.255.255.255로 rule1이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78864-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="78864-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="78864-110">PARAMETERS</span></span>

### <span data-ttu-id="78864-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78864-111">-DefaultProfile</span></span>
<span data-ttu-id="78864-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78864-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78864-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="78864-113">-FirewallRuleName</span></span>
<span data-ttu-id="78864-114">방화벽 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="78864-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="78864-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="78864-115">-RangeEnd</span></span>
<span data-ttu-id="78864-116">방화벽 규칙의 범위 끝</span><span class="sxs-lookup"><span data-stu-id="78864-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="78864-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="78864-117">-RangeStart</span></span>
<span data-ttu-id="78864-118">방화벽 규칙의 범위 시작</span><span class="sxs-lookup"><span data-stu-id="78864-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="78864-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78864-119">CommonParameters</span></span>
<span data-ttu-id="78864-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78864-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78864-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78864-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78864-122">입력</span><span class="sxs-lookup"><span data-stu-id="78864-122">INPUTS</span></span>

### <span data-ttu-id="78864-123">System.String</span><span class="sxs-lookup"><span data-stu-id="78864-123">System.String</span></span>

## <span data-ttu-id="78864-124">출력</span><span class="sxs-lookup"><span data-stu-id="78864-124">OUTPUTS</span></span>

### <span data-ttu-id="78864-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78864-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="78864-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78864-126">NOTES</span></span>

## <span data-ttu-id="78864-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78864-127">RELATED LINKS</span></span>

[<span data-ttu-id="78864-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="78864-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)