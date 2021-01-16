---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336938"
---
# <span data-ttu-id="3590c-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="3590c-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="3590c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3590c-102">SYNOPSIS</span></span>
<span data-ttu-id="3590c-103">사용 가능한 Azure Firewall Fqdn 태그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="3590c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3590c-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3590c-105">설명</span><span class="sxs-lookup"><span data-stu-id="3590c-105">DESCRIPTION</span></span>
<span data-ttu-id="3590c-106">**Get-AzFirewallFqdnTag** cmdlet은 Azure Firewall 애플리케이션 규칙에 사용할 수 있는 FQDN 태그 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="3590c-107">예제</span><span class="sxs-lookup"><span data-stu-id="3590c-107">EXAMPLES</span></span>

### <span data-ttu-id="3590c-108">1: 사용 가능한 모든 FQDN 태그 검색</span><span class="sxs-lookup"><span data-stu-id="3590c-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="3590c-109">이 예제에서는 사용 가능한 모든 FQDN 태그를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="3590c-110">2: 애플리케이션 규칙에서 사용 가능한 첫 번째 FQDN 태그 사용</span><span class="sxs-lookup"><span data-stu-id="3590c-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="3590c-111">이 예제에서는 사용 가능한 첫 번째 FQDN 태그를 사용하여 방화벽 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="3590c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3590c-112">PARAMETERS</span></span>

### <span data-ttu-id="3590c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3590c-113">-DefaultProfile</span></span>
<span data-ttu-id="3590c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3590c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3590c-115">CommonParameters</span></span>
<span data-ttu-id="3590c-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3590c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3590c-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3590c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3590c-118">입력</span><span class="sxs-lookup"><span data-stu-id="3590c-118">INPUTS</span></span>

### <span data-ttu-id="3590c-119">없음</span><span class="sxs-lookup"><span data-stu-id="3590c-119">None</span></span>

## <span data-ttu-id="3590c-120">출력</span><span class="sxs-lookup"><span data-stu-id="3590c-120">OUTPUTS</span></span>

### <span data-ttu-id="3590c-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="3590c-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="3590c-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3590c-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3590c-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3590c-123">NOTES</span></span>

## <span data-ttu-id="3590c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3590c-124">RELATED LINKS</span></span>

[<span data-ttu-id="3590c-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="3590c-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="3590c-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3590c-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
