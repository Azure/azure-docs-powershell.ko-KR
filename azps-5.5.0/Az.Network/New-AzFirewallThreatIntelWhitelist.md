---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206704"
---
# <span data-ttu-id="45714-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="45714-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="45714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45714-102">SYNOPSIS</span></span>
<span data-ttu-id="45714-103">Azure Firewall에 대한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="45714-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="45714-104">구문</span><span class="sxs-lookup"><span data-stu-id="45714-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45714-105">설명</span><span class="sxs-lookup"><span data-stu-id="45714-105">DESCRIPTION</span></span>
<span data-ttu-id="45714-106">**New-AzFirewallThreatIntelWhitelist** cmdlet은 Azure Firewall을 만들거나 설정할 때 사용할 수 있는 위협 Intel 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45714-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="45714-107">예제</span><span class="sxs-lookup"><span data-stu-id="45714-107">EXAMPLES</span></span>

### <span data-ttu-id="45714-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="45714-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="45714-109">이 예제에서는 두 개의 항목으로 된 FQDN 화이트리스트와 두 개의 항목의 IP 주소 화이트리스트를 포함하는 위협 Intel 화이트리스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45714-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="45714-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45714-110">PARAMETERS</span></span>

### <span data-ttu-id="45714-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45714-111">-DefaultProfile</span></span>
<span data-ttu-id="45714-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45714-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45714-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="45714-113">-FQDN</span></span>
<span data-ttu-id="45714-114">위협 Intel 화이트리스트의 FQDNS</span><span class="sxs-lookup"><span data-stu-id="45714-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45714-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="45714-115">-IpAddress</span></span>
<span data-ttu-id="45714-116">위협 Intel 허용 목록의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="45714-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45714-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45714-117">CommonParameters</span></span>
<span data-ttu-id="45714-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45714-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45714-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45714-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45714-120">입력</span><span class="sxs-lookup"><span data-stu-id="45714-120">INPUTS</span></span>

### <span data-ttu-id="45714-121">없음</span><span class="sxs-lookup"><span data-stu-id="45714-121">None</span></span>

## <span data-ttu-id="45714-122">출력</span><span class="sxs-lookup"><span data-stu-id="45714-122">OUTPUTS</span></span>

### <span data-ttu-id="45714-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="45714-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="45714-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45714-124">NOTES</span></span>

## <span data-ttu-id="45714-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45714-125">RELATED LINKS</span></span>

[<span data-ttu-id="45714-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45714-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="45714-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45714-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="45714-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45714-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)