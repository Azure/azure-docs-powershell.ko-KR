---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703292"
---
# <span data-ttu-id="cce1f-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="cce1f-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="cce1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce1f-102">SYNOPSIS</span></span>
<span data-ttu-id="cce1f-103">새 Analysis Services 방화벽 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cce1f-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cce1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cce1f-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="cce1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cce1f-105">DESCRIPTION</span></span>
<span data-ttu-id="cce1f-106">New-AzureRmAnalysisServicesFirewallConfig에서 새 방화벽 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cce1f-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="cce1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cce1f-107">EXAMPLES</span></span>

### <span data-ttu-id="cce1f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cce1f-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="cce1f-109">Power bi 서비스를 사용 하지 않고 방화벽 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cce1f-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="cce1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="cce1f-110">PARAMETERS</span></span>

### <span data-ttu-id="cce1f-111">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="cce1f-111">-EnablePowerBIService</span></span>
<span data-ttu-id="cce1f-112">PowerBI 서비스 사용 여부를 나타내는 플래그</span><span class="sxs-lookup"><span data-stu-id="cce1f-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce1f-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="cce1f-113">-FirewallRules</span></span>
<span data-ttu-id="cce1f-114">방화벽 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="cce1f-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cce1f-115">입력</span><span class="sxs-lookup"><span data-stu-id="cce1f-115">INPUTS</span></span>

## <span data-ttu-id="cce1f-116">출력</span><span class="sxs-lookup"><span data-stu-id="cce1f-116">OUTPUTS</span></span>

### <span data-ttu-id="cce1f-117">AnalysisServices. AzureAnalysisServicesFirewallConfig/.</span><span class="sxs-lookup"><span data-stu-id="cce1f-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="cce1f-118">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cce1f-118">RELATED LINKS</span></span>

[<span data-ttu-id="cce1f-119">새로운 AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="cce1f-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
