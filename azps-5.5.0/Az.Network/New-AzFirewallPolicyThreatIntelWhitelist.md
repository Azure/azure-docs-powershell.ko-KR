---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189665"
---
# <span data-ttu-id="19716-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="19716-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="19716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19716-102">SYNOPSIS</span></span>
<span data-ttu-id="19716-103">Azure Firewall 정책에 대한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="19716-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="19716-104">구문</span><span class="sxs-lookup"><span data-stu-id="19716-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19716-105">설명</span><span class="sxs-lookup"><span data-stu-id="19716-105">DESCRIPTION</span></span>
<span data-ttu-id="19716-106">**New-AzFirewallPolicyThreatIntelWhitelist** cmdlet은 Azure Firewall 정책을 만들거나 설정할 때 사용할 수 있는 위협 Intel 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19716-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="19716-107">예제</span><span class="sxs-lookup"><span data-stu-id="19716-107">EXAMPLES</span></span>

### <span data-ttu-id="19716-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="19716-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="19716-109">이 예제에서는 하나의 항목의 FQDN 화이트리스트와 두 개의 항목으로 된 IP 주소 화이트리스트를 포함하는 위협 Intel 화이트리스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19716-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="19716-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19716-110">PARAMETERS</span></span>

### <span data-ttu-id="19716-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19716-111">-DefaultProfile</span></span>
<span data-ttu-id="19716-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19716-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19716-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="19716-113">-FQDN</span></span>
<span data-ttu-id="19716-114">위협 Intel 화이트리스트의 FQDNS</span><span class="sxs-lookup"><span data-stu-id="19716-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19716-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="19716-115">-IpAddress</span></span>
<span data-ttu-id="19716-116">위협 Intel 허용 목록의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="19716-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19716-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19716-117">CommonParameters</span></span>
<span data-ttu-id="19716-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19716-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19716-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19716-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19716-120">입력</span><span class="sxs-lookup"><span data-stu-id="19716-120">INPUTS</span></span>

### <span data-ttu-id="19716-121">없음</span><span class="sxs-lookup"><span data-stu-id="19716-121">None</span></span>

## <span data-ttu-id="19716-122">출력</span><span class="sxs-lookup"><span data-stu-id="19716-122">OUTPUTS</span></span>

### <span data-ttu-id="19716-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="19716-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="19716-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19716-124">NOTES</span></span>

## <span data-ttu-id="19716-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19716-125">RELATED LINKS</span></span>
