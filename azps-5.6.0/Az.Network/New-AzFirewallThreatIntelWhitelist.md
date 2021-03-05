---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964155"
---
# <span data-ttu-id="412fb-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="412fb-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="412fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="412fb-102">SYNOPSIS</span></span>
<span data-ttu-id="412fb-103">Azure Firewall에 대한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="412fb-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="412fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="412fb-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="412fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="412fb-105">DESCRIPTION</span></span>
<span data-ttu-id="412fb-106">**New-AzFirewallThreatIntelWhitelist** cmdlet은 Azure 방화벽을 만들거나 설정할 때 사용할 수 있는 위협 인텔 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="412fb-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="412fb-107">예제</span><span class="sxs-lookup"><span data-stu-id="412fb-107">EXAMPLES</span></span>

### <span data-ttu-id="412fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="412fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="412fb-109">이 예제에서는 두 항목의 FQDN 화이트리스트와 두 항목의 IP 주소 화이트리스트가 포함된 위협 인텔 화이트리스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="412fb-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="412fb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="412fb-110">PARAMETERS</span></span>

### <span data-ttu-id="412fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412fb-111">-DefaultProfile</span></span>
<span data-ttu-id="412fb-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="412fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412fb-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="412fb-113">-FQDN</span></span>
<span data-ttu-id="412fb-114">위협 인텔 화이트리스트의 FQDNS</span><span class="sxs-lookup"><span data-stu-id="412fb-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="412fb-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="412fb-115">-IpAddress</span></span>
<span data-ttu-id="412fb-116">위협 인텔 허용 목록의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="412fb-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="412fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412fb-117">CommonParameters</span></span>
<span data-ttu-id="412fb-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="412fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412fb-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="412fb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412fb-120">입력</span><span class="sxs-lookup"><span data-stu-id="412fb-120">INPUTS</span></span>

### <span data-ttu-id="412fb-121">없음</span><span class="sxs-lookup"><span data-stu-id="412fb-121">None</span></span>

## <span data-ttu-id="412fb-122">출력</span><span class="sxs-lookup"><span data-stu-id="412fb-122">OUTPUTS</span></span>

### <span data-ttu-id="412fb-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="412fb-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="412fb-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="412fb-124">NOTES</span></span>

## <span data-ttu-id="412fb-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="412fb-125">RELATED LINKS</span></span>

[<span data-ttu-id="412fb-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="412fb-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="412fb-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="412fb-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="412fb-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="412fb-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)