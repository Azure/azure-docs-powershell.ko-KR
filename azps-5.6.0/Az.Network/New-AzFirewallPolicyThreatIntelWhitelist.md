---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960395"
---
# <span data-ttu-id="89610-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="89610-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="89610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89610-102">SYNOPSIS</span></span>
<span data-ttu-id="89610-103">Azure 방화벽 정책에 대한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="89610-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="89610-104">구문</span><span class="sxs-lookup"><span data-stu-id="89610-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89610-105">설명</span><span class="sxs-lookup"><span data-stu-id="89610-105">DESCRIPTION</span></span>
<span data-ttu-id="89610-106">**New-AzFirewallPolicyThreatIntelWhitelist** cmdlet은 Azure 방화벽 정책을 만들거나 설정할 때 사용할 수 있는 위협 인텔 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89610-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="89610-107">예제</span><span class="sxs-lookup"><span data-stu-id="89610-107">EXAMPLES</span></span>

### <span data-ttu-id="89610-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="89610-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="89610-109">이 예제에서는 하나의 항목의 FQDN 화이트리스트와 두 항목의 IP 주소 화이트리스트가 포함된 위협 인텔 화이트리스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89610-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="89610-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89610-110">PARAMETERS</span></span>

### <span data-ttu-id="89610-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89610-111">-DefaultProfile</span></span>
<span data-ttu-id="89610-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89610-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89610-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="89610-113">-FQDN</span></span>
<span data-ttu-id="89610-114">위협 인텔 화이트리스트의 FQDNS</span><span class="sxs-lookup"><span data-stu-id="89610-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="89610-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="89610-115">-IpAddress</span></span>
<span data-ttu-id="89610-116">위협 인텔 허용 목록의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="89610-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="89610-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89610-117">CommonParameters</span></span>
<span data-ttu-id="89610-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89610-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89610-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89610-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89610-120">입력</span><span class="sxs-lookup"><span data-stu-id="89610-120">INPUTS</span></span>

### <span data-ttu-id="89610-121">없음</span><span class="sxs-lookup"><span data-stu-id="89610-121">None</span></span>

## <span data-ttu-id="89610-122">출력</span><span class="sxs-lookup"><span data-stu-id="89610-122">OUTPUTS</span></span>

### <span data-ttu-id="89610-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="89610-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="89610-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89610-124">NOTES</span></span>

## <span data-ttu-id="89610-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89610-125">RELATED LINKS</span></span>
