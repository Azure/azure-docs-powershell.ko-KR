---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211579"
---
# <span data-ttu-id="6d5af-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="6d5af-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="6d5af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5af-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5af-103">Azure 방화벽에 대 한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="6d5af-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="6d5af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d5af-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d5af-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5af-106">**AzFirewallThreatIntelWhitelist** Cmdlet은 Azure 방화벽을 만들거나 설정할 때 사용할 수 있는 위협 intel 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d5af-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="6d5af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d5af-107">EXAMPLES</span></span>

### <span data-ttu-id="6d5af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d5af-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="6d5af-109">이 예제에서는 두 개의 항목에 대 한 FQDN 허용 목록을 포함 하는 intel 허용 목록와 두 개의 항목에 대 한 Ip 주소 허용 목록를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d5af-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="6d5af-110">변수</span><span class="sxs-lookup"><span data-stu-id="6d5af-110">PARAMETERS</span></span>

### <span data-ttu-id="6d5af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5af-111">-DefaultProfile</span></span>
<span data-ttu-id="6d5af-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5af-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="6d5af-113">-FQDN</span></span>
<span data-ttu-id="6d5af-114">위협 인텔 허용 목록의 Fqdn</span><span class="sxs-lookup"><span data-stu-id="6d5af-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="6d5af-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6d5af-115">-IpAddress</span></span>
<span data-ttu-id="6d5af-116">위협의 IP 주소 인텔 허용 목록</span><span class="sxs-lookup"><span data-stu-id="6d5af-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="6d5af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5af-117">CommonParameters</span></span>
<span data-ttu-id="6d5af-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5af-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d5af-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5af-120">입력</span><span class="sxs-lookup"><span data-stu-id="6d5af-120">INPUTS</span></span>

### <span data-ttu-id="6d5af-121">않아야</span><span class="sxs-lookup"><span data-stu-id="6d5af-121">None</span></span>

## <span data-ttu-id="6d5af-122">출력</span><span class="sxs-lookup"><span data-stu-id="6d5af-122">OUTPUTS</span></span>

### <span data-ttu-id="6d5af-123">PSAzureFirewallThreatIntelWhitelist에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6d5af-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="6d5af-124">상속자</span><span class="sxs-lookup"><span data-stu-id="6d5af-124">NOTES</span></span>

## <span data-ttu-id="6d5af-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d5af-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d5af-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6d5af-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="6d5af-127">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6d5af-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6d5af-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6d5af-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)