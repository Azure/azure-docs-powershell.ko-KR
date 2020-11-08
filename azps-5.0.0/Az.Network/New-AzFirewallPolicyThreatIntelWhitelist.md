---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216406"
---
# <span data-ttu-id="dad0b-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="dad0b-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="dad0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad0b-102">SYNOPSIS</span></span>
<span data-ttu-id="dad0b-103">Azure 방화벽 정책에 대 한 새 위협 인텔리전스 허용 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="dad0b-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="dad0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dad0b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad0b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dad0b-105">DESCRIPTION</span></span>
<span data-ttu-id="dad0b-106">**AzFirewallPolicyThreatIntelWhitelist** Cmdlet은 Azure 방화벽 정책을 만들거나 설정할 때 사용할 수 있는 위협 intel 허용 목록 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dad0b-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="dad0b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dad0b-107">EXAMPLES</span></span>

### <span data-ttu-id="dad0b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dad0b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="dad0b-109">이 예제에서는 한 항목의 FQDN 허용 목록와 두 항목의 Ip 주소 허용 목록를 포함 하는 위협 intel 허용 목록를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dad0b-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="dad0b-110">변수</span><span class="sxs-lookup"><span data-stu-id="dad0b-110">PARAMETERS</span></span>

### <span data-ttu-id="dad0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad0b-111">-DefaultProfile</span></span>
<span data-ttu-id="dad0b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dad0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad0b-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="dad0b-113">-FQDN</span></span>
<span data-ttu-id="dad0b-114">위협 인텔 허용 목록의 Fqdn</span><span class="sxs-lookup"><span data-stu-id="dad0b-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="dad0b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="dad0b-115">-IpAddress</span></span>
<span data-ttu-id="dad0b-116">위협의 IP 주소 인텔 허용 목록</span><span class="sxs-lookup"><span data-stu-id="dad0b-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="dad0b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad0b-117">CommonParameters</span></span>
<span data-ttu-id="dad0b-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad0b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad0b-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dad0b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad0b-120">입력</span><span class="sxs-lookup"><span data-stu-id="dad0b-120">INPUTS</span></span>

### <span data-ttu-id="dad0b-121">않아야</span><span class="sxs-lookup"><span data-stu-id="dad0b-121">None</span></span>

## <span data-ttu-id="dad0b-122">출력</span><span class="sxs-lookup"><span data-stu-id="dad0b-122">OUTPUTS</span></span>

### <span data-ttu-id="dad0b-123">PSAzureFirewallPolicyThreatIntelWhitelist에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dad0b-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="dad0b-124">상속자</span><span class="sxs-lookup"><span data-stu-id="dad0b-124">NOTES</span></span>

## <span data-ttu-id="dad0b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dad0b-125">RELATED LINKS</span></span>
