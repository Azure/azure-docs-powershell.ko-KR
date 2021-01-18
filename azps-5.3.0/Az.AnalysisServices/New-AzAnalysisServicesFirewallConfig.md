---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494515"
---
# <span data-ttu-id="708a6-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="708a6-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="708a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="708a6-102">SYNOPSIS</span></span>
<span data-ttu-id="708a6-103">새 Analysis Services 방화벽 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="708a6-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="708a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="708a6-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="708a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="708a6-105">DESCRIPTION</span></span>
<span data-ttu-id="708a6-106">이 New-AzAnalysisServicesFirewallConfig 새 방화벽 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="708a6-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="708a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="708a6-107">EXAMPLES</span></span>

### <span data-ttu-id="708a6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="708a6-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="708a6-109">Power BI 서비스에서 액세스를 사용하도록 설정하는 동시에 두 개의 규칙으로 방화벽 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="708a6-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="708a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="708a6-110">PARAMETERS</span></span>

### <span data-ttu-id="708a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708a6-111">-DefaultProfile</span></span>
<span data-ttu-id="708a6-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="708a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="708a6-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="708a6-113">-EnablePowerBIService</span></span>
<span data-ttu-id="708a6-114">방화벽이 Power BI에서 액세스를 허용하는지 나타내는 플래그</span><span class="sxs-lookup"><span data-stu-id="708a6-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="708a6-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="708a6-115">-FirewallRule</span></span>
<span data-ttu-id="708a6-116">방화벽 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="708a6-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="708a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708a6-117">CommonParameters</span></span>
<span data-ttu-id="708a6-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="708a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708a6-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="708a6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708a6-120">입력</span><span class="sxs-lookup"><span data-stu-id="708a6-120">INPUTS</span></span>

### <span data-ttu-id="708a6-121">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="708a6-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="708a6-122">출력</span><span class="sxs-lookup"><span data-stu-id="708a6-122">OUTPUTS</span></span>

### <span data-ttu-id="708a6-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="708a6-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="708a6-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="708a6-124">NOTES</span></span>

## <span data-ttu-id="708a6-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="708a6-125">RELATED LINKS</span></span>

[<span data-ttu-id="708a6-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="708a6-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)