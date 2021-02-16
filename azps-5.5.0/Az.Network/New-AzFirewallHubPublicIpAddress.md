---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206752"
---
# <span data-ttu-id="52e0c-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52e0c-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="52e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="52e0c-103">가상 허브의 방화벽에 연결된 공용 IP</span><span class="sxs-lookup"><span data-stu-id="52e0c-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="52e0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="52e0c-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52e0c-105">설명</span><span class="sxs-lookup"><span data-stu-id="52e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="52e0c-106">가상 허브의 방화벽에 연결된 공용 IP</span><span class="sxs-lookup"><span data-stu-id="52e0c-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="52e0c-107">예제</span><span class="sxs-lookup"><span data-stu-id="52e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="52e0c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="52e0c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="52e0c-109">이렇게 하면 가상 허브에 연결된 방화벽에 2개 공용 IP가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e0c-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="52e0c-110">이렇게 하면 백end에 IP 주소가 생성됩니다. 새 방화벽에 대해 ipaddresses를 명시적으로 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="52e0c-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="52e0c-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="52e0c-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="52e0c-112">이렇게 하면 방화벽에 이미 있는 $publicIp 1, $publicIp 2를 유지하여 방화벽에 1개 새 공용 IP가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e0c-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="52e0c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52e0c-113">PARAMETERS</span></span>

### <span data-ttu-id="52e0c-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="52e0c-114">-Addresses</span></span>
<span data-ttu-id="52e0c-115">허브에 연결된 방화벽의 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="52e0c-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="52e0c-116">-Count</span><span class="sxs-lookup"><span data-stu-id="52e0c-116">-Count</span></span>
<span data-ttu-id="52e0c-117">공용 IP 주소 수</span><span class="sxs-lookup"><span data-stu-id="52e0c-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="52e0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e0c-118">-DefaultProfile</span></span>
<span data-ttu-id="52e0c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52e0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52e0c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e0c-120">CommonParameters</span></span>
<span data-ttu-id="52e0c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52e0c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e0c-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52e0c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e0c-123">입력</span><span class="sxs-lookup"><span data-stu-id="52e0c-123">INPUTS</span></span>

### <span data-ttu-id="52e0c-124">없음</span><span class="sxs-lookup"><span data-stu-id="52e0c-124">None</span></span>

## <span data-ttu-id="52e0c-125">출력</span><span class="sxs-lookup"><span data-stu-id="52e0c-125">OUTPUTS</span></span>

### <span data-ttu-id="52e0c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="52e0c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="52e0c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52e0c-127">NOTES</span></span>

## <span data-ttu-id="52e0c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52e0c-128">RELATED LINKS</span></span>
