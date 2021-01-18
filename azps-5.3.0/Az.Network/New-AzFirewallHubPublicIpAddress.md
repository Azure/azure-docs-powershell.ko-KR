---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492630"
---
# <span data-ttu-id="c935b-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c935b-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="c935b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c935b-102">SYNOPSIS</span></span>
<span data-ttu-id="c935b-103">가상 허브의 방화벽에 연결된 공용 IP</span><span class="sxs-lookup"><span data-stu-id="c935b-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="c935b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c935b-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c935b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c935b-105">DESCRIPTION</span></span>
<span data-ttu-id="c935b-106">가상 허브의 방화벽에 연결된 공용 IP</span><span class="sxs-lookup"><span data-stu-id="c935b-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="c935b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c935b-107">EXAMPLES</span></span>

### <span data-ttu-id="c935b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c935b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="c935b-109">이렇게 하면 가상 허브에 연결된 방화벽에 2개 공용 IP가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c935b-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="c935b-110">이렇게 하면 백end에 IP 주소가 생성됩니다. 새 방화벽에 대해 ipaddresses를 명시적으로 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c935b-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="c935b-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="c935b-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="c935b-112">이렇게 하면 방화벽에 이미 있는 $publicIp 1, $publicIp 2를 유지하여 방화벽에 1개 새 공용 IP가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c935b-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="c935b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c935b-113">PARAMETERS</span></span>

### <span data-ttu-id="c935b-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="c935b-114">-Addresses</span></span>
<span data-ttu-id="c935b-115">허브에 연결된 방화벽의 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="c935b-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c935b-116">-Count</span><span class="sxs-lookup"><span data-stu-id="c935b-116">-Count</span></span>
<span data-ttu-id="c935b-117">공용 IP 주소 수</span><span class="sxs-lookup"><span data-stu-id="c935b-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c935b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c935b-118">-DefaultProfile</span></span>
<span data-ttu-id="c935b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c935b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c935b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c935b-120">CommonParameters</span></span>
<span data-ttu-id="c935b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c935b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c935b-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c935b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c935b-123">입력</span><span class="sxs-lookup"><span data-stu-id="c935b-123">INPUTS</span></span>

### <span data-ttu-id="c935b-124">없음</span><span class="sxs-lookup"><span data-stu-id="c935b-124">None</span></span>

## <span data-ttu-id="c935b-125">출력</span><span class="sxs-lookup"><span data-stu-id="c935b-125">OUTPUTS</span></span>

### <span data-ttu-id="c935b-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="c935b-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="c935b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c935b-127">NOTES</span></span>

## <span data-ttu-id="c935b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c935b-128">RELATED LINKS</span></span>
