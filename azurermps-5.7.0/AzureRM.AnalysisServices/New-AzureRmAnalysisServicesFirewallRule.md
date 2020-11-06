---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532880"
---
# <span data-ttu-id="50918-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="50918-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="50918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50918-102">SYNOPSIS</span></span>
<span data-ttu-id="50918-103">새 Analysis Services 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50918-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50918-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50918-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="50918-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50918-105">DESCRIPTION</span></span>
<span data-ttu-id="50918-106">New-AzureRmAnalysisServicesFirewallRule에서 새 방화벽 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50918-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="50918-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50918-107">EXAMPLES</span></span>

### <span data-ttu-id="50918-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="50918-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="50918-109">시작 범위가 0.0.0.0이 고 끝 범위가 255.255.255.255 인 rule1 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50918-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="50918-110">변수</span><span class="sxs-lookup"><span data-stu-id="50918-110">PARAMETERS</span></span>

### <span data-ttu-id="50918-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="50918-111">-FirewallRuleName</span></span>
<span data-ttu-id="50918-112">방화벽 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="50918-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50918-113">-차원 시작</span><span class="sxs-lookup"><span data-stu-id="50918-113">-RangeStart</span></span>
<span data-ttu-id="50918-114">방화벽 규칙 시작 범위</span><span class="sxs-lookup"><span data-stu-id="50918-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50918-115">-규격 종료</span><span class="sxs-lookup"><span data-stu-id="50918-115">-RangeEnd</span></span>
<span data-ttu-id="50918-116">방화벽 규칙의 범위 종료</span><span class="sxs-lookup"><span data-stu-id="50918-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="50918-117">입력</span><span class="sxs-lookup"><span data-stu-id="50918-117">INPUTS</span></span>

## <span data-ttu-id="50918-118">출력</span><span class="sxs-lookup"><span data-stu-id="50918-118">OUTPUTS</span></span>

### <span data-ttu-id="50918-119">AnalysisServices. AzureAnalysisServicesFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="50918-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="50918-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50918-120">RELATED LINKS</span></span>

[<span data-ttu-id="50918-121">새로운 AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="50918-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
