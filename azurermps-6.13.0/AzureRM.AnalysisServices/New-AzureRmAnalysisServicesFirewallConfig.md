---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702500"
---
# <span data-ttu-id="fa381-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="fa381-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="fa381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa381-102">SYNOPSIS</span></span>
<span data-ttu-id="fa381-103">새 Analysis Services 방화벽 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa381-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa381-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa381-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa381-105">DESCRIPTION</span></span>
<span data-ttu-id="fa381-106">New-AzureRmAnalysisServicesFirewallConfig에서 새 방화벽 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="fa381-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa381-107">EXAMPLES</span></span>

### <span data-ttu-id="fa381-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa381-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="fa381-109">Power BI 서비스에서 액세스를 사용 하도록 설정 하는 동안 두 개의 규칙이 있는 방화벽 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="fa381-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa381-110">PARAMETERS</span></span>

### <span data-ttu-id="fa381-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa381-111">-DefaultProfile</span></span>
<span data-ttu-id="fa381-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa381-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="fa381-113">-EnablePowerBIService</span></span>
<span data-ttu-id="fa381-114">방화벽이 Power BI에서 액세스할 수 있는지 여부를 나타내는 플래그</span><span class="sxs-lookup"><span data-stu-id="fa381-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="fa381-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fa381-115">-FirewallRule</span></span>
<span data-ttu-id="fa381-116">방화벽 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="fa381-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="fa381-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa381-117">CommonParameters</span></span>
<span data-ttu-id="fa381-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa381-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa381-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa381-120">입력</span><span class="sxs-lookup"><span data-stu-id="fa381-120">INPUTS</span></span>

### <span data-ttu-id="fa381-121">AnalysisServices ' 1 [[Microsoft Azure. PsAzureAnalysisServicesFirewallRule, Microsoft Azure. AnalysisServices, Version = 0.6.11.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fa381-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fa381-122">출력</span><span class="sxs-lookup"><span data-stu-id="fa381-122">OUTPUTS</span></span>

### <span data-ttu-id="fa381-123">AnalysisServices. PsAzureAnalysisServicesFirewallConfig/.</span><span class="sxs-lookup"><span data-stu-id="fa381-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="fa381-124">상속자</span><span class="sxs-lookup"><span data-stu-id="fa381-124">NOTES</span></span>

## <span data-ttu-id="fa381-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa381-125">RELATED LINKS</span></span>

[<span data-ttu-id="fa381-126">새로운 AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fa381-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
